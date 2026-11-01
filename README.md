# Mi Día

Aplicación web para apoyar la comunicación de un niño con TEA nivel 1, pensada para usarse en familia desde el celular o la tablet.

## Qué incluye

- **Mi día**: agenda visual con "Ahora" y "Después", voz, marcar actividades terminadas y aviso visual de cambios.
- **¿Cómo me siento?**: emociones y "¿Qué necesito?" para pedir abrazo, descanso, agua o ayuda.
- **Mi familia**: ver a la familia, juegos "¿Dónde está?" y "¿Quién es?" y armar su nombre con letras.
- **Primero / Después**: tablero de dos pasos con temporizador visual.
- **Botón AYUDA** siempre visible y **modo padres** protegido (mantener presionado el candado 1,5 s) para cargar fotos, audios y actividades.

Las intervenciones en las que se apoya (apoyos visuales, comunicación aumentativa, narrativas sociales, video-modelado e intervención implementada por los padres) están reconocidas como prácticas basadas en evidencia en el informe NCAEP 2020. La app es una herramienta de apoyo y no reemplaza la terapia.

## Configuración (una sola vez)

1. Crea un proyecto en [Firebase Console](https://console.firebase.google.com).
2. **Authentication › Sign-in method**: activa **Google**.
3. **Authentication › Settings › Authorized domains**: agrega `segproject.github.io`.
4. **Firestore Database**: créala (modo producción) y en la pestaña **Reglas** pega el contenido de `firestore.rules` y publica.
5. **Configuración del proyecto › Tus apps**: registra una app web y copia su `firebaseConfig` en `firebase-config.js`.
6. Sube los cambios a GitHub.

Las fotos y audios se guardan en Firestore dentro de la cuenta de Google con la que se inicia sesión; no se suben a este repositorio. Usa la misma cuenta en todos los dispositivos para ver los mismos datos.

## Instalar en la tablet o el celular

Abre `https://segproject.github.io/<nombre-del-repo>/`, inicia sesión y usa **Agregar a pantalla de inicio** en el menú del navegador. Se abrirá como una app, a pantalla completa.

## Desarrollo

Es un solo archivo (`index.html`) sin compilación. Para probarlo localmente: `python3 -m http.server` y abre `http://localhost:8000` (agrega `localhost` a los dominios autorizados de Firebase si quieres iniciar sesión).
