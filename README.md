# Portafolio — Luis Eduardo García Bohórquez

Sitio web personal de una sola página para presentar servicios de **Fractional FP&A**, con dashboard interactivo, modelo financiero y caso de estudio de automatización con IA.

---

## 📦 ¿Qué contiene este paquete?

| Archivo | Descripción |
|---|---|
| `index.html` | El sitio completo. HTML + CSS + JavaScript + Chart.js, todo embebido. No necesita build step. |
| `vercel.json` | Configuración de Vercel con headers de seguridad y caching. |
| `README.md` | Este archivo. |

El sitio es **100% estático** — se despliega en segundos.

---

## 🚀 Cómo publicar en Vercel

### Opción A — Drag & drop (la más rápida, 1 minuto)

1. Ve a **https://vercel.com/new**
2. Inicia sesión (puedes usar tu cuenta de Google).
3. Arrastra la carpeta completa `portfolio/` (con los 3 archivos dentro) al área "Deploy".
4. Vercel te asigna un nombre aleatorio — puedes aceptarlo o cambiarlo por algo como `luisgarcia-fpa`.
5. Click en **Deploy**.
6. En ~15 segundos obtienes una URL pública del tipo `https://luisgarcia-fpa.vercel.app`

### Opción B — Desde GitHub (recomendada para actualizaciones futuras)

1. Crea un repo nuevo en GitHub: `luisgarcia-portfolio` (público o privado da igual).
2. Sube los 3 archivos (`index.html`, `vercel.json`, `README.md`).

   ```powershell
   cd C:\ruta\a\portfolio
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/luisgarcia-portfolio.git
   git push -u origin main
   ```

3. En Vercel → **Add New → Project** → conecta GitHub → selecciona el repo.
4. Vercel detecta automáticamente que es un sitio estático. Click **Deploy**.
5. Cualquier cambio que hagas en GitHub se despliega solo.

### Opción C — Vercel CLI

```powershell
npm install -g vercel
cd C:\ruta\a\portfolio
vercel
```

Sigue los prompts. En el primer deploy te pregunta si enlazar a un proyecto existente o crear uno nuevo.

---

## 🌐 Dominio personalizado (opcional)

Si compras un dominio como `luisgarcia.co` o `legb.co`:

1. En Vercel → tu proyecto → **Settings → Domains**.
2. Agrega el dominio.
3. Vercel te da los registros DNS que debes configurar en tu proveedor (GoDaddy, Namecheap, Cloudflare, etc.).
4. El SSL se genera automáticamente.

---

## ✏️ Cómo editar el contenido

Todo está en `index.html`. No hay build step ni frameworks que configurar.

### Cambiar textos

- **Textos visibles en español/inglés**: busca el objeto `translations` cerca del final del archivo (línea ~1900 aproximadamente). Tiene dos claves: `es` y `en`. Edita el texto correspondiente.
- **Textos que no usan `data-i18n`**: edítalos directamente en el HTML.

### Cambiar el email de contacto

Busca `garciabohorquezluiseduardo@gmail.com` en el archivo (aparece 2 veces) y reemplázalo.

### Cambiar datos del dashboard (Burger Lab)

Busca `const DATA = {` en el JavaScript. Ahí están los 3 objetos: `chia`, `cajica`, `zipaquira`. Cambia los arrays de `revenue`, `tickets`, `food`, `labor`, etc. Los gráficos se actualizan solos.

### Cambiar datos del modelo financiero (CloudMetrics)

Los números están hardcodeados en las tablas HTML dentro de cada `<div class="model-view">`. Edita celda por celda.

### Cambiar colores

Al inicio del `<style>` están todas las variables CSS:

```css
--accent-blue: #00E5FF;
--accent-mint: #6EE7B7;
--bg-0: #05080F;
```

Cambia ahí y el tema completo se actualiza.

---

## 🛠️ Desarrollo local

Simplemente abre `index.html` en el navegador. No necesitas servidor.

Si prefieres un server local (para ver cambios con reload):

```powershell
# Python 3
python -m http.server 8000
# Luego abre http://localhost:8000
```

---

## 📋 Stack técnico

- **HTML5** semántico
- **CSS3** con variables, grid, flexbox, gradient mesh
- **JavaScript vanilla** (sin frameworks)
- **Chart.js 4.4.1** (vía CDN) para los gráficos del dashboard
- **Google Fonts**: Bricolage Grotesque, Manrope, JetBrains Mono
- **Diseño responsive** con breakpoints en 960px, 880px, 860px, 768px

---

## 📞 Contacto

**Luis Eduardo García Bohórquez**
garciabohorquezluiseduardo@gmail.com

---

_Built with care in Colombia · v1.0_
