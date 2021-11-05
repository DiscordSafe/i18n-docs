---
title: Versión 4.1
slug: v4.1
date: 2020-07-18 00:00:00
author: Vicente
authorTitle: Developing D-Safe
authorImageURL: https://github.com/vicente015.png
image: /img/blog-covers/version-4.1.png
categories: [Changelog]
---

Bienvenidos al registro de cambios que se han hecho desde las versiones 4.1.0 a la 4.1.9.

Esta versión ha sido mayoritariamente un arreglo de los errores que han existiendo en anteriores versiones, hemos priorizado arreglar los errores antes de introducir nuevas funciones y hemos añadido muy pocas nuevas funciones.
![Blog cover](/img/blog-covers/version-4.1.png)
<!--truncate-->
Antes de empezar con el registro de cambios me gustaría compartir algunas de las cosas que se vienen en las próximas versiones.

# Futuros cambios ✨
Ya hemos empezado a trabajar en la siguiente versión que viene con urgencia porque tenemos que hacer cambios grandes para la estabilidad y mantenimiento del bot en el futuro.

Algunas de las cosas muy esperadas que vendrán en las próxima s versiones son:
* Terminar la adaptación a múltiples lenguaje y TENER DE UNA PUTA VEZ EL BOT EN INGLÉS.
* Más comandos de moderación como: ``nickall, roleall, etc...``
* Reorganización del todo el sistema interno de comandos y lenguajes para que sea más sencillo para todos.
* Contador de votos para los Safers.
* Actualización urgente a Discord.js@v12.

* * *

# Registro de cambios: Versión 4.1

Los cambios están divididos en diferentes categorías:

* Generales.
* Arreglo de bugs/errores.
* Nuevas funciones/comandos.
* Webs.
* Bases de datos (forceban/whitelist/config/etc).

* * *

## Generales

1. 🏓 Nuevo prefijo/prefix predeterminado: ``d.``

	Hemos cambiado el prefijo por defecto del bot así que ahora mostrará un aviso cada vez que un usuario usa el anterior prefijo para que se vayan acostumbrando al nuevo prefijo.
2. 📈 Mejora del rendimiento y estabilidad quitando funciones temporalmente.

    Hemos quitado temporalmente la función de ``logs`` hasta arreglar los problemas de rendimiento.

* * *

## Arreglo de bugs/errores

1. 🐛 El ``mute`` no dice bien las razones.
2. 🦎 El ``ban ID`` no funciona.
3. 🐞 Las razones del comando ``warns`` se seleccionan mal e incompletas.
4. 🦗 La confirmación del ``reportar`` acepta cualquier cosa que no sea "Sí".
5. 🦟 El ``reportarbug`` manda bugs aunque no pongas "Sí".
6. 🐛 El "se unió al server" muestra el día actual y no el correspondiente.
7. 🦎 El filtro de spam detecta cualquier palabra suelta.
8. 🐞 El comando ``palabrasbloqueadas`` no manda nada.
9. 🦗 En el comando ``ajustes`` muestra dos veces el filtro de invitaciones.
10. 🦟 El ``seenon`` no es compatible con shards.
11. 🐛 La mención en el ``seenon`` dice que no se encuentra un usuario pero con la ID sí.
12. 🦎 El título del embed en ``filtros ayuda`` está pegado.
13. 🐞 El autoforceban para premiums no funciona en todos los shards.
14. 🦗 El ``forceban`` muestra la misma cantidad de baneados que de desbaneados.
15. 🦟 El ``setmensaje`` da error desconocido.
16. 🐛 No funcionan los webhooks de logs de comandos y soporte.
17. 🦎 Las sugerencias se envían en cada espacio.
18. 🐞 Hacer que se pueda desactivar la verificación.


* * *

## Nuevas funciones/comandos

1. ✨ Mejora en el comando ``ayuda``, cambios en todas las descripciones de los comandos, mejores ejemplos de uso y nuevos aliases.
2. 📥 En la lista de ``comandos`` ya aparecen todos los comandos sin ninguno repetido.
3. 🎏 Mejoras pequeñas: Aceptar mención en el ``unmute``, aceptar menciones en el comando ``info``, hacer que se manden en los logs las acciones del bot, aceptar ID en el ``ban``.
4. 🔧 Nuevo comando de ``unban``.
5. 📌 Ahora puedes aceptar a todos los usuarios pendientes con ``.aprobar todos``.
6. 🔮 Si pones ``@D-Safe prefix`` te dirá el prefijo actual del servidor.
7. 🔓 Mejorar las explicaciones de los comandos de ajustes.


* * *

## Webs

1. 🎆 Las páginas webs ahora se adaptan completamente al dispositivo del usuario.
2. 🍣 Se han quitado las referencias a ``discordapp.com`` y se ha cambiado por ``discord.com``.
3. 🎐 Se ha agregado el botón de política de cookies.

* * *

## Bases de datos

1. 🧹 Limpieza programada de la base de datos para quitar datos basura.

# Fin
Esos son todos los cambios, espero que te hayan entusiasmado porque nosotros seguiremos sin parar con el desarrollo de nuestro querido bot.

**Recordatorio:** Recuerda que puedes reportar errores usando el comando ``.reportarbug``, lo agradecemos mucho.
Gracias a por llegar hasta aquí y leer todo. <3 (o˘◡˘o)
