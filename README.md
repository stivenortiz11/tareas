# Mis Tareas

Una app para organizar tus tareas de universidad y de trabajo, cada una en su espacio. Decide qué conviene hacer primero, lleva el control del avance y te avisa de lo que se vence. Es un sitio estático: un solo `index.html`, sin servidor propio. Funciona sola y no depende de Claude ni de ninguna licencia.

## Cómo usarla

Abre `index.html` con doble clic y listo. También puedes subirla a Netlify (ver más abajo) para abrirla desde el móvil o cualquier equipo.

## Qué puedes hacer

- **Universidad y Trabajo como espacios independientes**, cada uno con su color (azul y ámbar) en las pestañas. Si solo usas uno, apaga el otro desde Ajustes: desaparece de las pestañas, del formulario y de las estadísticas, sin perder lo que ya tenías si lo vuelves a encender.
- Crear tareas con título, detalle, categoría (Universidad o Trabajo), prioridad y fecha límite.
- Asignar personas a cada tarea, no solo a ti. Se ven como iniciales en la tarjeta y puedes buscarlas por nombre.
- Dividir cada tarea en pasos (checklist). El avance se calcula solo según los pasos que marcas.
- Escribir una nota en cada paso para dejar constancia de qué se hizo.
- Varias notas por tarea, con fecha. Al cambiar de estado te pregunta si **ocultar** las notas de la etapa anterior o **mantenerlas**; las ocultas quedan guardadas y se pueden volver a ver.
- Estado por etapas (Sin revisar, Revisado, Iniciada, A la mitad, Casi lista, Terminada), con una barra de color que muestra el avance.
- Ver un aviso arriba cuando hay tareas atrasadas o para hoy.
- Crear una tarea desde un pantallazo: subes la captura, se lee el texto y se rellenan los campos. Entiende también fechas dichas de forma relativa ("mañana", "pasado mañana", "el próximo lunes"). Después de leerla, te muestra en chips **qué detectó** (categoría, fecha, prioridad, materia, persona) para que lo revises de un vistazo antes de guardar.
- **Orden sugerido** (el que trae por defecto): calcula qué conviene hacer primero combinando la fecha límite, la prioridad, lo que ya llevas empezado y el tiempo estimado.
- Las tareas se agrupan en bloques: **Atrasadas, Para hoy, Esta semana, Más adelante y Sin fecha**.
- **Plan del día** en la vista Hoy: las 3 tareas por las que conviene empezar, con el motivo de cada una y cuántas horas suman frente a las horas de clase que tienes ese día.
- **Aviso de días congestionados**: te marca cuando se te juntan 3 o más entregas el mismo día en las próximas 2 semanas.
- **Sugerir pasos**: si una tarea no tiene checklist, propone los pasos típicos según de qué trate (taller, informe, examen, exposición, ticket de soporte, etc.).
- **Tiempo estimado** por tarea, usado para planificar y priorizar.
- **Aviso de tareas estancadas**: marca las que empezaste pero llevan días sin movimiento.
- Vista **Hoy**: tus clases del día según el horario, más lo atrasado y lo que vence en los próximos 7 días.
- Vista **Calendario**: mes completo con las entregas marcadas por color (atrasada, pendiente, terminada). Tocas un día y ves sus tareas.
- Ver el **avance por materia**: cuántas llevas hechas, el porcentaje y cuántas están atrasadas.
- Guardar un **enlace** en cada tarea (aula virtual, ticket) y abrirlo desde la tarjeta.
- **Duplicar** una tarea, y borrar de una vez todas las realizadas.
- Tareas que se repiten (cada semana, cada 2 semanas o cada mes): al terminarlas se crea sola la siguiente.
- Vista compacta para ver muchas tareas de un vistazo, y "Marcar todos" los pasos de golpe.
- Contadores en las pestañas y atajos de teclado (N para nueva tarea, / para buscar).
- Elegir con cuánta antelación quieres el aviso (mismo día, 1, 2, 3, 5 o 7 días).
- **Resumen cada mañana** (opcional): una sola notificación con tu tarea más urgente y cuántas clases tienes hoy. Los avisos y recordatorios se revisan solos cada pocos minutos mientras tienes la app abierta, así no dependen de que hagas algo para refrescarse.
- Buscar, filtrar por materia y ordenar por fecha, prioridad, progreso o materia. Tema claro y oscuro.
- Ver la fecha con aviso claro: "hoy", "mañana", "en 2 días" o "atrasada 3 días".
- Ver tu horario recreado como tabla semanal editable (botón "Horario"): agregar, editar y quitar clases con día, hora y salón. También puedes subir el pantallazo original.
- Descargar una copia de respaldo y restaurarla cuando quieras.
- Instalarla en el celular como app (Agregar a pantalla de inicio) para abrirla a pantalla completa.
- Saltar a tu app de gastos con el botón de la cabecera.

