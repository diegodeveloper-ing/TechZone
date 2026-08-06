# TechZone

> Potencia tu mundo digital — Tu tienda de tecnología de alto rendimiento

TechZone es una plataforma web estática diseñada para una tienda de tecnología ubicada en Chía, Cundinamarca, Colombia. Ofrece un catálogo de productos, configuraciones personalizadas por presupuesto y uso, y un canal directo de contacto para cotizaciones.

---

## Características

- **Diseño responsive** adaptable a dispositivos móviles, tablets y escritorio
- **Efectos visuales modernos** con glassmorphism, transiciones suaves y hover effects
- **Formulario de configuración** para personalizar equipos según presupuesto, uso y extras
- **Catálogo de productos** con especificaciones detalladas y precios
- **Sección "Nosotros"** completa con historia, equipo, misión, visión, objetivos y servicios
- **Redes sociales** integradas (Facebook, Instagram, YouTube)
- **Navegación sticky** con efecto blur y sombra
- **Imágenes optimizadas** en formato WebP para mejor rendimiento

---

## Tecnologías Utilizadas

| Categoría | Tecnología | Descripción |
|-----------|------------|-------------|
| **Estructura** | HTML5 | Semántica y accesibilidad web |
| **Estilos** | CSS3 | Personalización visual avanzada |
| **Layout** | CSS Grid | Sistema de cuadrícula para catálogo y tarjetas |
| **Layout** | Flexbox | Alineación flexible en navegación y formularios |
| **Efectos** | Backdrop-filter | Efecto glassmorphism en navbar y secciones |
| **Animaciones** | CSS Transitions | Transiciones suaves en hover y estados interactivos |
| **Interactividad** | JavaScript ES6+ | Manejo de formularios y eventos del DOM |
| **Fuentes** | Google Fonts | Tipografía Poppins (400, 600, 700) |
| **Imágenes** | WebP | Formato optimizado para web (compresión superior a JPEG/PNG) |
| **Control de versiones** | Git | Control de versiones distribuido |
| **Repositorio** | GitHub | Alojamiento y colaboración |
| **Diseño visual** | Glassmorphism | Tendencia de UI con efecto de vidrio esmerilado |
| **Responsive** | Media Queries | Adaptación a múltiples resoluciones de pantalla |

---

## Estructura del Proyecto

```
01-TechZone/
├── css/
│   └── style.css              # Estilos principales del proyecto
├── img/
│   ├── Logo_empresa.webp      # Logo de TechZone
│   ├── WALLPAPER.webp         # Imagen de fondo
│   ├── productos/             # Imágenes de productos del catálogo
│   │   ├── NVIDIA_GeForce_RTX_4070_Ti_12GB_GDDR6X.webp
│   │   ├── Procesador_Intel_Core_i7_13700F_2.1GHz__13ª_Generación.webp
│   │   └── Corsair_Vengeance_RGB_32GB__2x16GB__DDR5_6000MHz.webp
│   └── redes_sociales/        # Iconos de redes sociales
│       ├── facebook.webp
│       ├── Instagram.webp
│       ├── X.webp
│       └── youtube.webp
├── js/
│   └── Recolector.js          # Lógica del formulario de configuración
├── pages/
│   ├── index.html             # Página principal
│   ├── productos.html         # Catálogo de productos
│   ├── nosotros.html          # Información de la empresa
│   └── contacto.html          # Redes sociales y contacto
└── README.md                  # Este archivo
```

---

## Instalación y Configuración

### Prerrequisitos

- Un navegador web moderno (Chrome, Firefox, Edge, Safari)
- Git instalado (opcional, para clonar el repositorio)

### Pasos

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/01-TechZone.git
   ```

2. **Navegar al directorio**
   ```bash
   cd 01-TechZone
   ```

3. **Abrir en el navegador**
   - Abrir el archivo `pages/index.html` directamente en el navegador
   - O usar un servidor local (recomendado):
     ```bash
     # Con Python
     python -m http.server 8000

     # Con Node.js (si tienes live-server instalado)
     npx live-server
     ```

4. **Acceder al sitio**
   - Abre `http://localhost:8000` en tu navegador

---

## Páginas del Sitio

| Página | Archivo | Descripción |
|--------|---------|-------------|
| **Inicio** | `pages/index.html` | Hero principal y formulario de configuración |
| **Productos** | `pages/productos.html` | Catálogo con 4 productos (SSD, CPU, GPU, RAM) |
| **Nosotros** | `pages/nosotros.html` | Historia, equipo, misión, visión, servicios y objetivos |
| **Contacto** | `pages/contacto.html` | Redes sociales (Facebook, Instagram, YouTube) |

---

## Equipo Fundador

| Miembro | Rol | Responsabilidad |
|---------|-----|-----------------|
| **Jaider Santiago Sotelo Campos** | Dirección General | Estrategia del negocio y visión empresarial |
| **Diego Alejandro López Sánchez** | Marketing Digital | Gestión de contenidos y presencia online |
| **Duván Yesid Munévar Hernández** | Operaciones | Logística y atención al cliente |
| **Andrés Eduardo Peraza Vásquez** | Gestión de Productos | Inventario, precios y proveedores |

---

## Roadmap / Mejoras Pendientes

- [ ] Corregir rutas de archivos (referencias a `IMG/Productos/` sin `/` inicial)
- [ ] Corregir nombre de archivo `Recolector.js` a `recolector.js` (compatibilidad case-sensitive)
- [ ] Agregar navegación completa entre todas las páginas
- [ ] Implementar funcionalidad real del formulario de búsqueda (mostrar resultados)
- [ ] Agregar más productos al catálogo
- [ ] Actualizar copyright a 2026
- [ ] Agregar footer a la página de contacto
- [ ] Implementar carrito de compras funcional
- [ ] Agregar página de productos individuales (detail view)
- [ ] Optimizar imágenes y implementar lazy loading
- [ ] Agregar animaciones de carga (skeleton screens)
- [ ] Implementar modo oscurecido (dark/light mode)
- [ ] Agregar formulario de contacto funcional con validación
- [ ] Integrar con backend para gestión de inventario
- [ ] Implementar sistema de autenticación de usuarios

---

## Problemas Conocidos

| # | Archivo | Problema | Severidad |
|---|---------|----------|-----------|
| 1 | `contacto.html:60` | Referencia a `JS/buscador.js` que no existe en el proyecto | Alta |
| 2 | `index.html:77` | Referencia a `js/recolector.js` (minúscula) pero el archivo es `Recolector.js` (R mayúscula) - falla en sistemas case-sensitive | Media |
| 3 | `productos.html` | Rutas de imágenes `IMG/Productos/` sin `/` inicial - no carga en servidores | Alta |
| 4 | `index.html:82` | Footer muestra "© 2025" y estamos en 2026 | Baja |
| 5 | `contacto.html` | No incluye sección de footer | Baja |
| 6 | Navegación | Solo hay enlace a "Cotiza con nosotros", sin links a otras páginas | Media |
| 7 | `Recolector.js` | El formulario solo muestra un `alert()`, no procesa ni muestra resultados reales | Media |

---

## Licencia

Este proyecto es de uso educativo. Todos los derechos reservados © 2025 TechZone.

---

## Contacto

Para cotizaciones y más información, síguenos en nuestras redes sociales o contáctanos directamente a través del formulario en la página de contacto.
