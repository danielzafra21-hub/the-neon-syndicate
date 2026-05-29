# CONTEXTO DEL PROYECTO — The Neon Syndicate V2

## 📁 Estructura de Carpetas

```
Desktop/
├── Prueba/
│   ├── WEB/                    # V1 original (oscura, lujo)
│   ├── WEB-V2/                 # Backup V2 (versión anterior guardada)
│   └── opencode.jsonc
│
└── Prueba 2/                   # 🎯 NUEVA VERSIÓN ACTIVA (Technically Stable style)
    ├── package.json
    ├── astro.config.mjs
    ├── tsconfig.json
    ├── postcss.config.mjs
    ├── node_modules/
    ├── public/
    │   ├── images/
    │   │   ├── productos/       # Imágenes copiadas de WEB/
    │   │   └── hero-bg-new.png
    │   └── svg/                 # SVGs decorativos
    │       ├── stairs.svg
    │       ├── door.svg
    │       ├── coin.svg
    │       ├── sparkle.svg
    │       ├── arrow.svg
    │       ├── banner-wave.svg
    │       └── logo-neon-syndicate-v2.svg
    ├── src/
    │   ├── data/
    │   │   ├── categorias.json   # Copiado de WEB/
    │   │   └── productos.json    # Copiado de WEB/
    │   ├── styles/
    │   │   └── global.css        # Design system Technically Stable
    │   ├── layouts/
    │   │   └── LayoutV2.astro    # SEO + Google Fonts + scroll reveal
    │   ├── components/
    │   │   ├── HeroSlider.astro  # 🆕 Hero con 4 slides automáticos
    │   │   ├── Header.astro      # Navbar sticky + menú mobile
    │   │   ├── Footer.astro      # Footer oscuro + newsletter
    │   │   ├── FloatingWhatsApp.astro
    │   │   ├── CategoryGrid.astro
    │   │   ├── CollectionSection.astro
    │   │   ├── ProductCard.astro
    │   │   ├── ProductGrid.astro
    │   │   ├── PriceDisplay.astro
    │   │   ├── SizeSelector.astro
    │   │   ├── Breadcrumb.astro
    │   │   ├── TestimonialCarousel.astro
    │   │   ├── NewsletterBanner.astro
    │   │   ├── CTASection.astro
    │   │   └── ui/
    │   │       ├── Badge.astro
    │   │       ├── Button.astro
    │   │       └── Tag.astro
    │   └── pages/
    │       ├── index.astro
    │       ├── catalogo.astro
    │       ├── contacto.astro
    │       ├── categoria/
    │       │   └── [slug].astro
    │       ├── producto/
    │       │   └── [slug].astro
    │       └── legal/
    │           ├── privacidad.astro
    │           ├── terminos.astro
    │           └── cookies.astro
    └── dist/                    # Build output (36 páginas)
```

## 🎨 Design System (global.css)
- **Colores Technically Stable**: rosa #ff2d78, cian #00d4ff, púrpura #7c3aed, amarillo #ffd600, naranja #ff6d00, verde #00e676
- **Tipografía**: DM Sans (headings) + Inter (body)
- **Fondo**: blanco cálido #f7f5f0
- **Clases globales**: .reveal, .gradient-text, .gradient-text-alt, .btn-primary, .btn-ghost, .hero-slider, .product-card

## 🆕 HeroSlider
- 4 slides con auto-play (5.5s cada uno)
- Slide 1: THE NEON SYNDICATE (rosa→púrpura→cian)
- Slide 2: MILITAR ART (azul marino→cian)
- Slide 3: ICON ART (púrpura→rosa→naranja)
- Slide 4: SET UPS (naranja→rosa→púrpura)
- Dots navegables + swipe táctil + barra de progreso

## 🛠 Stack
- Astro v6.4.0
- Tailwind CSS v4.3.0 (PostCSS)
- @tailwindcss/postcss
- sharp (para imágenes)

## 🔧 Fixes Aplicados
1. Títulos HeroSlider: usando `class:list` y CSS nativo en `<style>` (evita `{slide.accent}` literal)
2. SizeSelector: usa `define:vars={{ productName }}` para pasar datos al script cliente
3. PriceDisplay se actualiza al seleccionar tamaño (innerHTML + gradient-text-alt)
4. WhatsApp link se actualiza con talla seleccionada

## 📦 Build
- `npm run build` → 36 páginas, 0 errores
- `npm run dev` → servidor en localhost:4323

## 📝 Historial de Cambios
- 25/05/2026: Plan de implementación creado
- 28/05/2026: WEB-V2 creada con estructura base
- 29/05/2026: Prueba 2 creada con HeroSlider y colores TS
- 29/05/2026: Fixes de renderizado (class:list, define:vars)
