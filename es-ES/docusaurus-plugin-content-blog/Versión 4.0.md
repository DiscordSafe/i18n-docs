---
title: Lanzamos la versión 4.0
date: 2020-04-25 00:00:00
author: Vicente
authorTitle: Developing D-Safe
authorImageURL: https://github.com/vicente015.png
image: /img/blog-covers/version-4.0.png
categories: [Noticias]
---
# ¡Bienvenido a la versión 4.0!

Después de 9 meses de trabajo, pensar mucho y unos largos y desesperantes dolores de cabezas debido a los errores hemos lanzado Discord Safe 4.0, una versión que trae una grandísima cantidad de nuevos comandos y funciones de los que estamos orgullosos de mostrar. Como no tengo ni idea de por donde empezar esto, empezaré dando un resumen de las principales novedades y después hablaré de cada una de ellas.
![Blog cover](/img/blog-covers/version-4.0.png)
<!--truncate-->
* * *

# El inicio de algo mayor
Durante el verano del año pasado hemos estado recopilando las quejas que se han enviado, hemos estado muy atentos a vuestras sugerencias para elaborar una lista de ideas para mejorar Discord Safe y más tarde gracias a la motivación que nos produce los usuarios empezamos a desarrollar el bot empezando por volver a escribir y mejorar el rendimiento del código que nos llevó unos meses.
Y poco a poco buscando tiempo libre donde podíamos debido a que también estamos estudiando fuimos programando el bot hasta llegar al día de hoy tan esperado, su lanzamiento. Estamos emocionados por conseguir acabar de una vez todo y poder mostrárselo a todos.

Con todos ustedes, unas palabras de uno de los programadores:

> Muchas gracias a todos por la espera que creo que la nueva versión ha merecido y debo decir de que nunca pero nunca os hagáis programadores de Discord Safe a no ser que queráis soportar que todos los días vicente te diga que tiene un error y que no sabe como solucionarlo para que al segundo te diga "nada ya lo solucioné" o sea un error tan básico que ni el se ha dado cuenta de como arreglarlo pero bueno mucha suerte en vuestros servidores y que paséis una feliz cuarentena ^_^ con la mayor seguridad posible :)
> Seyron, programador de Discord Safe.

