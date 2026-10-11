# Los Muñecos de la Cumbia — Web y panel

Sitio público de la orquesta con formulario de cotización, y panel de administración de demostración (datos ficticios).

## Estructura
- `public/index.html` — la página completa (HTML, CSS y JS en un solo archivo).
- `public/firebase-config.js` — configuración de la app web de Firebase (pegar aquí).
- `firestore.rules` — reglas de seguridad de la base de datos.
- `firebase.json` — configuración de Firebase Hosting y Firestore.

## Probar en local
Abrir la carpeta en VS Code y usar la extensión Live Server sobre `public/index.html`.

## Publicar
```
npm install -g firebase-tools
firebase login
firebase use --add
firebase deploy --only hosting,firestore:rules
```

## Estado
- Las cotizaciones del formulario público se guardan en Firestore (`oportunidades`) cuando `firebase-config.js` está configurado.
- El panel de administración es una demostración: no lee de Firebase y no tiene autenticación real.
- Nunca subir archivos de cuentas de servicio (`serviceAccount*.json`) ni `.env`.
