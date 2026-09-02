# Sitio web NEXUS GSS

Sitio corporativo estático (HTML + CSS inline, sin build).

## Páginas
- `index.html` — redirección a Inicio
- `Nexus-Inicio.dc.html` — Inicio
- `Nexus-Oficina-Estrategica.dc.html` — Oficina Estratégica de Proyectos
- `Nexus-Areas.dc.html` — Áreas de trabajo
- `Nexus-Contacto.dc.html` — Contacto

## Recursos
- `assets/` — logo, emblema, GIFs de territorio
- `support.js`, `image-slot.js` — runtime de componentes y slots de imagen

## Publicación (GitHub Pages)
Settings → Pages → Source: `main` / raíz. El archivo `.nojekyll` evita el procesado Jekyll.

## Dominio
`CNAME` apunta a nexusgss.co. En el DNS del dominio crear registros A a 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 (o CNAME `juancpino-collab.github.io` para subdominio).

## Publicar
1. Subir todos los archivos a la raíz de `juancpino-collab/nexus` (rama `main`).
2. Settings → Pages → Source: `main` / `/ (root)`.
3. Settings → Pages → Custom domain: `nexusgss.co` → Enforce HTTPS.
