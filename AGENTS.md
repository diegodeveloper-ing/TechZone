# AGENTS.md — TechZone

Sitio web estático para una tienda de tecnología en Chía, Cundinamarca, Colombia. HTML5/CSS3/ES6+ puro — sin herramientas de build, sin package manager, sin bundler, sin framework. Todo el contenido en español.

## Inicio rápido

No hay paso de instalación. Sirve desde la raíz del repositorio:

```bash
python3 -m http.server 8000
# luego abre http://localhost:8000/pages/index.html
```

Las páginas están en `pages/`, el CSS en `css/style.css`, el JS en `js/Recolector.js`.

## Bugs conocidos (NO reintroducir)

Están documentados en el README y se están rastreando activamente. Cualquier agente que edite estos archivos debe tenerlos en cuenta:

1. **Referencia JS con case-sensitive** — `index.html:77` carga `js/recolector.js` (minúscula) pero el archivo real es `js/Recolector.js` (R mayúscula). Falla en Linux/sistemas de archivos case-sensitive. Corrección trackeada en el roadmap.
2. **Rutas de imagen rotas en `productos.html`** — Líneas 61, 84, 107 usan `IMG/Productos/...` (relativo, sin `/` inicial, case incorrecto). Debería ser `/img/productos/...`. Las imágenes no cargan en un servidor.
3. **Script faltante en `contacto.html`** — Línea 60 referencia `JS/buscador.js` que no existe en ningún lado del repositorio.
4. **Markup inconsistente del logo** — `productos.html` usa el texto `⚡ TechZone` para el logo mientras que otras páginas usan `<img>` con el archivo de logo real.

## Convenciones de código

- **Indentación**: 2 espacios (HTML, CSS, JS)
- **Colores CSS** (de `style.css` y `CONTRIBUTING.md`):
  - Azul primario: `#007bff`
  - Dorado: `#cfbc64`
  - Verde precio: `#00ff88`
  - Morado: `#7222ce`
  - Texto: `#e4e4e4`
- **JS**: Solo `const`/`let`, nunca `var`. Features de ES6+ permitidas.
- **Imágenes**: Formato WebP preferido. Todos los assets en `img/`.
- **Commits**: Conventional commits (`feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`). Sin atribución de IA.
- **Ramas**: Prefijos `feature/`, `fix/`, `docs/`, `refactor/`. Nunca hacer commit directo a `main`.

## Patrones de estilo

- Glassmorphism: navbar y secciones usan `backdrop-filter: blur()` con fondos semitransparentes `rgba()`
- Navbar sticky con `position: sticky; z-index: 1000`
- Tarjetas de productos usan CSS Grid (`.contenedor-productos`)
- Breakpoints responsive: móvil 320px+, tablet 768px+, escritorio 1020px+
- Fuente: Poppins (400, 600, 700) vía Google Fonts

## Estructura de archivos

```
pages/          ← Todas las páginas HTML (puntos de entrada)
css/style.css   ← Hoja de estilos única, ~830 líneas
js/Recolector.js ← Manejador del formulario (¡nombre case-sensitive!)
img/            ← Logo, wallpaper, imágenes de productos (WebP), iconos de redes
```

## Contexto del roadmap

El README lista ~15 ítems pendientes. Antes de trabajar en este repositorio, revisar las secciones "Roadmap / Mejoras Pendientes" y "Problemas Conocidos" del README — son la fuente de verdad sobre qué necesita arreglo.
