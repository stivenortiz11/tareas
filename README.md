# Organizador de tareas

Una app sencilla para organizar tus tareas de universidad y de trabajo en un mismo lugar. Registra el tiempo que dedicas a cada una y lleva el control del progreso. Todo funciona en el navegador, sin instalar nada.

## Cómo usarla

Abre `index.html` con doble clic. Se abre en tu navegador y ya está lista.

## Qué puedes hacer

- Crear tareas con título, detalle, categoría (Universidad o Trabajo), prioridad y fecha límite.
- Asignar personas a cada tarea, no solo a ti. Se muestran como iniciales en la tarjeta y puedes buscarlas por nombre.
- Dividir cada tarea en pasos (checklist). El avance se calcula solo según los pasos que marcas.
- Separar por pestañas: ver todas, solo universidad o solo trabajo.
- Cronometrar el tiempo dedicado a cada tarea con play y pausa. El contador sigue corriendo aunque cambies de vista, y solo hay un cronómetro activo a la vez para que el total sea real.
- Ajustar el progreso a mano con la barra cuando la tarea no tiene pasos.
- Marcar tareas como completadas con la casilla de la izquierda.
- Ver un aviso arriba cuando hay tareas atrasadas o para hoy, así no se te pasa nada.
- Buscar por texto o por persona y ordenar por fecha, prioridad o progreso.
- Ver un resumen arriba: total de tareas, pendientes, atrasadas, porcentaje completado y tiempo registrado.
- Saltar a tu app de gastos con el botón de la cabecera.
- Cambiar entre tema claro y oscuro con el botón del sol.

## Usarla desde cualquier lugar

Como es un solo archivo, puedes subirla a Netlify igual que tu app de gastos: arrastra el `index.html` a un sitio nuevo y tendrás un enlace para abrirla desde el móvil o cualquier equipo.

Ten en cuenta que, por ahora, los datos se guardan por navegador. Si abres el enlace en el móvil y en el portátil, cada uno tendrá sus propias tareas. Para que se sincronicen entre dispositivos y entre personas hace falta un paso más (ver más abajo).

## Lo que aún falta decidir

Estas cosas no caben en un archivo suelto y necesitan un servicio detrás:

- Sincronizar entre tus dispositivos y compartir tareas en vivo con otras personas.
- Guardar en tu Google Drive.
- Adjuntar un pantallazo y que la tarea se cree sola leyendo la imagen (necesita una IA con visión).

Cada una requiere crear una cuenta o unas claves. Cuando elijas el camino, se conecta.

## Dónde se guardan los datos

Las tareas se guardan en el almacenamiento local de tu navegador (`localStorage`). No viajan a ningún servidor y no salen de tu equipo. Ten en cuenta dos cosas:

- Si borras los datos del sitio o usas otro navegador u otro equipo, no verás las mismas tareas.
- Un cronómetro en marcha se guarda al cerrar la pestaña, así que no pierdes el tiempo acumulado.

## Estructura

Es un solo archivo, `index.html`, con el HTML, los estilos y el código dentro. Fácil de copiar, mover o abrir sin conexión.
