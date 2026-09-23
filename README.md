# Organizador de tareas

Una app para organizar tus tareas de universidad y de trabajo en un mismo lugar. Registra el tiempo que dedicas, lleva el control del avance y te avisa de lo que se vence. Es un sitio estático: un solo `index.html`, sin servidor propio. Funciona sola y no depende de Claude ni de ninguna licencia.

## Cómo usarla

Abre `index.html` con doble clic y listo. También puedes subirla a Netlify (ver más abajo) para abrirla desde el móvil o cualquier equipo.

## Qué puedes hacer

- Crear tareas con título, detalle, categoría (Universidad o Trabajo), prioridad y fecha límite.
- Asignar personas a cada tarea, no solo a ti. Se ven como iniciales en la tarjeta y puedes buscarlas por nombre.
- Dividir cada tarea en pasos (checklist). El avance se calcula solo según los pasos que marcas.
- Cronometrar el tiempo por tarea con play y pausa. Solo corre un cronómetro a la vez para que el total sea real.
- Ver un aviso arriba cuando hay tareas atrasadas o para hoy.
- Crear una tarea desde un pantallazo: subes la captura, se lee el texto y se rellenan los campos. Luego revisas y ajustas.
- Buscar, ordenar por fecha, prioridad o progreso, y cambiar entre tema claro y oscuro.
- Saltar a tu app de gastos con el botón de la cabecera.

## Lectura de pantallazos (OCR)

Al subir una captura, el texto se lee dentro del navegador con OCR (Tesseract.js). No se envía a ningún servidor ni necesita cuenta ni clave. La primera vez descarga los datos de idioma desde internet, así que conviene tener conexión. Rellena el título, el detalle y, si los detecta, la categoría, la prioridad y la fecha. Es una ayuda, no magia: revisa siempre lo que quedó.

## Guardar en Google Drive (opcional)

Por defecto las tareas se guardan en el navegador donde abres la app. Si quieres que se sincronicen entre tus dispositivos, puedes conectar tu Google Drive. Es opcional y la app funciona igual sin ello. Los pasos para activarlo están en `SETUP.md`.

Cuando conectas Drive, la app guarda un archivo `organizador-tareas.json` en tu Drive y lo usa para cargar y guardar tus tareas. Solo ve ese archivo suyo, no el resto de tu Drive.

## Usarla desde cualquier lugar

Como es un sitio estático, súbela a Netlify igual que tu app de gastos: arrastra la carpeta (o el `index.html`) a un sitio nuevo y tendrás un enlace. No hace falta configurar nada más para que funcione, porque no usa servidor.

## Dónde se guardan los datos

En el almacenamiento local del navegador (`localStorage`), y además en tu Google Drive si lo conectas. Sin Drive, cada navegador o equipo tiene sus propias tareas. Un cronómetro en marcha se guarda al cerrar la pestaña.

## Estructura

- `index.html`: toda la app (HTML, estilos y código).
- `netlify.toml`: configuración mínima para publicar en Netlify.
- `SETUP.md`: cómo activar Google Drive.
