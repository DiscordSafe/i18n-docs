---
id: comparison
title: Comparación con otros bots
sidebar_label: Comparación con otros bots
---

Esta es una comparación entre D-Safe y otros bots de moderación

La fuente de esta información está basada en [este artículo de la "Escuela de Moderadores de Discord"](https://discord.com/moderation/1500000178701-321:-Auto-Moderation-in-Discord), no tenemos ninguna intención de mantener de forma actualizada el contenido.

En un futuro tenemos planeado añadir a las tablas otras características relevantes que tiene D-Safe que no están mencionadas.

Tratamos de ser lo más objetivos posibles, no vamos a poner "planeado" para las cosas que no tiene el bot y especificaremos lo que está limitado a premium, para ver notas que le pueden afectar sobre la implementación de otros bots por favor diríjase al artículo fuente mencionado arriba.


## Anti-Spam
Una de las formas más comunes de auto moderación es el anti-spam, un tipo de filtro que previene distintos tipos de spam.

| Tipo de spam             | D-Safe | Mee6 | Dyno | Giselle | Gaius | YAGPDB | Carl | Gearbot |
|--------------------------|--------|------|------|---------|-------|--------|------|---------|
| Mensajes rápidos (flood) | ✅      | ❌    | ✅    | ✅       | ✅     | ✅      | ✅    | ❌       |
| Texto repetido           | ✅      | ✅    | ✅    | ✅       | ✅     | ✅      | ❌    | ❌       |
| Texto con muchas líneas  | ✅      | ❌    | ❌    | ✅       | ✅     | ❌      | ❌    | ❌       |
| Menciones                | ✅      | ✅    | ✅    | ✅       | ✅     | ✅      | ✅    | ✅       |
| Enlaces                  | ✅      | ✅    | ✅    | ✅       | ✅     | ✅      | ✅    | ✅       |
| Invitaciones             | ✅      | ✅    | ✅    | ✅       | ✅     | ✅      | ✅    | ✅       |
| Imágenes                 | ✅*      | ❌    | ✅    | ✅       | ✅     | ❌      | ✅    | ❌       |
| Emojis                   | ✅      | ✅    | ✅    | ❌       | ✅     | ❌      | ❌    | ❌       |
* D-Safe ofrece un filtro para limitar la cantidad de imágenes enviadas en X tiempo y un filtro de imágenes NSFW que es [premium](premium/index.mdx).

## Filtros de texto
Los filtros de texto le permiten controlar los tipos de palabras y/o enlaces que los usuarios tienen permitido usar en su servidor.

| Filtro              | D-Safe | Mee6  | Dyno    | Giselle | Gaius | YAGPDB | Carl  | Gearbot |
|---------------------|--------|-------|---------|---------|-------|--------|-------|---------|
| Palabras bloqueadas | ✅      | ✅     | ✅       | ✅       | ✅     | ✅      | ✅     | ✅       |
| Whitelist           | ✅      | ❌     | ❌       | ✅       | ✅     | ✅      | ❌     | ✅       |
| Plantillas          | ✅      | ❌     | ✅       | ❌       | ✅     | ❌      | ❌     | ❌       |
| Inmunidad           | ✅      | ✅     | ✅       | ✅       | ✅     | ✅      | ✅     | ✅       |
| Enlaces bloqueados  | ✅      | ✅     | ✅       | ❌       | ✅     | ✅      | ✅     | ✅       |
| Whitelist           | ❌      | ✅     | ❌       | ❌       | ✅     | ✅      | ✅     | ✅       |
| Plantillas          | ✅      | ❌     | ❌       | ❌       | ✅     | ✅      | ✅     | ❌       |
| Invitaciones        | ✅      | ✅     | ✅       | ✅       | ✅     | ✅      | ✅     | ✅       |
| Extras              |        | Zalgo | Selfbot |         | Regex | Regex  | Archivos |         |

## Anti-raid
Los raids, son entradas masivas de usuarios (a menudo selfbots) con la intención de dañar su servidor. Para mayor información sobre los términos aquí mencionados por favor diríjase al artículo que usamos como fuente mencionado al principio.

|                                | D-Safe | Mee6 | Dyno | Giselle | Gaius | YAGPDB | Carl | Gearbot |
|--------------------------------|--------|------|------|---------|-------|--------|------|---------|
| Detección de raids             | ✅      | ❌    | ❌    | ✅       | ❌     | ❌      | ❌    | ❌       |
| Prevención de raids            | ✅      | ❌    | ❌    | ✅       | ✅     | ❌      | ❌    | ❌       |
| Detección de usuarios en raids | ✅      | ❌    | ❌    | ✅       | ✅     | ❌      | ❌    | ❌       |
| Prevención de daños            | ✅      | ❌    | ✅    | ❌       | ✅     | ❌      | ✅    | ❌       |
| Anti-spam en raids             | ✅      | ❌    | ✅    | ✅       | ✅     | ✅      | ❌    | ❌       |
| Limpieza del raid              | ✅      | ❌    | ✅    | ✅       | ✅     | ✅      | ✅    | ✅       |

## Filtros de usuario
Los mensajes no son la única forma en la que los usuarios maliciosos pueden presentar contenido desagradable a su servidor. También pueden manipular su nombre de usuario o apodo de Discord para causar problemas.

| Filtro         | D-Safe | Mee6 | Dyno | Giselle | Gaius | YAGPDB | Carl | Gearbot |
|----------------|--------|------|------|---------|-------|--------|------|---------|
| Palabras malas | ❌      | ❌    | ❌    | ❌       | ✅     | ✅      | ❌    | ❌       |
| Spam           | ✅      | ❌    | ❌    | ❌       | ✅     | ✅      | ❌    | ❌       |
| Hoisting       | ❌      | ❌    | ❌    | ❌       | ✅     | ✅      | ❌    | ❌       |
