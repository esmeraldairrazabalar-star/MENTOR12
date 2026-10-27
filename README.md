# 🎓 MentorApp · Plataforma de Mentorías Académicas y Profesionales

**MentorApp** es una plataforma web moderna para conectar estudiantes con mentores verificados, permitiendo agendar mentorías, comunicarse por chat en tiempo real, coordinar clases por Google Meet y gestionar la comunidad mediante un panel de administración completo.

---

## 👑 Acceso de Administrador

Para ingresar al panel completo de administración (**Dashboard**, **Estudiantes**, **Mentores**, **Mentorías**, **Solicitudes**, **Conexiones**, **Control del sitio**):

### Opción 1: Correo y Contraseña
* **Nombre de Administradora:** `Esmeralda Irrazabal`
* **Correo:** `admin@mentorapp.com`
* **Contraseña:** `AdminMentorApp2026!`

### Opción 2: Iniciar con Google
* Puedes pulsar el botón **"Entrar con Google"** e iniciar sesión con tu cuenta de Google (`esmeraldairrazabalar@gmail.com`). El sistema te otorgará acceso como Administradora de forma automática.

---

## 💻 Cómo ejecutar el proyecto en Visual Studio Code

Debido a que Firebase y la autenticación de Google requieren un protocolo HTTP seguro para funcionar, el proyecto debe ejecutarse mediante un servidor local (no abrir con doble clic directo `file://`).

### Método A: Extensión Live Server de VS Code (Recomendado)
1. Abre la carpeta del proyecto en **Visual Studio Code**.
2. Instala la extensión **Live Server** (si aún no la tienes).
3. Haz clic derecho sobre el archivo `index.html` y selecciona **Open with Live Server**.
4. Se abrirá automáticamente en tu navegador (`http://localhost:5500`).

### Método B: Servidor Node integrado (Sin dependencias)
1. Abre la terminal en Visual Studio Code (`Ctrl + ñ` o `Terminal > New Terminal`).
2. Ejecuta:
   ```bash
   node server.js
   ```
3. Abre en tu navegador:
   ```
   http://localhost:3000
   ```

---

## 🚀 Guía paso a paso para subir el proyecto a GitHub (https://github.com/)

Sigue estos sencillos pasos desde la terminal de Visual Studio Code:

### 1. Inicializar Git y preparar los archivos
En la terminal integrada de VS Code en la carpeta del proyecto, ejecuta:
```bash
git init
git add .
git commit -m "Versión lista para producción de MentorApp"
```

### 2. Crear el repositorio en GitHub
1. Inicia sesión en tu cuenta de [GitHub](https://github.com/).
2. Haz clic en el botón verde **New** o entra a [https://github.com/new](https://github.com/new).
3. Ponle un nombre al repositorio (ejemplo: `mentorapp` o `Mentoria`).
4. Deja el repositorio en **Public** (para usar GitHub Pages gratis).
5. No marques las opciones de "Add a README file" ni ".gitignore" (ya los tenemos en la carpeta).
6. Haz clic en **Create repository**.

### 3. Vincular y subir tu código
Copia y ejecuta los siguientes comandos en tu terminal de VS Code (reemplaza `TU_USUARIO` y `TU_REPOSITORIO` por los tuyos):

```bash
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPOSITORIO.git
git push -u origin main
```

---

## 🌐 Cómo publicar tu web gratis en GitHub Pages

1. En tu repositorio de GitHub, haz clic en la pestaña **Settings** (Configuración).
2. En el menú lateral izquierdo, haz clic en **Pages**.
3. En la sección **Build and deployment**:
   * **Source:** Selecciona `Deploy from a branch`.
   * **Branch:** Selecciona `main` y en la carpeta elige `/(root)`.
4. Haz clic en **Save** (Guardar).
5. Espera unos 1 a 2 minutos. Al recargar la página verás el enlace público de tu web:
   ```
   https://TU_USUARIO.github.io/TU_REPOSITORIO/
   ```

---

## ⚙️ Configuración en Firebase (Importante al publicar)

Para que el inicio de sesión con Google y la base de datos funcionen en GitHub Pages:

### 1. Autorizar el dominio en Firebase Authentication
1. Entra a tu [Consola de Firebase](https://console.firebase.google.com/) y abre tu proyecto `mentorias-f8387`.
2. Ve a **Authentication** > pestaña **Settings** (Configuración) > **Authorized domains** (Dominios autorizados).
3. Haz clic en **Add domain** (Agregar dominio) y agrega:
   * `localhost` (ya viene por defecto)
   * `TU_USUARIO.github.io` (tu dominio de GitHub Pages)

### 2. Publicar las reglas de Firestore Database
1. En Firebase, ve a **Firestore Database** > pestaña **Rules** (Reglas).
2. Pega el contenido exacto del archivo `firestore.rules`.
3. Haz clic en **Publicar** (Publish).

---

## 📁 Estructura del Proyecto

```
Mentoria/
│── index.html           # Página principal y estructura de la app
│── app.js               # Lógica de la aplicación, vistas, componentes y Firebase Auth/Firestore
│── styles.css           # Estilos modernos, diseño responsive, temas y animaciones
│── firebase-config.js   # Credenciales de conexión a Firebase y correos de administradores
│── firestore.rules      # Reglas de seguridad para Firestore Database
│── server.js            # Servidor local Node.js sin dependencias para VS Code
│── .nojekyll            # Archivo para compatibilidad con GitHub Pages
│── README.md            # Guía completa de uso, credenciales y despliegue
└── avatars/             # Fotos de perfil predeterminadas
```

---

## 👩‍💼 Créditos
Desarrollado y administrado por **Esmeralda Irrazabal** · MentorApp 2026.
