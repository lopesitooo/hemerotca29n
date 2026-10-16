# Cómo trabajar en esta web

- La web entera es `public/index.html`. Se publica automáticamente en el Worker de Cloudflare `small-mud-7edc` (hemeroteca29n.com) al hacer push a `main` (Workers Builds ejecuta `npx wrangler deploy` con `wrangler.jsonc`). No hay paso de compilación.
- El dueño no programa: explicarle todo en español, sin comandos.
- Datos dentro de `public/index.html`:
  - `S` = mapa de fuentes `clave:["Medio","url"]`.
  - `PERSONAS` = fichas `{n,r,p,e:[{v,d,x,s}]}`; `d` es la fecha `AAAA-MM` o `AAAA`; dentro de cada ficha, lo más reciente primero.
  - `FICHAS` = tarjetas de Pedro Sánchez (se ordenan solas por la fecha de `who`).
  - `NOTICIAS` = lista `{f:"AAAA-MM-DD", go:"slug-de-ficha" o "", t, x, s}`. Se añaden, nunca se borran. El calendario se genera solo.
  - `FRASES` = textos que se escriben solos en la cabecera.
- Reglas de contenido: cada dato con fuente enlazada; distinguir condenado / a juicio / investigado / publicado / archivado; incluir la respuesta del afectado; no meter rumores ni frases sin registro. Si una noticia ya está en una ficha, también va en noticias del día.
- Para revisar noticias: The Objective, El Mundo, OKDiario, Libertad Digital, El Debate, Vozpópuli, El Español, ABC, El Confidencial y agencias (EFE/Europa Press).
- Antes de subir: comprobar que la página carga sin errores de JavaScript.
