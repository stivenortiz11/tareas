# Organizador de tareas

Una app sencilla para organizar tus tareas de universidad y de trabajo en un mismo lugar. Registra el tiempo que dedicas a cada una y lleva el control del progreso. Todo funciona en el navegador, sin instalar nada.

## Cómo usarla

Abre `index.html` con doble clic. Se abre en tu navegador y ya está lista.

## Qué puedes hacer

- Crear tareas con título, detalle, categoría (Universidad o Trabajo), prioridad y fecha límite.
- Separar por pestañas: ver todas, solo universidad o solo trabajo.
- Cronometrar el tiempo dedicado a cada tarea con play y pausa. El contador sigue corriendo aunque cambies de vista, y solo hay un cronómetro activo a la vez para que el total sea real.
- Ajustar el progreso de 0 a 100 con la barra. Al llegar a 100 la tarea se marca como hecha.
- Marcar tareas como completadas con la casilla de la izquierda.
- Buscar por texto y ordenar por fecha, prioridad o progreso.
- Ver un resumen arriba: total de tareas, pendientes, atrasadas, porcentaje completado y tiempo registrado.
- Cambiar entre tema claro y oscuro con el botón del sol.

## Dónde se guardan los datos

Las tareas se guardan en el almacenamiento local de tu navegador (`localStorage`). No viajan a ningún servidor y no salen de tu equipo. Ten en cuenta dos cosas:

- Si borras los datos del sitio o usas otro navegador u otro equipo, no verás las mismas tareas.
- Un cronómetro en marcha se guarda al cerrar la pestaña, así que no pierdes el tiempo acumulado.

## Estructura

Es un solo archivo, `index.html`, con el HTML, los estilos y el código dentro. Fácil de copiar, mover o abrir sin conexión.
