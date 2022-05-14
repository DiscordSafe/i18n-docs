---
title: Versión 5.0
slug: v5.0
date: 2022-05-14 00:00:00
authors: vicente
image: /img/blog-covers/version-5.0.png
categories: [Changelog]
tags: [D-Safe, "5.0"]
---

La versión 5.0 ya está aquí, después de un largo desarrollo, esta nueva versión está enfocada en mejorar radicalmente la moderación con D-Safe y hacerla accesible para todo el mundo. 🚀🌍

![Blog cover](/img/blog-covers/version-5.0.png)

<!--truncate-->

## Prólogo 📖 {#preface}

Un poco de explicación sobre cómo hemos llegado hasta aquí.

D-Safe se creó hace cuatro años con <u>su principal característica siendo el forceban</u>, una lista de usuarios maliciosos donde los usuarios podían contribuir reportando, su objetivo era evitar que estos usuarios dañaran servidores haciendo que no puedan entrar a ellos, <u>el bot nunca se centró en moderación desde el principio</u>, debido a esto fuimos cada vez dándole forma añadiendo funciones de moderación, anti-spam, verificación, etc.

Pero seamos sinceros, como el objetivo principal no era la moderación <u>las características de moderación como el anti-spam estaban incompletas y eran poco eficientes y poco avanzadas.</u>

**Eso cambia hoy.** 🍃

## Objetivos 🪄 {#gaosl}

Los cambios en esta versión han sido basados en los siguientes objetivos:

* 🛠️ **Moderación avanzada**, [hemos convertido a D-Safe en el mejor bot de moderación](/docs/intro/comparison).

* 🦾 **Configuración accesible**, nosotros también odiamos que parece que tengas que tener 8 cursos y 4 títulos para poder configurar un bot, <u>queremos un bot fácil de configurar y accesible para todo el mundo sin limitar sus funciones más esenciales</u>.

* 🎨 **Innovación**, queremos crear nuevas funciones de las maneras más creativas aprovechando las nuevas funciones que Discord ofrece a los bots.

* ✏️ **Diseño consistente**, queremos que sientas que el bot es único y que sea reconocible.

* 😀 **Experiencia de usuario**, queremos asegurar que nuestros usuarios tengan una una buena experiencia usando el bot, que todo funcione y esté como ellos lo esperan.

