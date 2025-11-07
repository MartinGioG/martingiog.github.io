# Guía Definitiva: Publicar y Actualizar tu Portafolio en GitHub

Esta guía te explica todo el proceso. Primero, cómo publicar tu sitio (Fase 1) y, segundo, las DOS formas de actualizarlo (Fase 2).

---

### 📥 Prerrequisito: Instalar Git

Si quieres usar la consola (Método Profesional), primero debes instalar Git.
* **Descarga:** Ve a [git-scm.com](https://git-scm.com/).
* **Instalación (Windows):** Durante la instalación, te recomiendo seleccionar la opción que añade **"Git Bash"**. Esta será tu consola.

---

### 🚀 FASE 1: Configuración Inicial (Solo se hace una vez)

El objetivo es crear tu repositorio en GitHub y poner tu sitio en línea por primera vez.

#### Parte A: Crear el Repositorio en GitHub

1.  **Nuevo Repositorio:** Ve a tu página de GitHub, haz clic en el ícono `+` (esquina superior derecha) y selecciona **"New repository"**.
2.  **Nombre Clave:** Nombra tu repositorio *exactamente* así:
    `tu-nombre-de-usuario.github.io`
    (En tu caso, es: **`martingiog.github.io`**)
    *Esto es muy importante para que tu enlace sea corto y funcione bien.*
3.  **Público:** Asegúrate de que sea **"Public"**.
4.  **Crear:** Haz clic en **"Create repository"**. No añadas ningún archivo (README, .gitignore, etc.) todavía.

#### Parte B: Subir tus Archivos (La forma correcta)

1.  **Prepara tus Archivos:** En tu computadora, ten lista tu carpeta de portafolio (ej. `mi-portafolio`).
2.  **Sube el Contenido:** Ve a la página de tu repositorio recién creado y haz clic en **"uploading an existing file"**.
3.  **Arrastra los Archivos:** **Abre** tu carpeta `mi-portafolio` y arrastra **todo el contenido** (`index.html`, carpeta `assets`, etc.) a la caja de subida de GitHub. **No arrastres la carpeta `mi-portafolio` en sí.**
4.  **Guarda:** Haz clic en **"Commit changes"**.

#### Parte C: Activar GitHub Pages

1.  **Settings:** En tu repositorio, ve a la pestaña **"Settings"** (Configuración).
2.  **Pages:** En el menú izquierdo, haz clic en **"Pages"** (Páginas).
3.  **Fuente (Source):** En "Build and deployment", selecciona **"Deploy from a branch"** (Desplegar desde una rama).
4.  **Configuración:** Asegúrate de que la rama sea **`main`** y la carpeta sea **`📁 / (root)`**.
5.  **Save:** Haz clic en **"Save"** (Guardar).
6.  **Espera:** Tarda 1-2 minutos. Recarga la página hasta que aparezca el recuadro verde/azul con tu enlace: `https://martingiog.github.io`

---

### ✨ FASE 2: Cómo Actualizar tu Sitio (Tu día a día)

Ahora que tu sitio está en línea, así es como subirás cambios (corregir texto, añadir imágenes, etc.). Tienes dos métodos:

#### Método A: El Fácil (Editar desde la Web de GitHub)

Ideal para cambios rápidos de texto o corregir una ruta.

1.  **Navega al Archivo:** Ve a tu repositorio en GitHub (`martingiog.github.io`).
2.  **Encuentra el Archivo:** Haz clic en el archivo que quieres cambiar (ej. `index.html`).
3.  **Edita:** Haz clic en el **ícono de lápiz ✏️** (Editar este archivo) en la esquina superior derecha.
4.  **Haz tus Cambios:** Edita el texto directamente en el navegador.
5.  **Guarda:** Ve al final de la página y haz clic en el botón verde **"Commit changes"**.
6.  **Espera:** En 1 o 2 minutos, tu sitio web se actualizará con los cambios.

*Nota: Para subir archivos nuevos (como imágenes), es mejor usar la opción "Add file" > "Upload files" en la página principal de tu repositorio.*

---

#### Método B: El Profesional (Usar la Consola de Git)

Esta es la forma más rápida y potente una vez que te acostumbras.

**Sub-Fase B1: Conectar tu PC (Solo la primera vez)**

1.  **Abre la Consola:** Abre **"Git Bash"** (o tu terminal).
2.  **Navega:** Ve a la carpeta donde guardas tus proyectos (ej. `cd Documentos/Proyectos`).
3.  **Clona:** Descarga tu repositorio a una nueva carpeta.
    ```bash
    git clone [https://github.com/MartinGioG/martingiog.github.io.git](https://github.com/MartinGioG/martingiog.github.io.git)
    ```
4.  **¡Listo!** Ahora tienes una nueva carpeta `martingiog.github.io` en tu PC. **Usa esta carpeta para todos tus cambios futuros.**

**Sub-Fase B2: Configurar tu Identidad (Solo la primera vez)**

1.  **Abre la consola EN** la nueva carpeta `martingiog.github.io` (puedes hacer clic derecho > "Git Bash Here").
2.  **Configura tu nombre:**
    ```bash
    git config --global user.name "MartinGioG"
    ```
3.  **Configura tu email:** (Usa el mismo email de tu cuenta de GitHub)
    ```bash
    git config --global user.email "tu-email-de-github@ejemplo.com"
    ```
    *(Este era el paso que te daba el error "Author identity unknown". Ya no te volverá a pasar).*

**Sub-Fase B3: El Flujo de Trabajo (Cada vez que actualices)**

1.  **Haz tus cambios:**
    * Abre la carpeta `martingiog.github.io` en tu editor de código (VS Code).
    * Modifica tu `index.html`, agrega imágenes a `assets/`, etc.
    * Guarda tus archivos.

2.  **Abre la Consola:**
    * Abre **Git Bash** *dentro* de tu carpeta `martingiog.github.io`.

3.  **Ejecuta los 3 Comandos Mágicos:**

    **A. `git add .`**
    * **Qué hace:** Prepara todos los archivos nuevos o modificados.
    ```bash
    git add .
    ```

    **B. `git commit -m "Tu mensaje"`**
    * **Qué hace:** Guarda una "foto" (commit) de tus cambios en tu PC. El mensaje (`-m`) describe lo que hiciste.
    ```bash
    # Ejemplo:
    git commit -m "Agregué nuevos proyectos y corregí enlaces"
    ```

    **C. `git push origin main`**
    * **Qué hace:** Sube todos los cambios guardados de tu PC a GitHub.
    ```bash
    git push origin main
    ```

4.  **Espera y Celebra:**
    * Espera de 1 a 3 minutos.
    * Recarga tu sitio `https://martingiog.github.io` en el navegador.
    * Tus cambios ya estarán en línea.

---

### ⚠️ Solución de Problemas Comunes

* **Las imágenes no cargan (Error 404):**
    * **Causa:** Mayúsculas y minúsculas. El servidor de GitHub (Linux) distingue entre `imagen.jpg` e `Imagen.JPG`. Tu PC (Windows/Mac) no.
    * **Solución:** Revisa el nombre exacto del archivo/carpeta en GitHub (ej. `Proyectos/foto.png`) y asegúrate de que la ruta en tu `index.html` sea *idéntica*:
        `<img src="assets/images/Proyectos/foto.png">`
    * Corrige el `index.html`, guarda, y vuelve a subir el cambio (con el Método A o B).