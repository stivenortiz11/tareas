# Activar Google Drive (opcional)

La app funciona sin esto. Conecta Drive solo si quieres que tus tareas se sincronicen entre tu móvil y tus equipos. Necesitas un Client ID de Google, que se saca gratis. Toma unos 10 minutos la primera vez.

## Paso 1: crear un proyecto en Google Cloud

1. Entra a https://console.cloud.google.com/ con tu cuenta de Google.
2. Arriba, en el selector de proyectos, crea un proyecto nuevo. Ponle el nombre que quieras.

## Paso 2: activar la API de Drive

1. En el buscador de arriba escribe "Google Drive API" y entra.
2. Pulsa "Habilitar".

## Paso 3: configurar la pantalla de consentimiento

1. Ve a "APIs y servicios" y luego "Pantalla de consentimiento de OAuth".
2. Elige tipo "Externo" y continúa.
3. Rellena lo mínimo: nombre de la app y tu correo.
4. En "Usuarios de prueba", agrega tu propio correo (y el de quien vaya a usarla).

## Paso 4: crear el Client ID

1. Ve a "APIs y servicios" y luego "Credenciales".
2. Pulsa "Crear credenciales" y elige "ID de cliente de OAuth".
3. Tipo de aplicación: "Aplicación web".
4. En "Orígenes de JavaScript autorizados" agrega las direcciones desde donde abrirás la app. Por ejemplo:
   - `http://localhost:8000` (si la pruebas en tu equipo con un servidor local)
   - La URL de tu sitio en Netlify, por ejemplo `https://tu-sitio.netlify.app`
5. Crea y copia el "Client ID". Se parece a `1234567890-abcdef.apps.googleusercontent.com`.

## Paso 5: pegar el Client ID en la app

1. Abre `index.html`.
2. Busca esta parte, cerca del inicio del código:

   ```js
   var CONFIG = {
     googleClientId: ""
   };
   ```

3. Pega tu Client ID entre las comillas:

   ```js
   var CONFIG = {
     googleClientId: "1234567890-abcdef.apps.googleusercontent.com"
   };
   ```

4. Guarda y vuelve a subir la app a Netlify (o ábrela de nuevo).

## Usar Drive

Pulsa "Conectar Drive" en la cabecera, inicia sesión con Google y acepta el permiso. La primera vez la app crea el archivo `organizador-tareas.json` en tu Drive. A partir de ahí, cada cambio se guarda solo, y al conectar desde otro dispositivo con la misma cuenta verás las mismas tareas.

Nota: abrir la app desde una dirección que no esté en los "Orígenes autorizados" hará que Google rechace la conexión. Si cambias de URL, agrégala en el Paso 4.

## Importante sobre abrir el archivo directo

Google no permite el inicio de sesión cuando abres el archivo con `file://` (doble clic). Para usar Drive necesitas abrir la app desde una URL `http://` o `https://`: tu sitio de Netlify, o un servidor local. Un servidor local rápido, si tienes Python:

```
python3 -m http.server 8000
```

Luego abre `http://localhost:8000`.
