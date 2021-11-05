---
title: Versión 4.2
slug: v4.2
date: 2020-09-20 00:00:00
author: Vicente
authorTitle: Developing D-Safe
authorImageURL: https://github.com/vicente015.png
image: /img/blog-covers/version-4.2.png
categories: [Changelog]
tags: [D-Safe, Servidor Discord, "4.0"]
---

Bienvenidos al registro de cambios de la **versión 4.2**.

En esta versión hemos priorizado arreglar los problemas de consumo de recursos y latencia que nos estaban dando sobrecostes. Además, priorizamos arreglar y mejorar las funciones principales que más se usan del bot.
![Blog cover](/img/blog-covers/version-4.2.png)
<!--truncate-->

Antes de empezar a comentar los cambios, un pequeño avance de en lo que empezaremos a trabajar para próximas versiones.

# Futuros cambios ✨
Algunas de las cosas muy esperadas que vendrán en las próximas versiones son:
* Full configuración en todos los aspectos y funciones del bot.
* Rediseño y ampliación del contenido de la página web principal.
* Sistema de tickets de soporte.
* Más comandos de moderación  y utilidad.
* Contador de votos para los Safers.

Si esperas estos cambios, considera donarnos mediante [patreon](https://patreon.com/DiscordSafe) para pagar los costes que suponen. <3

* * *

# Registro de cambios: Versión 4.2

Los cambios están divididos en diferentes categorías:

* Generales.
* Nuevas funciones/comandos.
* Webs.
* Arreglo de bugs/errores.
* Bases de datos (forceban/whitelist/config/etc).

* * *

## Generales

1. 🌏 Multilenguaje funcional.

	Hemos arreglado y mejorado el sistema de lenguaje, **habrán nuevos lenguajes disponibles pronto**, pero para mejorar el uso y entendimiento de comandos al cambiar de lenguajes hemos decidido **cambiar los nombres de todos los comandos en Español y pasarlo a Inglés**.

2. 📦 Agrupación, revisión, optimización, rediseño y limpieza de comandos

    Hemos juntado los comandos que hacian varias acciones bajo la misma función en uno para que sea más consistente. Además, hemos optimizado y añadido nuevas funciones a los comandos actuales para que tengan una respuesta más óptima y rápida. 

3. 📊 Mejora de los problemas de consumo de recursos elevados.

    El bot estaba teniendo una gran cantidad de fallos, errores e incidentes debido a lo mal optimizado que está, hemos mejorado todo lo posible esto y seguramente hagamos otra publicación hablando más técnicamente acerca de esto.

### Lista de cambios en los comandos:
```diff
+ announcement
- setanuncios editanuncios delanuncios
+ report
- reportar
+ settings 
- ajustes
+ filters
- filtros 
+ setlang
- idioma 
+ notifications
- avisos
+ whitelist add/rem/list/reset
- ignorar, resetearwhitelist
+ blockword add/rem/list/reset
- bloquearpalabra, palabrasbloqueadas, resetearpalabras
+ help
- ayuda
+ commands
- comandos
+ reportbug
- reportarbug
+ support
- soporte
+ suggest
- sugerencia
+ alarm
- alarma, desactivaralarma
+ clearbans
- limpiarbans 
+ detect 
- detectar
+ genpassword 
- generarcontraseña
+ verification, approve, verifyme
- verificación, aprobar, verificarme
```

* * *

## Nuevas funciones/comandos

1. ⛔ Mejorar el anti-spam y ponerlo en 3 modos **(alto, medio, bajo)** e integrar anti-flood. `d.filters activate anti-spam <Nivel>`
2. 📥 Arreglar el modo ``captcha`` y mejorarlo, ahora funciona y se envia al canal de verificación en vez de por MD.
3. 📄 Pasar y mejorar la mayoría explicaciones de configuraciones a la documentación.
4. 🔧 Mejorar el sistema de usuarios bloqueados y servidores bloqueados, ahora hay un registro público en nuestro servidor con razones de por qué son añadidos.
5. ❌ Palabras bloqueadas: Que detecte también mensajes editados, quitar negrita, acentos y tildes para ser más sensible.
6. 🎮 Añadir un estado exclusivo del bot donde ponga que está jugando Among Us.
7. 📑 Que si no pones una id en el ``seenon`` te muestre tu seenon.
8. ⏩ Agregarle paginación al ``seenon`` y al ``warnings``, ahora se pueden ver todos los servidores y warns.
9. 🎨 Rediseñar embeds de reportes.
10. 🥚 Algunos easter eggs y funciones ocultas interesantes.
11. 🔐 Ajuste de mínimo de edad de las cuentas al entrar al servidor, ``d.verification setage <1-30 Días>``
12. 💾 **¡Han vuelto los logs!**
13. 🎻 Añadir más iploggers a las listas y mejorar el filtro.
14. ✨ **Comandos reescritos:**
    + **Ignorados:**
        Que no se pueda añadir a personas que no estén en el forceban.
        Hacer limpieza de la base de datos.
        Poder añadir varios.
        Poner embed con las pruebas etc cuando añade a alguien y esperar confirmación por reacción.

    + **Anuncios:**
        Meter del delanuncios, setanuncios y editanuncios en un solo comando

    + **Palabras bloqueadas.**
        Poder quitar una palabra exacta o todas.
        Poder añadir varias a la vez.
        Hacer limpieza de la base de datos.
        Poder añadir packs (paquetes) de palabras bloqueadas preseleccionadas por nosotros.

* * *

## Webs

1. 🎏 **¡Nueva [documentación](https://docs.discordsafe.com)!** Completa, con más páginas, con mejores ejemplos y mucho mejor redactada, diseñada y desarrollada para facilitarle las tareas de configuración a los moderadores.
2. ✨ Nueva política de privacidad del bot.

* * *

## Arreglo de bugs/errores

1. 🐛 Agregarle cooldown aunque el bot diga que no tiene permisos de usar ese comando.
2. 🦎 Arreglar el modo ``captcha`` de la verificación.
3. 🐞 Cambiar los permisos que requieren los usuarios al usar comandos para que tengan sentido.
4. 🦗 Poner más filtros al comando ``report`` para evitar el abuso.
5. 🦟 El ``ban`` da un error cuando tratas de banear a un usuario que no está en el servidor.
6. 🐛  El comando ``seenon`` da error muy pocas veces cuando el embed sobrepasa el límite de líneas en un embed, parece ser que no funciona el método que hicimos para evitar esto no funciona correctamente.
7. 🦎 El bot puede dejar de añadir/quitar un rol en la verificación a veces por razones desconocidas.
8. 🐞 No es posible ver todos los warns en el comando ``warnings`` cuando son demasiados, hay que añadir paginación.
9. 🦗 El comando ``warnings`` en búsqueda por mención puede dar error cuando el usuario no se encuentra en el servidor.
10. 🦟 No funciona el ``@D-Safe prefix`` en algunos servidores
11. 🐛 El ``forceban`` puede interrumpirse durante el proceso en muy poca cantidad de servidores.
12. 🦎 El ``seenon`` y el ``info`` pueden no encontrar a los usuarios cuando están en diferentes shards.
13. 🐞 Error de baneo desconocido en el comando unban.
14. 🦗 El comando ``mute`` da mensajes de error incorrectos.
15. 🦟 Falta de ortografía en el ``forceban``.
16. 🐛 El bot no dice nada cuando tratas de desbanear a un usuario con el ``unban`` poniendo una mención, debería rechazarlo.
17. 🦎 **Más de 42 bugs arreglados durante el proceso de pruebas en la fase beta.**
    Gracias a todos los Testers que participaron en esto **<3**.

* * *

## Bases de datos

1. 🧹 Limpieza programada de la base de datos para quitar datos basura.
2. 📃 Nuevas tablas de servidores y usuarios bloqueados.
3. 🔑 Nuevas opciones en la verificación, nuevas opciones en los ajustes.
4. 🧹 Limpieza de la base de datos de la whitelist y warnings.

# Fin
Esos son todos los cambios, espero que te hayan entusiasmado porque nosotros seguiremos sin parar con el desarrollo de nuestro querido bot.

Gracias a por llegar hasta aquí y leer todo. <3 (o˘◡˘o)
