---
title: Registro de cambios
slug: changelog-v4.0
date: 2020-04-26 00:00:00
authors: vicente
image: /img/blog-covers/changelog-4.0.png
tags: [update, v4.0]
---

A continuación podréis ver todos los cambios que se han hecho en la versión 4.0 de Discord Safe.
![Blog cover](/img/blog-covers/changelog-4.0.png)
<!--truncate-->
Los cambios están divididos en diferentes categorías:

* Generales.
* Arreglo de bugs/errores.
* Nuevas funciones/comandos.
* Webs.
* Bases de datos (forceban/whitelist/config/etc).

* * *

## Generales

1. 🌍 Sistema de lenguaje.
	1. Español.
	2. Inglés (aún no disponible).
2. 📔 Rewrite (todo el código ha sido rescrito).
3. 📊 Sharding (el bot ahora puede estar en más de 2500 servidores).
4. 🎨 Nuevos diseños y logos.
5. 📈 Mejora del rendimiento y estabilidad.
6. 📜 Mejor seguimiento y registro de los errores y comandos.

* * *

## Arreglo de bugs/errores

1. 🐛 Arreglo de bugs pequeños.
2. 🦎 No avisaba cuando no tenía los permisos necesarios para ejecutar las acciones.
3. 🐞 Error clear, no avisaba cuando no podía borrar los mensajes.
4. 🦗 Error info, en la fecha de entrada al servidor.
5. 🦟 Todos los errores que conocemos que hay en la nueva versión.

* * *

## Nuevas funciones/comandos

1. 🔒 Verificación.
	1. Aprobación, usando ``d.aprobar``.
	2. Reacción, reaccionando a un mensaje.
	3. Verificación, usando ``d.verificarme``.
	3. Captcha, completando un captcha.
2. 📥 Ajustes de avisos de raiders.
3. 🔑 Auto Forceban (Premium).
4. 🔧 Desbaneo de los usuarios que han sido eliminados del forceban al usar ``d.forceban``.
5. 💿 Prefijo customizable.
6. 📋 Filtros.
	1. Invitaciones.
	2. Anti Iploggers.
	4. Imágenes (Premium).
	5. Malicioso (Premium).
	6. Palabras (ya existente).
7. 🔧 Comando ajustes donde se ve la configuración actual de todas las configuraciones y como cambiar cada una de ellas.
8. 🔐 Generador de contraseñas por nivel de seguridad y longitud de la contraseña.
9. 🔬 Comando de ``d.reportarbug``.
10. 🎫 Mejora del comando info y server para desplegar más información.
11. 😄 Cambio en todos los emojis que usaba el bot.
12. 👥 Permitir menciones en los comandos: info, seenon, setanuncios, editanuncios, setlogs y otros ajustes.
13. 📃 Logs.
14. ✨ Cambios en el diseño de ``d.ayuda`` y ``d.comandos``.
15. 🔮 Mejorado el comando clear, ahora acepta usuarios ej: ``d.clear @Usuario <Cantidad>``
16. 📌 Añadir reacciones de votos cuando se envía una sugerencia.
17. 🎉 Discord Safe Premium.
	1. Filtro Imágenes.
	2. Filtros Malicioso.
	3. Filtro Anti Iploggers Avanzado.
	4. Auto Forceban
18. ⏰ Quitar a los usuarios del forceban después de unos meses.
19. 📤 DM al enviar sugerencia.
20. 🔧 Comando ``d.botinfo``.
21. 🔓 Añadida más información al usar el ``d.baninfo``.
22. 📕 Cambios en todos los mensajes de errores.
23. ⏱ Cooldown.
24. 📑 Información de como usar un comando usando ``d.ayuda <comando>``.
25. 🏓 Cambio en el diseño del comando ``d.ping``.
26. 🔨 Más comandos de moderación.
27. 🔨 Comando de warns almacenados por códigos.

* * *

## Webs

1. 🎏 Dominio web.
2. 🥁 [Web](https://discordsafe.com).
3. 📄 [Documentación](https://docs.discordsafe.com).
4. 📰 [Blog](https://blog.discordsafe.com).
5. 🔧 Arreglo de errores y faltas de ortografía.
6. 🎨 Nuevo diseño de las webs.

* * *

## Bases de datos

1. 💾 Nuevas bases de datos (premium, reportes, verificación, warns).
2. 🧹 Limpieza de las bases de datos, se han quitado los datos de servidores a los que no pertenecía.
3. 🚽 Borrado de datos del servidor automático al expulsar al bot, esto hace que las configuraciones se borren.
4. 🧼 Limpieza desde 0 del forceban.
5. 🚔 Nuevos valores al añadir un usuario al forceban: Prueba y Tiempo, la prueba será para mostrarla al usar ``d.baninfo`` y el tiempo será la fecha exacta en la que el usuario tiene que ser eliminado del forceban (normalmente 2 meses).
6. 💽 Reportes almacenados por códigos para hacer más fácil y efectivo el trabajo.
7. 📉 Mejora en el rendimiento de las bases de datos.

# Fin
Esos son todos los cambios, al menos que hasta ahora me haya acordado.
**Recordatorio:** Recuerda que puedes reportar errores usando el comando ``d.reportarbug``, lo agradecemos mucho.
Gracias a por llegar hasta aquí y leer, ¡se nota que te interesa lo que hacemos! (o˘◡˘o)

