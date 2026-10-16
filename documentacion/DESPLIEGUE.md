# Despliegue en GitHub Pages

1. Crea un repositorio y sube todo el contenido de esta carpeta.
2. En Settings → Pages elige la rama `main` y la carpeta `/ (root)`.
3. Abre `https://USUARIO.github.io/REPO/` una vez con internet.
4. iPad (Safari): Compartir → Añadir a pantalla de inicio. Android (Chrome): menú → Instalar app.

Después funciona sin conexión.

## Actualizar la app

La carpeta raíz contiene la versión compilada (`index.html`, un solo archivo con todo incluido). El código editable está en `src/`. Después de cambiar el código hay que volver a compilar a un solo archivo. Cuando subas una versión nueva, cambia el número de `CACHE` en `sw.js` (por ejemplo `puebla360-v4`) para que los dispositivos descarguen la nueva.

## Probar el código fuente

Abre `src/` con un servidor local (extensión Live Server de VS Code o `npx serve src`). No abras el archivo con doble clic.
