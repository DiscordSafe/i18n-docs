---
id: commands
title: Comandos
sidebar_label: Comandos
---
Lista de comandos de D-Safe.

Recuerda que no debes poner los siguientes símbolos al usar el comando.
* ` / ` Divide y separa las opciones de ese comando.
* `[]` Indica que el argumento es requerido.
* `<>` Indica que el argumento es opcional.

## Configuración {#config}

| Nombre       | Descripción                                                               | Uso                                                                                                      | Ejemplo                              | Permisos                    |
| ------------ | ------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------ | --------------------------- |
| blockword    | Bloquea el uso de palabras en el servidor.                                | `add [Palabra/Pack] / remove [Palabra/Pack] / ignore [#Canal/@Rol] / list / reset`                       | `d.blockword add pack 0`             | `MANAGE_MESSAGES`           |
| filter       | Configura los filtros.                                                    | `help / [filtro] enable / [filtro] disable / [filtro] ignore [#Canal/@Rol]`                              | `d.filter activate anti-spam`        | `MANAGE_ROLES MANAGE_GUILD` |
| logs         | Configura los los del servidor.                                           | `help / list / [#Canal/CanalID/disable] / mod [#Canal/CanalID/disable] / boost [#Canal/CanalID/disable]` | `d.logs #logs`                       | `MANAGE_GUILD`              |
| notification | Configura los avisos de entrada de usuarios maliciosos.                   | `on / off`                                                                                               | `d.notification on`                  | `ADMINISTRATOR`             |
| setlang      | Establece el idioma del bot en el servidor.                               | `es-ES / en-US`                                                                                          | `d.setlang es-ES`                    | `MANAGE_GUILD`              |
| setprefix    | Establece el prefijo en el servidor.                                      | `[Prefijo]`                                                                                              | `d.setprefix !!`                     | `MANAGE_GUILD`              |
| settings     | Muestra los ajustes del servidor e información sobre cómo configurarlo.   |                                                                                                          |                                      | `BAN_MEMBERS`               |
| setup        | Configure los ajustes del bot de forma sencilla con reacciones y botones. |                                                                                                          |                                      | `ADMINISTRATOR`             |
| whitelist    | Configura la Whitelist de su servidor.                                    | `add <ID> / remove <ID> / list / reset`                                                                  | `d.whitelist add 461171501715161108` | `BAN_MEMBERS`               |


## Información {#info}

