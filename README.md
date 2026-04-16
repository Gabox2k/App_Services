# ServiAsunción 🇵🇾

> La app para encontrar al proveedor de servicios **menos malo** de Asunción.

## Demo

Abrí `index.html` en tu navegador — no requiere servidor.

---

## Páginas

| Archivo | Descripción |
|---|---|
| `index.html` | Inicio: hero, categorías, top proveedores, testimonios |
| `proveedores.html` | Listado completo con filtros, búsqueda, modal y formulario de alta |
| `como-funciona.html` | Guía paso a paso, consejos, FAQ, sección de confianza |

---

## Setup local

```bash
# Opción 1: Abrir directamente
open index.html

# Opción 2: Servidor local simple (Python)
python3 -m http.server 8080
# → http://localhost:8080

# Opción 3: Live Server (VS Code)
# Instalar extensión "Live Server" → clic derecho en index.html → "Open with Live Server"
```

No hay dependencias npm ni build steps. Todo es HTML + CSS + JS vanilla.

---

## Despliegue

### Netlify (recomendado)
1. Esta subido en github pages: https://gabox2k.github.io/App_Services/
2. O conectá tu repo de GitHub → "New site from Git"
3. Build command: *(vacío)* · Publish directory: `.` (raíz)

### GitHub Pages
```bash
git init && git add . && git commit -m "init"
git remote add origin https://github.com/TU_USUARIO/serviasuncion.git
git push -u origin main
# En GitHub → Settings → Pages → Branch: main → / (root) → Save
```

### Vercel
```bash
npx vercel --prod
```

---

## Funcionalidades implementadas

- ✅ Búsqueda por nombre, categoría y descripción
- ✅ Filtros por categoría, calificación mínima y zona
- ✅ Modal de perfil con reseñas
- ✅ Sistema de calificación desde el modal (★★★★★)
- ✅ Formulario para agregar nuevo proveedor (se suma al listado en tiempo real)
- ✅ Botón de llamada directa (`tel:`)
- ✅ Navegación responsive + menú hamburguesa
- ✅ 3 páginas completas

---

## Estructura

```
serviasuncion/
├── index.html          ← Página de inicio
├── proveedores.html    ← Listado de proveedores
├── como-funciona.html  ← Guía + FAQ
├── README.md
└── CHANGELOG.md
```

---

## Tecnologías

- HTML5 semántico
- CSS3 nativo (variables, grid, flexbox, animaciones)
- JavaScript vanilla (sin frameworks)
- Google Fonts: Syne + DM Sans

---

## 🚀 Optimización de rendimiento (Lighthouse)

Se realizaron mejoras para optimizar **Core Web Vitals** y accesibilidad detectadas por Lighthouse.

### 1️⃣ Eliminación de solicitudes que bloquean renderizado

Se optimizó la carga de **Google Fonts** para evitar que bloqueen el renderizado inicial de la página.

Antes las fuentes se cargaban de forma normal, lo que retrasaba el **LCP (Largest Contentful Paint)**.

Ahora se utilizan:

- `preconnect` para abrir conexión anticipada con Google Fonts
- `display=swap` para evitar saltos de diseño (CLS)

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet">


### Mejora la accesibiliada con main

Se agregó un punto de referencia principal (<main>) para mejorar la navegación de lectores de pantalla.

Esto permite que herramientas de accesibilidad identifiquen el contenido principal de la página.
