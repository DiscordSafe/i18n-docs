---
title: Como recuperamos al bot de una muerte lenta
slug: como-recuperamos-al-bot
date: 2020-11-27 00:00:00
author: Vicente
authorTitle: Developing D-Safe
authorImageURL: https://github.com/vicente015.png
image: /img/blog-covers/como-salvamos-el-bot.png
categories: [Código]
---
# Cómo recuperamos el bot de una muerte lenta

**¡Hola a todos!**
Esta vez los desarrolladores vamos a hacer un post más técnico sobre la infraestructura de D-Safe. 
![Blog cover](/img/blog-covers/como-salvamos-el-bot.png)
<!--truncate-->
Durante estos últimos meses hemos superado retos los cuales nos han hecho aprender bastante a base de dolores de cabeza. Aunque parezca extraño, **son estos retos y las dificultades lo que nos mantiene seguir queriendo continuar este proyecto** desde hace más de 2 años. Si todo fuera sencillo ya lo hubiéramos abandonado.

Vamos comentando punto a punto qué cambios realizamos y cómo mejoramos el rendimiento y la estabilidad del bot más de un 60%. Antes de nada, un poco de contexto para entender la situación.

## Contexto
![Timeline](https://i.imgur.com/tr9ecD7.png)

## Abril - Versión 4.0
El 25 de Abril de 2020 lanzamos la versión 4.0, una actualización con muchos meses de trabajo donde reescribimos toda la base del código y lo estructuramos mejor. Además, hicimos caso a todas las sugerencias y comenzamos con el sistema de verificación, lenguaje, logs, filtros, etc.

### Junio - 3k de servidores
Llegamos a 3k de servidores.

## Julio - Versión 4.1
El 18 de Julio de 2020 lanzamos la versión 4.1, una actualización donde **nos limitamos a arreglar todos los bugs** que la versión anterior tuvo. Empezamos a monitorizar el rendimiento.

## Agosto - Problemas
A principios del mes de Agosto empezamos a presenciar que el consumo de recursos estaba elevándose más de lo normal.
Limitamos algunas funciones pero el rendimiento sigue empeorando.

- Logs.
- Filtros.

## Septiembre - Incidencias
A mediados de agosto y septiembre empiezan a haber **2 incidencias y problemas a la semana**. Empezamos a analizar duramente la estructura y a idear un plan para mitigar estos problemas.

Mejoramos los recursos de nuestro alojamiento (VPS) para intentar lidiar la situación, esto acaba **causándonos sobrecostes que no esperábamos**, amablemente pedimos donaciones.

![RAM Last Month](https://i.imgur.com/a1Fo5tD.png)

## Septiembre - Versión 4.2
Ya tenemos un plan para mitigar la situación así que cambiamos de librería, nos deshacemos de mucha caché que se obtenía automáticamente al iniciar el bot y mejoramos la estructura interna orientándola mejor a objetos.

**Las mejoras se empiezan a ver por fin y bajamos drásticamente los recursos**, a partir de aquí empezamos a mejorar aún más el rendimiento poco a poco con más calma y pensando bien las decisiones.

Tenemos un multilenguaje funcional, agrupamos y optimizamos todos los comandos. Y agregamos nuevas funciones geniales que se llevaban pidiendo un largo tiempo.

A partir de aquí el bot es más estable y el consumo de memoria no está tan disparatado, pero aumentaba poco a poco conformen pasaba la semana. Así que aún podíamos hacer algo más para mejorarlo.

## El impacto de la caché
### ¿Qué es "la caché?"
La cache hace referencia a todos esos datos que son guardados temporalmente en la memoria para ser utilizados.

El almacenamiento en caché es el proceso de mantener una copia de algo en la memoria. La mayoría de las librerías de Discord mantienen los datos recibidos de Discord en la memoria para cualquier necesidad eventual. El almacenamiento en caché de los datos de Discord da acceso a funciones como leer todos los canales, buscar algo por nombre o por cualquier otra cosa que no sea un ID, realizar la verificación de permisos, etc. El almacenamiento en caché es muy útil y hace posibles muchas funciones, pero a un costo grande...

### ¿Cómo afecta esto al bot?
Una vez que un bot empieza a crecer significablemente estos datos empiezan a ser un problema de consumo de recursos, especialmente de memoria RAM.

Esto es debido a que [discord.js](https://discord.js.org), la librería donde están miles bots y estaba D-Safe almacena en caché tanto como puede para evitar para evitar peticiones a la API de Discord, así es como consigue proporcionar muchas de las funciones. Sin embargo, esto es un problema ya que la librería está almacenando en caché datos que nunca usamos.

Decidimos que lo mejor sería cambiar de [librería](https://discord.com/developers/docs/topics/community-resources), pero queríamos que fuera lo menos complicado posible, no queríamos aprender otro lenguaje, nos plantamos usar la alternativa, **[Eris](https://abal.moe/Eris/)**, en esta librería están gran parte de los bots con más servidores de Discord, [fuente](https://gist.github.com/advaith1/451dcbca2d7c3503d4f48d63eb918cb0).

![img](https://i.imgur.com/jCj986n.png)

No queríamos reescribir de nuevo toda la estructura del código, por ello decidimos pasar a [discord.js-light](https://github.com/timotejroiko/discord.js-light). Esta librería ofrece y mantiene las mismas características que discord.js pero te permite elegir qué cosas que necesitas sean guardas en caché y cuáles son solicitadas directamente a la API de Discord.

En el siguiente gráfico pueden ver una comparativa del consumo y datos en caché entre diferentes librerías, [fuente](https://github.com/timotejroiko/discord.js-light#readme).

![img](https://github.com/timotejroiko/discord.js-light/raw/v3/bench.png)

### Pros y contras
Para entender mejor qué características ofrece esta, hágamos una comparativa:

#### Pros.
- Proporciona todos los eventos de discord.js, sin ningún tipo de caché automática.

- La mayor parte de estructuras en el código existente pueden seguir intactas.

- El sistema de partials (parciales en español) personalizado garantiza que los eventos se emitan independientemente del estado de la caché.

- La mayoría de las cosas las puedes solicitar o almacenar en caché cuando sea necesario.

- Reduce drásticamente el consumo de recursos a gran escala.

#### Contras.

- Aumenta el consumo de banda ancha, debido a que ahora la mayoría de los datos que se requieren son solicitados directamente.
- Mucha información que se recibe de los eventos puede estar limitada.
- Debes tener mucha más conciencia de qué datos estás usando y de cómo pueden afectar.


### Datos en caché.
Hay varios tipos de datos que puede controlar usando **discord.js-light**.

* **Servidores.**
	Este guarda la información de los servidores y sus propiedades, son muy útiles y necesarios para la mayoría de funciones.

* **Canales.**
	Los canales tienen un gran impacto en la memoria y el bot puede funcionar perfectamente sin ellos, pero si recibe actualizaciones de los canales como logs la información que reciba se verá afectada, aún se pueden adaptar de forma eficiente para que esta información limitada sea solicitada.

* **Roles.**
	Los roles pueden tener un impacto moderado en la memoria, son requeridos para comprobaciones de permisos generales. Puedes seguir obteniendo los roles de los miembros pero estos solo contendrán la ID y pueden ser solicitados. Los roles también podrán ser solicitados solo cuando sean necesarios.

* **Emojis**.
	Los emojis tienen un bajo impacto en la memoria, pero son solo necesarios si quiere listar emojis, buscar emojis por el nombre o recibir eventos de actualizados de ellos. De todas maneras, podrán ser obtenidos y usados por el bot usando la estructura de un emoji en Discord `<:NOMBRE DEL EMOJI:ID DEL EMOJI>` .

* **Presencias.**
	Las presencias son básicamente los estados del usuario, y tienen un muy gran impacto (sobretodo cuando tienes + 700.000 usuarios) en la memoria. Estos no son necesarios la mayor parte del tiempo y pueden ser solicitados cuando lo sean.

* **Usuarios y miembros.**
    Además del bot, todos los demás usuarios y miembros nunca se almacenan en caché automáticamente. Tener un caché de usuario incompleto no es muy útil la mayor parte del tiempo, por lo que es todo o nada. La opción de cliente `fetchAllMembers` se puede utilizar para almacenar en caché todos los usuarios y miembros; de lo contrario, se deben solicitar manualmente si es necesario. Los eventos que incluyen algunos datos de usuario por lo general no requieren ser recuperados, ya que el evento en sí ya contiene suficiente información.

* **Mensajes.**
	Tienen un gran impacto en memoria y la mayoría de veces no son necesarios, sigue pudiendo solicitar los mensajes directamente sin ser guardados. Desactivando esto afecta también a lo que recibe de los eventos que contienen mensajes. Los mensajes son guardados en caché solo si el canal que lo contiene está también en caché. La caché de mensajes puede ser controlada por las opciones del cliente como`messageCacheMaxSize`, `messageCacheLifetime` y `messageSweepInterval`.

### Experiencia
Discord.js-light proporciona una gran documentación que nos ha sido de gran utilidad para saber que nuevos métodos usar para solicitar información, qué datos son recibidos con los eventos y qué caché requiere para que funcionen ciertas cosas, en general debe tener **muy en cuenta los datos que tienes** al escribir código. Puede ver más en la su [documentación](https://github.com/timotejroiko/discord.js-light#readme).



Los principales cambios en D-Safe se vieron cuando desactivamos la caché de usuarios, presencias y la de canales. Con los usuarios y presencias solo se vio afectado el comando `info` y tuvimos reescribir el código donde se solicitaban usuarios. Pero, lo que más hemos tenido que sacrificar ha sido la caché de canales y por lo tanto de mensajes. Esto ha sido una gran mejora, pero no planeamos mantenerlo por mucho tiempo así ya que sacrificamos la información que podríamos proporcionar en los logs.

También tuvimos que sacrificar el comando `seenon`, ya que este requería comprobar en cada servidor miembros, además no era muy bien recibido por personas que se preocupaban de su privacidad.



A consecuencias de estos cambios, el consumo de banda ancha se vio ligeramente aumentado. Esto no ha sido un problema ya que nuestro alojamiento soporta de sobra la carga. Pero tendremos que ir regulando entre solicitar datos y guardarlos en caché al escalar en el futuro.
Además, nuestra estructura está soportada para evitar hacer más peticiones de las que debería para evitar ser [ratelimited](https://discord.com/developers/docs/topics/rate-limits).



En general, recomendaríamos hacer este cambio antes de que su bot se vea afectado, esto depende de cada uso y funciones del bot. En D-Safe empezó a ser a partir de los 5k de servidores, almacenar la información de millones de usuarios y miles de mensajes no es una buena idea.



![Bandwith](https://i.imgur.com/IWCDNyj.png)

## Actualidad - Versión 4.2.1
Empezamos a lanzar pequeñas actualizaciones semanales donde primero pasa por el proceso de **Testing** para evitar errores y tras comprobar que es estable se lanza.

La versión 4.2.1 es una pequeña mejora de la 4.2 que seguimos desarrollando donde hasta ahora hemos arreglado todos los bugs, mejorado el rendimiento y la estructura a la vez que sacamos mejoras en las funcionalidades.

![CPU Last Month](https://i.imgur.com/8eRO9PM.png)

### Noviembre - 7k de servidores
Llegamos a los 7k de servidores y tenemos un constante flujo de nuevos usuarios y servidores.

## Agradecimiento

Me gustaría agradecer a varios usuarios que nos han ayudado con este reto.

Los dos nuevos desarrolladores que están haciendo un gran trabajo:

 * [AcousticCat](https://discord.com/users/249561705066135552).

 * [Anventec](https://discord.com/users/715373744515710997).

Al mantenedor de  **discord.js-light**.

 * [Timotej Rojko](https://patreon.com/timotejroiko).

Y a varios usuarios por sus consejos en este tema.

* [perronosaurio](https://discord.com/users/237947982769553408).
* [Awoo](https://discord.com/users/224619540263337984).



## Conclusión

El crecimiento del bot es increíble y muchos nuevos usuarios lo están usando en el último mes, gracias a la resolución de este reto que no esperábamos hemos conseguido aprender sobre **escalabilidad, gestión de proyectos, estructura y programación orientada a objetos**, hemos tenido que aplicar todos estos nuevos conocimientos. Aunque cambiásemos de librería también tiene un gran impacto la estructura del código, nuestro objetivo es mantener un código limpio, estabilidad a la vez que vamos añadiendo y proporcionando nuevas funciones.



**¡Gracias por llegar hasta aquí! ＼(＾▽＾)／**