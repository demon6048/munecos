# Los Muñecos de la Cumbia — Web y panel

- `public/index.html`: sitio público y panel (`#/admin/login`).
- `public/firebase-config.js`: configuración de la app web de Firebase (proyecto `munecoscumbia`).
- `firestore.rules`: el público solo crea cotizaciones; todo lo demás exige administrador.

## Publicar
    npm install -g firebase-tools
    firebase login
    firebase deploy --only hosting,firestore:rules

## Primer administrador
1. Firebase > Authentication > Método de acceso > activar Correo/contraseña.
2. Authentication > Usuarios > Agregar usuario.
3. Firestore > crear la colección `admins` con un documento cuyo ID sea el UID de ese usuario.