![gif](https://i.imgur.com/enwzRCM.gif)

## Nuevas características :sparkles: {#new-features}

¡Todas estas características las puedes probar ya! Algunos títulos pueden llevarte a la página que explica cómo configurar eso.

### Generales 🎏 {#general-changes}

- **[Todos los comandos han sido pasados a comandos de barra diagonal](/docs/basics/commands)**, tan solo escribe `/` y pruébalos.

  ![gif](https://i.imgur.com/p0VfFYb.gif)

- **Comandos de menú contextual**, ahora puedes ver la información de un usuario, sus casos aprobar una sugerencia, establecer el mensaje de verificación y un montón de cosas más haciendo solo dos clicks.
  ![gif](https://i.imgur.com/VbgIBEZ.gif)

- **Nueva página web, documentación y blog**, ya la estás viendo, puedes darte un paseo por ella, la nueva documentación incluye:

  - Barra de búsqueda.
  - Tema claro y oscuro.
  - Futuro soporte para otros idiomas.
  - Mejor organización.

  ![img](https://i.imgur.com/8MinnW4.png)

- **[Nuevos comandos](/docs/basics/commands)**, una tonelada de nuevos comandos, la mayoría solo están disponibles mediante barra diagonal.

  * `setup` configura varios aspectos del bot seleccionando opciones.
  * `deafen` y `undeafen` para ensordecer/desensordecer a un miembro.
  * `emoji` muestra el emoji agrandado.
  * `inviteinfo` muestra la información de una invitación.
  * `roleinfo` muestra la información de un rol.
  * `suggestions editcomment` edita los comentarios del staff de las sugerencias ya aprobadas/denegadas.
  * `topbots` muestra el top de bots de Discord.
  * `softban` banea y desbanea inmediatamente para borrar todos sus mensajes.
  * `delrole` elimina un rol.
  * `antinuke` configura el anti-nuke.
  * `antiraid` configura el anti-raid.
  * `modroles` configura los roles de moderadores.
  * `punishment` configura la moderación automática.
  * `lock`, `unlock` y `lockdown` bloquean canales.
  * `case` y `cases` visualiza los casos de moderación.
  * `duration` cambia la duración de una sanción.
  * `modstats` ver estadísticas de la moderación.
  * `reason` cambiar la razón de un caso
  * `cooldown` cambia el modo lento del canal.

- **[Insignias de D-Safe](/docs/basics/faq#safebadges)**, se mostrarán en `/userinfo` y `/server`.

- **¡Soporte a nuevas características de Discord!**

  - Todos los selectores por reacciones han sido reemplazados por botones.
  - Nuevo formato de fechas y tiempo.
  - Logs de hilos y eventos.
  - Ícono de rol y enlace en `/roleinfo`.
  - Soporte a avatares por servidor en `/avatar` y `/userinfo`.
  - Soporte a banners y color personalizado en `/userinfo`.

### Moderación 🔨 {#moderation}

- **[Anti-nuke](/docs/config/antinuke)** limita las acciones de administrador que se pueden hacer en un tiempo.

- **[Anti-raid](/docs/config/antiraid)** limita la cantidad de usuarios que pueden entrar a la vez.
  ![gif](https://i.imgur.com/uCT8CiI.gif)

- **[Auto moderación avanzada](/docs/config/automod)**, haz que el bot se encargue de moderar él solo.

- **¡Casos de moderación!**
  Ahora cada acción de moderación se guardará como caso (con un número único) con información del usuario sancionado, moderador, acción, razón, tiempo, etc.

  * `/cases`: ver los casos ordenados por recientes.
  * `/case`: ver la información de un caso.
  * `/reason`: añadir o editar la razón de un caso.

  :warning: *Se han migrado internamente todos los warns como casos, como no se guardaba la fecha en los warns aparecerá una incorrecta.*

- **Estadísticas de moderación**,
  con el nuevo comando `/modstats` puedes ver gráficos de los casos, los moderadores más activos y más en un futuro.

  ![img](https://i.imgur.com/5z13nie.png)

- **[Logs de casos](/docs/config/logs#mod)**, podras ver cada acción que se realiza con el bot.

  ![img](https://i.imgur.com/8u3gyMH.png)

- **[Roles de moderadores](/docs/config/moderation)**, configura quién puede usar los comandos de moderación.

- **[Ignorar canales o roles en los filtros](/docs/config/filters#ignore)**, una de las cosas más solicitadas ya está aquí.

- **[Nuevos packs de palabras bloqueadas](/docs/config/blockedwords#blockedwords-packs)**.

- **[Nuevos tipos de logs, más avanzados](/docs/config/logs)**.

- **[Nuevos filtros](/docs/config/filters)**, ahora no existe un solo filtro llamado "anti-spam", ahora está divido en varias partes que puedes elegir.

  * <u>Flood</u>, borra mensajes enviados rápidamente.
  * <u>Palabras repetidas</u>, borra mensajes con muchas palabras repetidas.
  * <u>Mayúsculas</u>, borra mensajes con exceso de mayúsculas.
  * <u>Estafas</u>, borra enlaces fraudulentos con motivos económicos.
  * <u>Phishing</u>, borra enlaces que suplantan a Discord y otras empresas para recopilar información y/o robar cuentas.

![gif](https://i.imgur.com/zk9s0fu.gif)

- [Bloqueador de enlaces](/docs/premium/config#block-links).

- **+15 opciones en el `/clear advanced`**, borra solo invitaciones, mensajes que contengan una palabra y más.

- **Más opciones avanzadas en todos los comandos de moderación**.

- [Whitelist de palabras bloqueados](/docs/config/blockedwords#whitelist)

### Verificación 🛡️ {#verification}

- [Nuevo modo de verificación](/docs/config/verification#modes) usando esta nueva característica de Discord.

  ![gif](https://cdn.discordapp.com/attachments/750725274748059799/970785009709514782/DiscordCanary_iRi1kILXtZ.gif)

- [Filtro de no avatar](/docs/config/verification#no-avatar), expulsará a los nuevos miembros que no tengan avatar.

- Ya no es necesario tener la verificación configurada para poder configurar la [edad mínima de la cuenta](/docs/config/verification#min-age)

- Ahora puedes aprobar a un usuario con `/approve` independientemente del modo de verificación.

- Ahora la imagen del captcha es más pequeña para que en móviles se pueda ver el último carácter correctamente.

- Ahora el captcha no es sensible a mayúsculas ni espacios.

- Respuestas del bot mejoradas para ser más fáciles de entender.

### Premium 💜 {#premium}

El premium ha sido completamente renovado.

- [Nuevos beneficios](/docs/premium#features).
- Nuevos precios.
- Ya no se puede obtener el premium mediante voto, la funcionalidad de votos ha sido eliminada.
- Ahora puedes tener varios premiums para varios servidores.
- Gestión del premium completamente integrada en Discord con el comando `/premium`.
- Hemos dejado de usar Patreon.

## Mejoras varias :pushpin: {#improvements}

- Mails del `/mails` ordenados bien por fecha, un alivio para tus ojos.
- Nuevas opciones en todos los comandos de moderación.
- <u>Rediseño</u>

  * Nuevos emojis diseñados por nosotros para usar en elementos de la interfaz.
  * Nuevos colores.

- Se borra el mensaje que hizo la persona cuando envía una sugerencia
- Imágenes en `/avatar` a máxima calidad.
- El commands edita el mensaje de "revisa tus mds" si no puede y envía la lista de comandos al canal directamente.
- Soporte a todos los formatos de colores en `/suggestions palette setcolor`.
- Un montón de mejoras de calidad más que no son tan relevantes.
- Ahora los logs usarán webhooks en vez de ser enviados por el bot.
- Los logs de mensajes borrados incluyen un botón para ir al mensaje respondido si este respondía a alguno.


## Arreglo de bugs :bug: {#bugs}

Hay muchísimos arreglos de bugs ero solo incluimos los relevantes que estaban desde la anterior versión.

* Logs de mensajes borrados con solo la ID.

* La verificación por reacción no funciona si tienes configurado el canal de sugerencias.

## Cosas eliminadas 💀 {#shit-removed}
En esta versión hemos decidido quitar algunas cosas.

- Comandos desactivados (solo disponibles mediante comandos de barra diagonal): info, role, server, setup, suggestions, delrole, genpassword, setprefix, blockword.
- Comandos eliminados: whitelist, baninfo, forceban, report, detect, support, alarm.
- Se ha eliminado el soporte a los canales de tienda, fueron eliminados por Discord.

Los motivos para estos cambios pueden ser:

1. Dificultad para seguir manteniendo dicha funcionalidad.
2. El objetivo principal del comando ha quedado obsoleto y ha sido reemplazado por algo mejor.
3. Poca utilidad, utilidad reemplazada por nueva función.

## Agradecimientos 💞 {#thank-you}

![gif](https://c.tenor.com/U45Q8YaJzBUAAAAC/moti-hearts.gif)

Gracias a los safers que han contribuido económicamente, a los traductores por hacerlo accesible a todo el mundo, a los miembros de la beta que aportaron sus sugerencias sobre los nuevos cambios,a los testers por reportar bugs, a los nuevos desarrolladores que han aportado su granito de arena y su creatividad, **gracias a tí y a todos por hacer este proyecto una realidad**.

> Dicho todo esto, espero que os guste la nueva versión, estaré unos días arreglando bugs y después me retiraré a comer cocos en una playa. 🥥🏖️
>
> \- Vicente.
