# Óscar Curieses — web oficial

Web estática (HTML y CSS, sin WordPress ni base de datos) lista para publicar en GitHub Pages.

## Cómo publicarla en GitHub

1. Entra en github.com con tu cuenta y pulsa **New repository**. Ponle de nombre `oscar-curieses`, déjalo **Public** y créalo sin README.
2. En la página del repositorio vacío, pulsa **uploading an existing file**. Arrastra **todo el contenido de esta carpeta** (no la carpeta en sí: tienen que quedar `index.html`, `libros/`, `en/`, `img/`… en la raíz). Pulsa **Commit changes**.
   - El archivo `.nojekyll` está oculto en el Finder/Explorador. Si no se sube, no pasa nada grave, pero es mejor incluirlo (en Mac: Cmd + Mayús + . muestra los ocultos).
3. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama **main**, carpeta **/ (root)**, y guarda.
4. En uno o dos minutos la web estará en `https://TU-USUARIO.github.io/oscar-curieses/`. Ese es el enlace para revisarla.

## Conectar el dominio oscarcurieses.com (cuando se decida el cambio)

1. En **Settings → Pages → Custom domain** escribe `oscarcurieses.com` y guarda (GitHub crea solo el archivo `CNAME`).
2. En el panel donde se gestionan las DNS del dominio, crea:
   - Registros **A** para `@` apuntando a `185.199.108.153`, `185.199.109.153`, `185.199.110.153` y `185.199.111.153`.
   - Un registro **CNAME** para `www` apuntando a `TU-USUARIO.github.io`.
3. Cuando GitHub verifique el dominio, marca **Enforce HTTPS**.
4. Da de alta el dominio en Google Search Console y Bing Webmaster Tools y envía `https://oscarcurieses.com/sitemap.xml`.

Hasta que el dominio apunte aquí, la página 404 y los enlaces absolutos de las etiquetas SEO (canonical, Open Graph, sitemap) apuntan ya a oscarcurieses.com: es lo correcto para el lanzamiento.

## Estructura

| Español | Inglés |
|---|---|
| `/` (inicio) | `/en/` |
| `/libros/` y `/libros/<título>/` | `/en/books/` y `/en/books/<título>/` |
| `/performance/` | `/en/performance/` |
| `/bio/` | `/en/bio/` |
| `/contacto/` | `/en/contact/` |

- **Redirecciones**: las direcciones antiguas de WordPress (`/archivos/obras-literarias-2/…` y `/archivos/obras-literarias/…`) llevan a la ficha nueva de cada libro, para no perder enlaces ni posicionamiento. `/bio/` y `/contacto/` mantienen la misma dirección.
- **SEO**: cada página tiene título y descripción propios, URL canónica, versión ES/EN enlazada (hreflang), etiquetas para redes sociales (Open Graph) y datos estructurados de schema.org (Person para Óscar, Book para cada libro con ISBN, editorial, año y páginas cuando se conocen).
- **Imágenes**: en WebP, con dimensiones y carga diferida; las versiones JPG se usan solo al compartir en redes.
- `sitemap.xml`, `robots.txt`, `404.html` y `favicon.svg` incluidos.

## Pendiente de datos

- *El operario y la sal*: ISBN y número de páginas.
- *Hay una jaula en cada pájaro*: número de páginas.
- Revisión de la traducción inglesa por el autor.
