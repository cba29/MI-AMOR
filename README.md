# ❤️ Nuestro primer mes — Edith

Página romántica interactiva, adaptable a celulares y lista para GitHub y Netlify. Incluye 12 fotografías reales, video de Sucre, canción aportada, 20 razones interactivas, carta, contador y sorpresa final.

## Iniciar en tu computadora

1. Instala Node.js 20 o superior desde https://nodejs.org/.
2. Abre una terminal dentro de esta carpeta.
3. Ejecuta `npm install`.
4. Ejecuta `npm run dev`.
5. Abre la dirección que muestra la terminal (normalmente http://localhost:5173).

## Publicar en Netlify

1. Sube esta carpeta a un repositorio GitHub (no subas `node_modules`).
2. En Netlify, selecciona **Add new project → Import an existing project → GitHub**.
3. Elige tu repositorio. Comando de compilación: `npm run build`. Directorio de publicación: `dist`.
4. Publica. El archivo `netlify.toml` ya tiene la configuración.

También puedes ejecutar `npm run build` y subir manualmente la carpeta `dist` a Netlify Drop.

## Personalizar

Todo lo editable está en **`src/config.js`**:
- `nombre`: nombre de tu novia (algunos textos de diseño también dicen Edith en `src/main.js`).
- `fechaInicio`: fecha real en formato ISO con zona horaria peruana. **IMPORTANTE**: puse `2026-10-20T00:00:00-05:00` como fecha provisional porque el primer mes se celebra el 20 de noviembre de 2026. Cámbiala si corresponde otro mes o año.
- `momentos`: lugares, títulos, descripciones y fotos de la línea de tiempo.
- `fotos`: galería y leyendas.
- `razones`: las 20 razones.
- Para cambiar la carta, edita el texto dentro de `src/main.js`, buscando `Mi querida Edith`.

### Imágenes, música y video

Todos los archivos están en `public/assets/`. La galería usa versiones WebP optimizadas de las fotos originales. La canción incluida es la que aportaste y solo empieza cuando se pulsa el botón de música. Para sustituirla, reemplaza `public/assets/nuestra-cancion.mp3`. El video original está en `public/assets/sucre.mp4`. Si lo cambias, conserva ese nombre o actualiza `config.js`.

**Nota sobre derechos:** la canción comercial aportada puede estar sujeta a derechos de autor; publicarla en una web pública puede generar restricciones o reclamaciones. Si deseas compartirla públicamente, utiliza música con autorización.

## Verificación

- `npm run build` genera `dist` para producción.
- Se requiere interacción del usuario para reproducir música.
- Las fotos se pueden ampliar, navegar con flechas y cerrar con Escape.
- El contador se actualiza cada segundo y la fecha se modifica en `src/config.js`.
