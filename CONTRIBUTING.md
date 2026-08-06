# Guía de Contribución - TechZone

¡Bienvenido! Si estás leyendo esto, es porque quieres ser parte del equipo TechZone. Aquí encontrarás todo lo que necesitas para empezar a contribuir.

---

## Requisitos Previos

- Conocimientos básicos de **HTML5**, **CSS3** y **JavaScript**
- Git instalado en tu máquina
- Un navegador web moderno para pruebas
- Un editor de código (VS Code recomendado)

---

## Primeros Pasos

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/01-TechZone.git
cd 01-TechZone
```

### 2. Crear una rama para tu tarea

```bash
git checkout -b feature/nombre-de-la-tarea
```

**Convención de ramas:**
- `feature/` → Nuevas funcionalidades
- `fix/` → Corrección de bugs
- `docs/` → Documentación
- `refactor/` → Mejora de código existente

### 3. Hacer tus cambios

- Edita los archivos necesarios
- Prueba en múltiples navegadores
- Verifica que sea responsive (mobile, tablet, desktop)

### 4. Commitear tus cambios

```bash
git add .
git commit -m "feat: descripción breve del cambio"
```

**Formato de commits:**
- `feat:` → Nueva funcionalidad
- `fix:` → Corrección de bug
- `docs:` → Documentación
- `style:` → Cambios de estilo (CSS)
- `refactor:` → Refactorización de código
- `test:` → Agregar o modificar tests

### 5. Push y Pull Request

```bash
git push origin feature/nombre-de-la-tarea
```

Luego crea un Pull Request en GitHub describiendo:
- Qué hiciste
- Por qué lo hiciste
- Cómo probarlo

---

## Convenciones de Código

### HTML

- Usar semántica HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- Todos los atributos `alt` en imágenes deben ser descriptivos
- Mantener indentación de 2 espacios

```html
<!-- Correcto -->
<section class="hero">
  <h1>Título</h1>
</section>

<!-- Incorrecto -->
<div class="hero">
  <font size="5">Título</font>
</div>
```

### CSS

- Seguir la metodología existente en `style.css`
- Usar clases descriptivas (BEM opcional pero recomendado)
- Mantener consistencia con los colores existentes:
  - Azul primario: `#007bff`
  - Dorado: `#cfbc64`
  - Verde precio: `#00ff88`
  - Morado: `#7222ce`
  - Texto: `#e4e4e4`
- Agregar comentarios para secciones nuevas

### JavaScript

- Usar `const` y `let` (nunca `var`)
- Mantener código modular y reutilizable
- Agregar comentarios en funciones complejas
- Manejar errores con `try/catch` cuando sea necesario

```javascript
// Correcto
const form = document.querySelector(".buscador form");

// Incorrecto
var form = document.querySelector(".buscador form");
```

---

## Estructura de Archivos

```
01-TechZone/
├── css/
│   └── style.css              # Estilos principales
├── img/
│   ├── Logo_empresa.webp      # Logo
│   ├── WALLPAPER.webp         # Fondo
│   ├── productos/             # Imágenes de productos
│   └── redes_sociales/        # Iconos de redes
├── js/
│   └── Recolector.js          # Lógica JavaScript
├── pages/
│   ├── index.html             # Inicio
│   ├── productos.html         # Catálogo
│   ├── nosotros.html          # Nosotros
│   └── contacto.html          # Contacto
└── README.md
```

---

## Reglas Importantes

1. **Nunca hacer commit directamente a `main`** — Siempre crear una rama
2. **Probar en diferentes navegadores** — Chrome, Firefox, Edge
3. **Verificar responsive** — Mobile (320px+), Tablet (768px+), Desktop (1024px+)
4. **No romper la funcionalidad existente** — Si algo se modifica, verificar que todo siga funcionando
5. **Documentar cambios significativos** — Actualizar README si es necesario
6. **Usar formato WebP para imágenes** — Mantener optimización
7. **Respetar la paleta de colores** — No agregar colores sin consultar

---

## Tareas Pendientes (Good First Issues)

Si quieres empezar con algo sencillo, estas son algunas tareas pendientes:

- [ ] Corregir ruta de imagen en `productos.html` (agregar `/` inicial)
- [ ] Agregar footer a `contacto.html`
- [ ] Agregar navegación completa en todas las páginas
- [ ] Actualizar copyright a 2026
- [ ] Corregir nombre de archivo `Recolector.js` a `recolector.js`

---

## Preguntas

Si tienes alguna duda, pregúntale al equipo. Estamos aquí para ayudarte.

¡Bienvenido al equipo TechZone!