Ahora sí, después de unas bonitas declaraciones, los dejo con las novedades. ╰(*´︶`*)╯♡

* * *

# Novedades
**Estas solo son las principales, la lista de novedades puedes verla en el [registro de cambios](https://blog.discordsafe.com/Noticias/Registro-de-cambios/registro-de-cambios).**

* Lenguaje.
* Verificación.
* Logs.
* Discord Safe Premium.
* Rewrite, todo el código ha sido rescrito.
* Limpieza del forceban.
* [Documentación](https://docs.discordsafe.com).
* Nueva página web y dominio.
* Desbaneo de los usuarios quitados del forceban.
* Usuarios añadidos al forceban durante solo un tiempo y con pruebas.
* Más comandos de moderación.
* Arreglo de bugs.
* Mejor sistema de reportes.
* Sistema de partners en nuestro servidor.
* [Blog](https.//blog.discordsafe.com) donde diremos noticias.
* Shards.
* Forceban Automático.
* Filtros.
* Alertas configurables de amenazas.
* Prefijo cambiable/custom.
* Aceptar menciones en comandos que pedían solo la ID.
* Nuevos diseños y logos.

## Lenguaje
Ahora Discord Safe estará disponible en multiples idiomas, así nos abiremos al mundo entero poco a poco.

Aún no podéis usarlo, no hemos alcanzado el nivel 3 en duolingo y cuesta acostumbrase a nuevas culturas.

## Verificación
Ahora tu servidor será más seguro contra selfbots y usuarios spammers con la verificación.
La verificación está disponible en cuatro modos:
1. Aprobación, mediante el comando ``d.aprobar @Usuario``d.
2. Reacción, el usuario debe reaccionar a un mensaje.
3. Verifiación, usando el comando ``d.verificarme``d.
4. Captcha, el usuario debe de completar un captcha por md.

## Logs
¿Hace falta explicar qué es esto? Ahora podrás tener constancia de todas las acciones que se realizan en el servidor.

## Discord Safe Premium.
![Discord Safe Premium](https://i.imgur.com/M1twWXZ.png "Discord Safe Premium")

Es un beneficio premium para Partners, Safers y donadores.

### Beneficios
* Filtro Iplogger Avanzado (+800 bloqueados).
* Filtro imágenes (NSFW o gore fuera de canales nsfw).
* Auto Forceban cada vez que se añade o quita un usuario.
* Más próximamente.

### ¿Cómo conseguirlo?
* Obteniendo Safer II, [saber más en nuestro servidor](https://discord.gg/UwqvMDZ).
* Siendo partner en [nuestro servidor](https://discord.gg/UwqvMDZ).
* [Patreon](https://patreon.com/DiscordSafe).

## Limpieza del forceban
Así es, hemos decidido empezar de 0 en el forceban, no te extrañes si dice "5 usuarios baneados con éxito".

### ¿Por qué?
1. La mayoría de los usuarios eran Deleted Users, es decir que habían sido baneados.
2. Al no tener un sistema como el de ahora que lo quita del forceban después de unos meses, habían raiders que habían dejado de raidear desde hace años y como no apelaban no se les eliminaba.
3. Era injusto, los miembros que eran quitados del forceban seguían baneados en la mayoría de servidores, hemos solucionado esto haciendo que también se desbaneen a los usuarios que han sido quitados del forceban al usar el comando `.forceban` **Esto solo se aplica a los baneos a partir de esta versión, los baneados anteriormente no podrán ser desbaneados.**
4. Se pedían muchos motivos, también hemos agregado que se tengan que añadir pruebas al añadir a un usuario al forceban siempre y cuando sea posible.
5. Hemos mejorado los críterios, ahora seremos más objetivos y comprobaremos bien a quién estamos baneando de tantos servidores.

## Nueva página web y dominio
Como estás leyendo, ahora tenemos una web oficial que funciona bien con un diseño moderno y que se adapta a todos los dispositivos.

### ¿Y qué hay nuevo?
* [Web](https://discordsafe.com)
* [Documentación](https://docs.discordsafe.com)
* [Blog](https://blog.discordsafe.com)
* [Estado](https.//status.discordsafe.com)

## Más comandos de moderación.
¡Por fin! Ya podéis moderar correctamente como es debido, los comandos de moderación ahora son:
* clear
* warn
* warnings
* clearwarn
* kick
* ban
* hackban
* mute
* unmute
* bloquearpalabra
* ignorar

## Mejor sistema de reportes.
¡Yep! Ahora los reportes irán por códigos, ahora los encargados de aceptarlos o rechazarlos lo tienen íncreiblemente más fácil y no se nos pasará ninguno sin aceptar o rechazar.

## Sistema de partners en nuestro servidor.
Eh, estó aún no está preparado del todo, pero si estás interesado pregunta en [nuestro servidor](https://discord.gg/UwqvMDZ).

## Blog
¿No lo estás viendo ya?

## Forceban Automático.
Exacto, los usuarios serán baneados o desbaneados automáticamente si tienes Discord Safe Premium.

## Filtros.
Exacto, ¿a quién no le gusta tener sus canales de su servidor más limpios que el culito de un bebé?
Los filtros disponibles son:
1. Invitaciones, no permite que los miembros que no son Administradores o no puedan modificar mensajes envien invitaciones.
2. Loggers, borra un mensaje si contiene un logger.
    * Básico.
    * Avanzado. **Premium**
3. Imágenes, analiza las imágenes y borra todo el contenido NSFW o gore fuera de canales NSFW. **Premium**
4. Anti Malware/Phishing/Scam, elimina los mensajes que contienen contenido malicioso.
5. Palabras, (ya existente) bloquea palabras, tales como insultos, etc.

## Alertas configurables de amenazas.
¿Tú también estabas cansado de que el bot te hablara por privado para avisarte de que ha entrado un usuario raider en tu servidor? Respondas sí como respondas no, ¡ahora será configurable!

## Prefijo cambiable/custom.
No sabéis cuantas veces habéis pedido esto, os podéis callar ya de una vez, gracias.

## Nuevos diseños y logos.
¿A quién no le viene bien cambiar un poco de aires?

* * *

# Agradecimientos
GRACIAS, **gracias** y _gracias_ a todos.

Sin vuestro apoyo no hubiera sacado la fuerza de voluntad para seguir porque soy un vago.