## Dónde funciona

- **Celular:** diseño pensado para pantalla pequeña; el resumen y los filtros ocupan poco para que veas tus tareas enseguida. Se puede instalar desde el navegador ("Agregar a pantalla de inicio") y abrirla a pantalla completa.
- **Computador:** el contenido se centra y aprovecha el ancho sin estirarse de más.
- **Sin conexión:** te avisa arriba y puedes seguir trabajando; los cambios se guardan en el equipo y se sincronizan con Drive cuando vuelve la conexión. La lectura de pantallazos sí necesita internet la primera vez.
- **Almacenamiento lleno:** si el navegador se queda sin espacio te avisa y te dice qué hacer, en vez de fallar en silencio.
- **Impresión:** al imprimir salen solo las tareas, sin botones ni filtros, con fondo blanco y sin cortar tarjetas por la mitad.

## Lectura de pantallazos (OCR)

Al subir una captura, el texto se lee dentro del navegador con OCR (Tesseract.js). No se envía a ningún servidor ni necesita cuenta ni clave. La primera vez descarga los datos de idioma desde internet, así que conviene tener conexión. Rellena el título, el detalle y, si los detecta, la categoría, la prioridad y la fecha. Es una ayuda, no magia: revisa siempre lo que quedó.

## Acceso privado con Google

La app trae configurado un Client ID de Google (el mismo de la app de gastos). Con eso, al abrirla pide iniciar sesión con Google y no muestra nada hasta que entras. Tus tareas viven en tu Google Drive, así que solo tú, con tu cuenta, las ves, igual que en la app de gastos.

Guarda un archivo `organizador-tareas.json` en tu Drive y lo usa para cargar y guardar. Solo ve ese archivo suyo, no el resto de tu Drive. Como los datos están en Drive, entras desde el móvil y el portátil y ves las mismas tareas.

Para que el login funcione, la URL desde donde abres la app tiene que estar en los "orígenes autorizados" del Client ID en Google Cloud (por ejemplo tu sitio de Netlify). Si algún día quieres quitar el login y volver al modo local, deja `googleClientId` vacío en el código. Los pasos completos están en `SETUP.md`.

## Usarla desde cualquier lugar

Como es un sitio estático, súbela a Netlify igual que tu app de gastos: arrastra la carpeta (o el `index.html`) a un sitio nuevo y tendrás un enlace. No hace falta configurar nada más para que funcione, porque no usa servidor.

## Dónde se guardan los datos

En el almacenamiento local del navegador (`localStorage`), y además en tu Google Drive si lo conectas. Sin Drive, cada navegador o equipo tiene sus propias tareas. Un cronómetro en marcha se guarda al cerrar la pestaña.

## Estructura

- `index.html`: toda la app (HTML, estilos y código).
- `netlify.toml`: configuración mínima para publicar en Netlify.
- `SETUP.md`: cómo activar Google Drive.