| Nombre      | Descripción                                                   | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Ejemplo                                                                                                      | Permisos      |
| ----------- | ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------------- |
| botinfo     | Muestra la información del bot.                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |
| changelog   | Muestra el último registro de cambios.                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |
| commands    | Lista de comandos.                                            | `<--channel>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                                                                              |               |
| help        | Menú de ayuda e información de comandos.                      | `<Comando>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | `d.help ban`                                                                                                 |               |
| info        | Muestra la información de un usuario.                         | `<@Usuario/Usuario ID>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | `d.info @Vicente#0001`                                                                                       |               |
| invite      | Muestra la información de una invitación                      | `<Código invitación/Enlace invitación>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | `d.invite discord-testers`                                                                                   |               |
| mail        | Muestra el buzón de correos.                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |
| ping        | Muestra el ping del bot.                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |
| premium     | Panel de control de D-Safe Premium.                           | `help / redeem / info / safergen`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | `d.premium help`                                                                                             |               |
| reportbug   | Reporta un error a mi desarrollador para que sea solucionado. | `<Descripción detallada del error>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | `d.reportbug La alarma se enciende sola y no hay manera de apagarla.`                                        |               |
| role        | Muestra la información de un rol.                             | `<@Rol/Rol ID>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | `d.role @Usuario`                                                                                            |               |
| server      | Muestra la información del servidor.                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |
| suggest     | Envía una sugerencia.                                         | `<Descripción de la sugerencia>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | `d.suggest Me gustaría que creen un canal de #gaming donde los usuarios podemos hablar sobre ese tema allí.` |               |
| suggestions | Ajustes e información de las sugerencias.                     | `help` `list` `approve [IDSugerencia] <Comentario>` `deny [IDSugerencia] <Comentario>` `delete [IDSugerencia]` `setchannel [CanalID/#Canal/disable]` `setapproved [CanalID/#Canal/disable]` `setdenied [CanalID/#Canal/disable]` `questionEmoji enable / disable` `autoaccept [Número(1-1000)] / disable` `massapprove [IDSugerencia]...` `massdeny [IDSugerencia]...` `massdelete [IDSugerencia]...` `editcomment [SuggestionID] [New staff comment]` `setrole [Rol ID/@Rol]` `setpalette ayu / tailwind / default / p1 / p2 / p3 / n1 / n2 / n3` `setcommandschannel [CanalID/#Canal]` `setcooldown [Número(1-60)] / disable` `setemoji [EmojiPositivo] [EmojiNegativo] <EmojiIndeciso> / disable` | `d.suggestions setchannel #sugerencias`                                                                      |               |
| support     | Pide soporte a nuestro personal en caso de raid.              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              | `BAN_MEMBERS` |
| topbots     | Muestra la lista de top bots de Discord.                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |
| vote        | Muestra la información acerca de los votos.                   | ` / <@Usuario>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                              |               |

## Moderación {#mod}

| Nombre    | Descripción                                                        | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Ejemplo                                                                  | Permisos          |
| --------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ----------------- |
| ban       | Banea a un miembro del servidor.                                   | `[@Usuario/Usuario ID/Nombre miembro] <Razón> <--md> <--save>`                                                                                                                                                                                                                                                                                                                                                                                                               | `d.ban @Vicente#0001 Romper la regla 4.`                                 | `BAN_MEMBERS`     |
| case      | Muestra la información de un caso de moderación.                   | `[ID Caso]`                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | `d.case 5`                                                               | `MANAGE_MESSAGES` |
| cases     | Muestra la lista de casos de moderación del servidor.              | `<@Usuario>`                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |                                                                          | `MANAGE_MESSAGES` |
| clear     | Borra una cantidad de mensajes.                                    | `[Cantidad(2-100)]` `[@Usuario/Usuario ID] [Cantidad(2-100)]` `all` `match [Texto] [Cantidad(2-100)]` `not [Texto] [Cantidad(2-100)]` `startswith [Texto] [Cantidad(2-100)]` `endswith [Texto] [Cantidad(2-100)]` `links [Cantidad(2-100)]` `invites [Cantidad(2-100)]` `images [Cantidad(2-100)]` `mentions [Cantidad(2-100)]` `embeds [Cantidad(2-100)]` `bots [Cantidad(2-100)]` `before [ID Mensaje] [Cantidad(2-100)]` `after [ID Mensaje] [Cantidad(2-100)]` `around [ID Mensaje] [Cantidad(2-100)]` | `d.clear @Seyron#5532 15` `d.clear match RAID 100`                                 | `MANAGE_MESSAGES` |
| clearwarn | Elimina una advertencia del servidor.                              | `<Código> / all`                                                                                                                                                                                                                                                                                                                                                                                                                                                             | `d.clearwarn 43das78`                                                    | `BAN_MEMBERS`     |
| deafen    | Ensordece a un miembro.                                            | `[@Usuario/Usuario ID] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                                       | `d.deafen @Usuario Miembro molesto --md`                                 | `MANAGE_ROLES`    |
| forceban  | Banea a los usuarios reportados como peligrosos.                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                          | `MANAGE_GUILD`    |
| hackban   | Banea a miembros mediante su ID.                                   | `[ID] <ID> <ID>...`                                                                                                                                                                                                                                                                                                                                                                                                                                                          | `d.hackban 124545463433127 124545463433127 124545463433127`              | `BAN_MEMBERS`     |
| kick      | Expulsa a un miembro del servidor.                                 | `[@Usuario/Usuario ID/Nombre miembro] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                        | `d.kick Discord#0000 Romper la regla 8.`                                 | `KICK_MEMBERS`    |
| modstats  | Muestra estadísticas de los casos de moderación del servidor       | `actions / mods`                                                                                                                                                                                                                                                                                                                                                                                                                                                             | `d.modstats mods`                                                        | `MANAGE_MESSAGES` |
| mute      | Silencia a un miembro.                                             | `[@Usuario/Usuario ID] <Tiempo> <s/m/h> <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                      | `d.mute @Clyde#0001 15m Romper regla 14.`                                | `MANAGE_ROLES`    |
| reason    | Establece la razón de un caso de moderación.                       | `[ID Caso] [Razón]`                                                                                                                                                                                                                                                                                                                                                                                                                                                          | `d.reason 54 Roptura de la regla 16: No se permite spam en el servidor.` | `MANAGE_MESSAGES` |
| softban   | Banea e inmediatamente desbanea a un miembro para borrar mensajes. | `[@Usuario/Usuario ID] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                                       | `d.softban @Clyde#0001 Flood en el chat --md`                            | `BAN_MEMBERS`     |
| unban     | Desbanea a un usuario del servidor.                                | `[@Usuario/Usuario ID/Nombre miembro] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                        | `d.unban 287574458963722240`                                             | `BAN_MEMBERS`     |
| undeafen  | Desensordece a un miembro.                                         | `[@Usuario/Usuario ID] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                                       | `d.undeafen @Usuario`                                                    | `MANAGE_ROLES`    |
| unmute    | Desilencia a un miembro silenciado.                                | `[@Usuario/Usuario ID] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                                       | `d.unmute 182866681520062465`                                            | `MANAGE_ROLES`    |
| warn      | Advierte a un usuario de su mal comportamiento.                    | `[@Usuario/Usuario ID] <Razón> <--md>`                                                                                                                                                                                                                                                                                                                                                                                                                                       | `d.warn @Juan#4449 Romper la regla 3.`                                   | `KICK_MEMBERS`    |
| warnings  | Muestra lista de advertencias del servidor o miembro.              | `[@Usuario/Usuario ID]`                                                                                                                                                                                                                                                                                                                                                                                                                                                      | `d.warnings @Vicente#0001`                                               | `MANAGE_MESSAGES` |

