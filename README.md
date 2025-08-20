# Muro Interactivo (estilo Facebook)

Sistema web con React + Firebase que permite:
1) Ver todas las publicaciones (público, sin login)
2) Crear cuenta: guarda usuario, clave (auth), nombre, apellido
3) Iniciar sesión
4) Publicar posts (solo autenticados)

## Tecnologías
- React + Vite
- Tailwind CSS
- Firebase Auth (Email/Password) + Firestore

## Configuración rápida
1. **Clona** el proyecto y entra a la carpeta.
2. Copia `.env.example` a `.env` y completa con las credenciales de tu proyecto Firebase.
3. En Firebase Console, habilita **Authentication (Email/Password)** y **Firestore**.
4. Sube `firestore.rules` a Firestore (Rules) y publica.
5. Instala dependencias y ejecuta:

```bash
npm install
npm run dev
```

Abre http://localhost:5173

## Campos de usuario
- usuario (username)
- nombre
- apellido
- clave: se maneja por Firebase Authentication (no se guarda como texto plano)

## Notas de diseño
- Navbar azul tipo Facebook (`#1877F2`).
- Feed centrado, cards con bordes redondeados y sombra.
- Composer de post arriba cuando el usuario está autenticado.

## Estructura
```
src/
  components/
    AuthModal.jsx
    Navbar.jsx
    Post.jsx
    PostComposer.jsx
    PostList.jsx
  services/
    posts.js
  firebase.js
  App.jsx
  main.jsx
  index.css
```

## Producción
```bash
npm run build
npm run preview
```

## Licencia
MIT
