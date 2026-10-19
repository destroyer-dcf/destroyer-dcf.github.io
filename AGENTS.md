# AGENTS.md — destroyer.me

## Proyecto

- Sitio personal/blog de proyectos, construido con Jekyll y el tema local `the-plain`.
- Contenido principal: páginas Markdown/HTML en la raíz y entradas en `_posts/`.
- Configuración del sitio: `_config.yml`; layouts/includes: `_layouts/` y `_includes/`; estilos: `_sass/` y `assets/`.

## Entorno y comandos

- Requiere Ruby y Bundler; dependencias se declaran en `/Users/destroyer/Homelab/proyectos/destroyer-dcf.github.io/Gemfile` y `the-plain.gemspec`.
- Instalar dependencias: `bundle install`.
- Compilar el sitio: `bundle exec jekyll build` (genera `_site/`).
- CI histórico: `script/cibuild.sh` ejecuta build y `htmlproofer`; el validador apunta a `../_site`, por lo que puede no funcionar desde este repositorio sin adaptar la ruta.
- No hay suite de tests de aplicación identificada.

## Convenciones de contenido

- Las entradas viven en `_posts/` y usan el formato de nombre `YYYY-MM-DD-titulo.md`.
- Mantener el front matter YAML existente (`title`; `updated` cuando corresponda); las páginas y posts reciben layouts por defecto desde `_config.yml`.
- Escribir contenido del sitio en español y conservar el tono/documentación técnica de los posts existentes.
- Las imágenes compartidas van en `assets/`; respetar rutas y referencias existentes antes de mover recursos.
- Mantener enlaces, licencias y atribuciones de proyectos externos al editar documentación.

## Cambios y validación

- Leer los archivos afectados y seguir el estilo local; evitar reformateos no relacionados.
- No editar `_site/` como fuente: es salida generada por Jekyll.
- Tras cambios de contenido/configuración/plantillas, ejecutar `bundle exec jekyll build`.
- Tratar warnings de dependencias/Sass como avisos preexistentes salvo que el cambio los cause; no hacer migraciones amplias sin necesidad.
- No desplegar ni modificar configuración de publicación externa salvo petición explícita.
