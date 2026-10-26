# Project Exodus - Legal Web (Privacy Policy & EULA)

Este repositorio contiene la página web estática oficial de la **Política de Privacidad** y el **Acuerdo de Licencia de Usuario Final (EULA)** para *Project Exodus* (AstroxStudio).

Está optimizada con:
- **Diseño profesional oscuro** adaptado a la estética del videojuego.
- **Soporte multilingüe instantáneo** con selector (Inglés por defecto, Español incluido).
- **Pestañas navegables con soporte de anclas (Hash URLs)** para poner enlaces separados en Steamworks:
  - `https://<tu-usuario>.github.io/<tu-repo>/#privacy`
  - `https://<tu-usuario>.github.io/<tu-repo>/#eula`
- **Cero dependencias:** No requiere Node.js, React ni compilación. Carga instantáneamente y es 100% compatible con **GitHub Pages**.

---

## 🚀 Cómo publicarlo gratis en GitHub Pages (Paso a paso)

### Paso 1: Crear un nuevo repositorio en GitHub
1. Entra en tu cuenta de [GitHub](https://github.com/) y pulsa en **New repository**.
2. Dale un nombre (por ejemplo: `project-exodus-legal` o `privacy-policy`).
3. Elige que sea **Público** (Public) y pulsa en **Create repository**.

### Paso 2: Subir los archivos
Puedes subir los archivos mediante Git por consola o directamente arrastrando el archivo `index.html` en la web de GitHub:

**Vía terminal (Git):**
```bash
cd ProjectM-Legal-Web
git init
git add index.html README.md
git commit -m "Initial commit: Privacy Policy and EULA"
git branch -M main
git remote add origin https://github.com/<TU_USUARIO>/<TU_REPOSITORIO>.git
git push -u origin main
```

*(O en la web de GitHub pulsa en "Uploading an existing file", arrastra `index.html` y haz commit).*

### Paso 3: Activar GitHub Pages
1. En tu repositorio de GitHub, haz clic en la pestaña **Settings** (arriba a la derecha).
2. En la barra lateral izquierda, pulsa en **Pages**.
3. En **Build and deployment > Branch**:
   - Selecciona la rama: **`main`**.
   - Carpeta: **`/ (root)`**.
   - Pulsa en **Save**.
4. En 30 segundos, GitHub te dará tu URL pública con HTTPS gratis:
   `https://<TU_USUARIO>.github.io/<TU_REPOSITORIO>/`

---

## 🎮 Enlaces para Steamworks

Una vez publicado en GitHub Pages, pon estos dos enlaces exactos en tu panel de **Steamworks** (*Edit Store Page > Basic Info*):

1. **Privacy Policy URL:**
   ```text
   https://<TU_USUARIO>.github.io/<TU_REPOSITORIO>/#privacy
   ```
2. **EULA URL:**
   ```text
   https://<TU_USUARIO>.github.io/<TU_REPOSITORIO>/#eula
   ```

*Nota: También puedes forzar el idioma en la URL si lo deseas:*
- `https://<TU_USUARIO>.github.io/<TU_REPOSITORIO>/?lang=en#privacy` (Inglés)
- `https://<TU_USUARIO>.github.io/<TU_REPOSITORIO>/?lang=es#privacy` (Español)

---

## 🌐 Cómo añadir más idiomas en el futuro (ej. Francés, Alemán, Chino)
En el archivo `index.html`:
1. En el encabezado (`.lang-switch`), añade un nuevo botón con el código del idioma:
   ```html
   <button class="lang-btn" data-lang="de">DE</button>
   ```
2. Dentro de cada sección (`#privacy` y `#eula`), añade un bloque con la clase correspondiente:
   ```html
   <div class="lang-content lang-de" style="display: none;">
       <!-- Texto traducido -->
   </div>
   ```
3. En el script de abajo, añade los textos clave en el objeto `i18n.de`.