## Utilidad {#util}

| Nombre      | Descripción                                                                | Uso                                         | Ejemplo                        | Permisos        |
| ----------- | -------------------------------------------------------------------------- | ------------------------------------------- | ------------------------------ | --------------- |
| alarm       | Configura la alarma en el servidor y prohibe la entrada a nuevos usuarios. |                                             |                                | `MANAGE_GUILD`  |
| avatar      | Muestra el avatar de un usuario.                                           | `<@Usuario>`                                |                                |                 |
| baninfo     | Muestra el motivo de forceban de un usuario.                               | `[ID]`                                      | `d.baninfo 287574458963722240` |                 |
| clearbans   | Quita todos los baneos del servidor.                                       |                                             |                                | `ADMINISTRATOR` |
| detect      | Detecta a usuarios peligrosos presentes en el servidor.                    |                                             |                                |                 |
| genpassword | Genera una contraseña acorde a los parámetros proporcionados.              | `<Nivel(low/medium/high)> <Longitud(5-50)>` | `d.genpassword Alto 26`        |                 |

## Verificación {#verification}

| Nombre       | Descripción                                           | Uso                                                                                                                                                                             | Ejemplo                              | Permisos       |
| ------------ | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ | -------------- |
| approve      | Aprueba la entrada al servidor a los nuevos usuarios. | `<@Usuario>`                                                                                                                                                                    | `d.approve @Vicente#0001`            | `MANAGE_ROLES` |
| verification | Modifica la configuración de la verificación.         | `off / setmode <Modo(approval, reaction, verification, captcha)> / setguest <@Rol / Rol ID> / setuser <@Rol / Rol ID> setchannel <#Canal / Canal ID> / setmessage <Mensaje ID>` | `d.verification setuser @Verificado` | `MANAGE_GUILD` |
| verifyme     | Te da el rol de usuario en el servidor.               |                                                                                                                                                                                 |                                      |                |


## Slash Commands

### Config

* blockword
    * ignore
        * channel
        * role
    * pack
        * add
        * remove
    * word
        * add
        * remove
    * help
    * list
    * reset
* filter
    * help
    * anti-iploggers
        * toggle
    * anti-spam
        * toggle
    * images
        * toggle
    * invites
        * toggle
    * ignore
        * channel
        * role
* setlang
* setprefix
* settings
* setup

### Info

* changelog
    * follow
    * view
* avatar
* botinfo
* commands
* help
* inviteinfo
* mail
* ping
* roleinfo
* serverinfo
* topbots
* userinfo

### Moderation

* clear
    * advanced
    * basic

* clearwarn
    * user
    * all
* ban
* case
* cases
* deafen
* hackban
* kick
* modstats
* mute
* reason
* softban
* unban
* undeafen
* unmute
* warn
* warnings

### Util

* suggestions
    * autoaccept
        * disable
        * set
    * channels
        * disable
        * set
    * customemojis
        * disable
        * set
    * palette
        * help
        * set
        * setcolor
    * approve
    * cooldown
    * delete
    * deny
    * disable
    * editcomment
    * help
    * list
    * massaction
    * questionemoji
    * role
* clearbans
* delrole
* emoji
* genpassword
* reportbug
* suggest

### Verification

* approve
    * all
    * user
* verification
    * setage
        * disable
        * set
    * disable
    * help
    * setattempts
    * setchannel
    * setguest
    * setmessage
    * setmode
    * settime
    * setuser
    * showconfig
* verifyme

