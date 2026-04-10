# Instituto Bilingüe República de Italia - Web Site

Web institucional multipage completa para un colegio, desarrollada con **Astro** y **Tailwind CSS**.

## 🚀 Características

✅ **Multipágina (NO SPA)** - 6 páginas separadas con rutas independientes
✅ **Diseño Responsivo** - Mobile-first, adaptable a cualquier pantalla
✅ **Colores Institucionales** - Rojo, Verde, Blanco y Celeste (Italia & Argentina)
✅ **Componentes Reutilizables** - Navbar, Footer, Card, Hero, NewsCard
✅ **Animaciones Suaves** - Fade-in en scroll, hover effects
✅ **SEO Optimizado** - Meta tags y estructura semántica
✅ **Navegación Sticky** - Navbar fijo en pantalla
✅ **Formulario de Contacto** - Integración con Formspree

## 📁 Estructura del Proyecto

```
.
├── src/
│   ├── components/
│   │   ├── Navbar.astro       # Navegación principal
│   │   ├── Footer.astro       # Pie de página
│   │   ├── Hero.astro         # Sección hero
│   │   ├── Card.astro         # Tarjeta genérica
│   │   └── NewsCard.astro     # Tarjeta de noticias
│   ├── layouts/
│   │   └── Layout.astro       # Layout base con head global
│   ├── pages/
│   │   ├── index.astro        # Página de inicio
│   │   ├── institucional.astro # Información institucional
│   │   ├── oferta-educativa.astro # Descripción de niveles
│   │   ├── noticias.astro     # Listado de noticias
│   │   ├── galeria.astro      # Galería de fotos
│   │   └── contacto.astro     # Formulario de contacto
│   └── styles/
│       └── global.css         # Estilos globales
├── astro.config.mjs           # Configuración de Astro
├── tailwind.config.mjs        # Configuración de Tailwind
├── package.json               # Dependencias
└── README.md                  # Este archivo
```

## 📄 Páginas

| Página | URL | Descripción |
|--------|-----|-------------|
| **Inicio** | `/` | Hero, presentación, niveles, noticias destacadas, CTA |
| **Institucional** | `/institucional` | Historia, valores, proyecto educativo, infraestructura |
| **Oferta Educativa** | `/oferta-educativa` | Detalles de Inicial, Primario, Secundario y servicios |
| **Noticias** | `/noticias` | Listado completo de noticias en cards |
| **Galería** | `/galeria` | Galería con filtros por categoría |
| **Contacto** | `/contacto` | Formulario, información, mapa, WhatsApp |

## 🎨 Colores

```css
--color-rojo: #CE2B37
--color-verde: #009246
--color-blanco: #FFFFFF
--color-celeste: #0066CC
```

## 🛠️ Instalación

### Requisitos
- Node.js 16+
- npm o yarn

### Pasos

1. **Clonar/descargar el proyecto**
```bash
cd landingbili
```

2. **Instalar dependencias**
```bash
npm install
```

3. **Iniciar servidor de desarrollo**
```bash
npm run dev
```
Accede a `http://localhost:3000`

4. **Compilar para producción**
```bash
npm run build
```

5. **Vista previa de compilación**
```bash
npm run preview
```

## ⚙️ Configuración Personalizada

### Cambiar datos de contacto
Edita `/src/components/Footer.astro` y `/src/pages/contacto.astro`:
- Email
- Teléfono
- Dirección
- WhatsApp
- Redes sociales

### Integrar formulario de contacto
El formulario usa **Formspree**:

1. Ve a [formspree.io](https://formspree.io)
2. Crea una cuenta y nuevo formulario
3. Obtén tu Form ID
4. En `/src/pages/contacto.astro`, reemplaza `YOUR_FORM_ID` en:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Cambiar imágenes
Se usan placeholders de Unsplash. Para usar tus propias imágenes:
```astro
<img src="tu-ruta-de-imagen.jpg" alt="Descripción" />
```

### Personalizar contenido
Todos los textos pueden editarse directamente en los archivos `.astro`

## 🎯 Variables Tailwind

Se agregaron colores personalizados en `tailwind.config.mjs`:
```javascript
colors: {
  italia: {
    rojo: '#CE2B37',
    verde: '#009246',
    blanco: '#FFFFFF',
    celeste: '#0066CC',
  }
}
```

Úsalos: `bg-italia-rojo`, `text-italia-verde`, etc.

## 📱 Responsive

Breakpoints utilizados:
- `md:` (768px) - Tablet/Desktop
- `lg:` (1024px) - Desktop completo
- Mobile-first por defecto

## ✨ Funcionalidades JavaScript

### Navbar Mobile
- Menú hamburguesa funcional
- Cierra al hacer click en un enlace

### Galería con Filtros
- Filtra por categoría
- Animación de transición

### Scroll Animations
- Fade-in automático al hacer scroll
- Usa Intersection Observer API

### Hover Effects
- Escala en imágenes
- Cambio de color en botones y links

## 🔍 SEO

Cada página tiene:
- `<title>` único
- `<meta description>`
- `<meta keywords>`
- Estructura semántica HTML
- Open Graph ready (opcional)

## 🚀 Deployment

### Netlify
```bash
npm run build
# Sube la carpeta 'dist/' a Netlify
```

### Vercel
```bash
npm run build
# Conecta tu repositorio Git
```

### GitHub Pages
```bash
npm run build
# Sube 'dist/' al branch gh-pages
```

## 📝 Personalización Adicional

### Agregar página nueva
1. Crea archivo en `/src/pages/mi-pagina.astro`
2. Importa componentes necesarios
3. Agrega link en `/src/components/Navbar.astro`
4. La ruta se genera automáticamente

### Agregar componente
1. Crea en `/src/components/MiComponente.astro`
2. Importa en las páginas donde lo necesites

### Editar estilos globales
```css
/* src/styles/global.css */
```

## 📚 Recursos

- [Documentación Astro](https://docs.astro.build)
- [Tailwind CSS](https://tailwindcss.com)
- [Formspree](https://formspree.io)

## 📄 Licencia

Este proyecto es de uso exclusivo del Instituto Bilingüe República de Italia.

---

**Desarrollado con ❤️ para educación de calidad**
