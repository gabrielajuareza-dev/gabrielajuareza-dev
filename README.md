# Portafolio profesional de Gabriela Juárez

Página estática en inglés para presentar un perfil de ingeniería de manufactura, ingeniería de proyectos e Industria 4.0 a reclutadores internacionales. Usa HTML, utilidades de Tailwind CSS 4 y componentes con estilos de Material Design 3.

Abre `index.html` con doble clic, o elige **Abrir con → Google Chrome** en el menú del archivo. Conserva la carpeta `assets/` al lado de `index.html`. La página y sus recursos visuales funcionan sin conexión, sin servidor y sin Node.js. El enlace a GitHub requiere internet.

## Dónde editar

| Archivo | Qué puedes cambiar |
| --- | --- |
| `index.html` | Nombre, cargo, presentación, áreas de enfoque, enlaces y metadatos del sitio. Los comentarios en español marcan las secciones. |
| `assets/theme.css` | Paleta, tipografía, tamaños, espaciado y estilos de cada componente. Empieza por las variables de `:root`. |
| `assets/site.css` | Utilidades de Tailwind compiladas, listas para usar. |
| `styles/tailwind.css` | Entrada del compilador autónomo si quieres añadir nuevas utilidades de Tailwind. |
| `assets/manufacturing.webp` | Fotografía de portada. Si usas otro archivo, cambia `src`, `alt` y el pie de foto en `index.html`. |
| `assets/favicon.svg` | Iniciales y color del icono de la pestaña. |

Puedes editar el HTML y `assets/theme.css`, guardar y recargar la pestaña. Actualiza también `<title>`, la descripción y las iniciales si cambias el nombre. Si añades un proyecto, usa un bloque `<article>` y describe el problema, tu contribución y un resultado que puedas compartir.

## Añadir correo, LinkedIn y CV

En el bloque `id="contact"` de `index.html`, añade los enlaces que necesites junto al botón de GitHub. Reemplaza los ejemplos con tus datos y guarda el PDF en `assets/` antes de enlazarlo.

```html
<a class="button button-primary" href="mailto:tu-correo@ejemplo.com">Email me</a>
<a class="button button-primary" href="https://www.linkedin.com/in/tu-perfil/">LinkedIn</a>
<a class="button button-primary" href="./assets/cv.pdf">View CV (PDF)</a>
```

## Añadir utilidades de Tailwind (opcional)

Este paso solo hace falta si añades clases de Tailwind que todavía no están en `assets/site.css`. Descarga el [CLI autónomo de Tailwind CSS](https://github.com/tailwindlabs/tailwindcss/releases/tag/v4.3.3) para tu sistema. En Windows x64, guarda `tailwindcss-windows-x64.exe` en Descargas y ejecuta desde la raíz del repositorio:

```powershell
& "$env:USERPROFILE\Downloads\tailwindcss-windows-x64.exe" -i ./styles/tailwind.css -o ./assets/site.css --minify
```

Incluye el `assets/site.css` regenerado en tu commit. GitHub Pages sirve la hoja estática incluida.

## Publicar en GitHub Pages

1. Confirma el nombre, los textos y los datos de contacto. Haz commit y sube los archivos a la rama `main`.
2. En el repositorio de GitHub, abre **Settings → Pages**.
3. En **Build and deployment**, elige **Deploy from a branch**. Selecciona **main** y **/(root)**, y pulsa **Save**.
4. Cuando finalice el despliegue, abre la URL que aparece en **Settings → Pages**. Comprueba la página y sus enlaces desde el móvil y el escritorio.

Las rutas locales empiezan con `./` para funcionar dentro de la ruta de un repositorio. Conserva `.nojekyll` en la raíz para servir el sitio tal como está. [Guía oficial de publicación desde una rama](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-from-a-branch).

## Créditos

- Fotografía de portada de [Lilian Do Khac en Unsplash](https://unsplash.com/photos/robotic-arms-assembling-a-car-chassis-on-a-factory-line-EyqUxJuOb1Q), bajo la [licencia de Unsplash](https://unsplash.com/license).
