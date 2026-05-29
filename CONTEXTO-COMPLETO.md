# ============================================
# CONTEXTO COMPLETO — The Neon Syndicate V2
# ============================================
# Fecha: 29/05/2026
# Proyecto activo: C:\Users\User\Desktop\Prueba 2\
# Backup: C:\Users\User\Desktop\Prueba 2_backup_2026-05-29_133839\
# ============================================

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 1. ARQUITECTURA DEL PROYECTO
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### Stack Tecnológico
- Framework: Astro v6.4.0 (static site generator)
- CSS: Tailwind CSS v4.3.0 via PostCSS (@tailwindcss/postcss)
- Fuentes: DM Sans (headings) + Inter (body) via Google Fonts
- Imágenes: sharp v0.34.5
- SEO: @astrojs/sitemap v3.7.3
- Node: >=22.12.0

### Estructura Completa de Archivos

```
C:\Users\User\Desktop\Prueba 2\
│
├── package.json              # Dependencias y scripts
├── package-lock.json
├── astro.config.mjs          # Config Astro + sitemap
├── tsconfig.json             # TypeScript strict
├── postcss.config.mjs        # PostCSS + Tailwind
├── CONTEXTO.md               # Este archivo
│
├── node_modules/             # Dependencias instaladas
│
├── public/                   # Archivos estáticos
│   ├── images/
│   │   ├── hero-bg-new.png   # Fondo hero (desde WEB/)
│   │   └── productos/        # 38 imágenes de productos
│   │       ├── animal-lion-king-corona-roja.png
│   │       ├── animal-pantera-rosa-swag-streetwear.png
│   │       ├── dollar-gta6-vice-city-billete-100-bucks.png
│   │       ├── exclusive-bugs-bunny-selfmade.png
│   │       ├── exclusive-goku-ssj4-dragon-ball-gt.png
│   │       ├── funko-personalizado-frediel-edition.png
│   │       ├── gallery-customer-design-1.png
│   │       ├── gallery-naruto-itachi-wallpaper.png
│   │       ├── gallery-rafa-producto.jpg
│   │       ├── icon-breaking-bad-empire-business.png
│   │       ├── icon-dragon-ball-super-sparking-zero.png
│   │       ├── icon-itachi-uchiha-eternal-mangekyo.png
│   │       ├── icon-joker-arte-urbano-dc.png
│   │       ├── icon-perfect-cell-dragon-ball-z.png
│   │       ├── icon-pokemon-card-neon-fucsia.png
│   │       ├── logo-theneonsyndicate.png
│   │       ├── militar-2-cia-referencia-legion-tercio-duque-alba.png
│   │       ├── militar-3-cia-montana-escudo.png
│   │       ├── militar-3-cia-pantera-regimiento-principe-brilat.png
│   │       ├── militar-comandancia-ceuta.png
│   │       ├── militar-escarapela-circular-espana.png
│   │       ├── militar-escarapela-guardia-civil.png
│   │       ├── militar-escarapela-madoc.png
│   │       ├── militar-escarapela-ume.png
│   │       ├── militar-legion-novio-muerte-escudo.png
│   │       ├── militar-legionario-honor-muerte-novio.png
│   │       ├── militar-sereco-1-6-siempre-unida-regimiento-saboya.png
│   │       ├── militar-sereco-67-nostra-sponte.png
│   │       ├── opt/                    # Imágenes optimizadas
│   │       ├── ref-mewtwo-card.jpg
│   │       ├── ref-pokemon-card.png
│   │       ├── testimonial-cliente-1.jpg  (al 7)
│   │       └── ...
│   │
│   └── svg/                   # SVGs decorativos
│       ├── stairs.svg         # Divisor de secciones
│       ├── door.svg           # Elemento hover descubrimiento
│       ├── coin.svg           # Moneda animada (precios)
│       ├── sparkle.svg        # Destellos decorativos
│       ├── arrow.svg          # Flechas decorativas
│       ├── banner-wave.svg    # Onda decorativa
│       └── logo-neon-syndicate-v2.svg  # Logo colorido
│
├── src/
│   ├── data/
│   │   ├── categorias.json    # 3 categorías (Militar, Icon, Set Ups)
│   │   └── productos.json     # 24 productos con precios y slugs
│   │
│   ├── styles/
│   │   └── global.css         # Design system completo (252 líneas)
│   │
│   ├── layouts/
│   │   └── LayoutV2.astro     # Layout principal con SEO y scripts globales
│   │
│   ├── components/            # 17 componentes
│   │   ├── HeroSlider.astro   # Slider principal con 4 slides
│   │   ├── Header.astro       # Navbar + menú mobile
│   │   ├── Footer.astro       # Footer + newsletter
│   │   ├── FloatingWhatsApp.astro  # Botón flotante WhatsApp
│   │   ├── CategoryGrid.astro # Grid de categorías
│   │   ├── CollectionSection.astro # Sección reutilizable
│   │   ├── ProductCard.astro  # Card de producto
│   │   ├── ProductGrid.astro  # Grid de productos
│   │   ├── PriceDisplay.astro # Display de precio
│   │   ├── SizeSelector.astro # Selector de tallas
│   │   ├── Breadcrumb.astro   # Migas de pan
│   │   ├── TestimonialCarousel.astro # Carrusel clientes
│   │   ├── NewsletterBanner.astro   # Banner suscripción
│   │   ├── CTASection.astro   # Llamada a la acción
│   │   └── ui/
│   │       ├── Badge.astro    # Badge (🔥, ⭐, 💎, 🆕)
│   │       ├── Button.astro   # Botón reutilizable
│   │       └── Tag.astro      # Tag de color
│   │
│   └── pages/                 # 9 páginas → 36 rutas
│       ├── index.astro        # Home
│       ├── catalogo.astro     # Catálogo con filtros
│       ├── contacto.astro     # Contacto
│       ├── categoria/
│       │   └── [slug].astro   # 3 categorías dinámicas
│       ├── producto/
│       │   └── [slug].astro   # 24 productos dinámicos
│       └── legal/
│           ├── privacidad.astro
│           ├── terminos.astro
│           └── cookies.astro
│
├── dist/                      # Build output (generado)
│   ├── index.html
│   ├── catalogo/index.html
│   ├── contacto/index.html
│   ├── categoria/*/index.html (3)
│   ├── producto/*/index.html  (24)
│   ├── legal/*/index.html     (3)
│   ├── _astro/                # Assets compilados
│   └── sitemap-index.xml
│
└── .playwright-mcp/           # Capturas de prueba
```

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 2. DESIGN SYSTEM (global.css)
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### Colores
--color-bg:              #f7f5f0     (fondo blanco cálido)
--color-bg-surface:      #ffffff     (superficie blanca)
--color-bg-elevated:     #eeebe4     (elevado)
--color-bg-alt:          #1a1a2e     (fondo oscuro)
--color-bg-dark:         #0f0f1a     (más oscuro)
--color-text-primary:    #1a1a2e     (texto principal)
--color-text-secondary:  #5a5a7a     (texto secundario)
--color-text-muted:      #9a9ab0     (texto muted)

--color-accent-pink:     #ff2d78     (rosa vibrante)
--color-accent-blue:     #00d4ff     (cian)
--color-accent-purple:   #7c3aed     (púrpura)
--color-accent-yellow:   #ffd600     (amarillo)
--color-accent-orange:   #ff6d00     (naranja)
--color-accent-green:    #00e676     (verde)
--color-accent-red:      #ff1744     (rojo)
--color-accent-cyan:     #00e5ff     (cian claro)

### Gradientes HeroSlider
Slide 1 (NEON):     #ff2d78 → #7c3aed → #00d4ff
Slide 2 (MILITAR):  #003366 → #0055aa → #00d4ff
Slide 3 (ICON):     #7c3aed → #ff2d78 → #ff6d00
Slide 4 (SETS):     #ff6d00 → #ff2d78 → #7c3aed

### Gradientes Texto
neon:    #ffd600 → #ff2d78 → #00d4ff
militar: #00d4ff → #00e676 → #00d4ff
icon:    #ff2d78 → #ffd600 → #7c3aed
sets:    #ffd600 → #ff6d00 → #ff2d78

### Tipografía
--font-heading: "DM Sans", sans-serif (bold 800)
--font-body:    "Inter", sans-serif

### Breakpoints Responsive
< 640px:   1 columna, hero apilado, menú hamburguesa
640-1024:  2 columnas, hero compacto
> 1024px:  3-4 columnas, nav desktop

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 3. HERO SLIDER (HeroSlider.astro)
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### Slides
1. THE NEON SYNDICATE — Wall art de neón LED que BRILLA
   Badge: "✨ Nueva Colección 2026"
   CTAs: Explorar Catálogo / WhatsApp

2. MILITAR ART — Insignias de élite iluminadas
   Badge: "⚔️ Heráldica en Neón"
   CTAs: Ver Colección / Catálogo

3. ICON ART — Cultura pop hecha luz
   Badge: "🎭 Ediciones Exclusivas"
   CTAs: Ver Colección / Catálogo

4. SET UPS — Diseños personalizados y únicos
   Badge: "🎨 Tu idea, hecha luz"
   CTAs: Ver Más / Contacto

### Comportamiento
- Auto-play cada 5.5 segundos (interval)
- Transición: opacity 0.8s + transform scale
- Dots navegables abajo
- Swipe táctil (touchstart/touchend)
- Barra de progreso (5s linear)
- Primer slide comienza con clase "active"
- Gradientes definidos en <style> con nombres fijos (grad-neon, grad-militar, etc.)
- Texto gradiente con clases CSS dedicadas (gradient-text-neon, etc.)

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 4. DATOS
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### Categorías (categorias.json)
1. Militar Art (slug: militar-art, 12 productos)
2. Icon Art (slug: icon-art, 11 productos)
3. Set Ups (slug: set-ups, 4 productos)

### Productos (productos.json) — 24 productos
Militar Art (12):
- 2ª CIA 'La Referencia' IV Bandera Legión
- 3ª CIA Montaña Escudo
- 3ª CIA Pantera II/3 Regimiento Príncipe
- Comandancia General de Ceuta
- Escarapela Circular España
- Escarapela Guardia Civil
- Escarapela MADOC
- Escarapela UME
- Legión Novio de la Muerte Escudo
- Legionario Honor Muerte Novio
- SERECO 1/6 Siempre Unida
- SERECO 67 Nostra Sponte

Icon Art (11):
- Breaking Bad Empire Business
- Pokémon Card Neon Edition
- Dragon Ball Super Sparking Zero
- Itachi Uchiha Eternal Mangekyō 1/1
- Joker Arte Urbano DC
- Perfect Cell Dragon Ball Z
- Bugs Bunny Selfmade Exclusive
- Goku SSJ4 Dragon Ball GT Exclusive
- GTA6 Vice City Dollar Bill
- Lion King Corona Roja
- Pantera Rosa Swag Streetwear

Set Ups (4):
- Funko Personalizado Frediel Edition
- Customer Design Personalizado
- Naruto Itachi Wallpaper Gallery
- Rafa Custom Gallery Piece

### Rangos de Precios
- Desde 95.00 € (tallas pequeñas) hasta 219.00 € (tallas grandes)
- Tallas comunes: 30x40, 40x50, 40x60, 55x75, 60x80, 70x95
- Envío gratis a España

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 5. COMPONENTES — Props y Comportamiento
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### HeroSlider.astro
- Sin props (autocontenido)
- Renderiza 4 slides con datos internos
- CSS gradients via clases fijas en <style>
- JS slider con auto-play, dots, touch

### Header.astro
- NavLinks: Inicio, Militar Art, Icon Art, Set Ups, Catálogo, Contacto
- Mobile: menu-toggle con overlay fullscreen
- Sticky + bg blanco backdrop-blur
- Logo: inline SVG gradient NS

### Footer.astro
- Brand + redes sociales
- 4 columnas: Categorías, Contacto, Legal, Newsletter
- Fondo: #0f0f1a
- Año dinámico

### FloatingWhatsApp.astro
- Posición: fixed bottom-6 right-6
- Link: https://wa.me/34722617372
- Gradient bg: pink → purple
- Hover: scale-110 + glow

### CategoryGrid.astro
- Props: categories[], products[]
- 3 tarjetas con overlay de color por categoría
- Hover: scale image + opacity overlay

### CollectionSection.astro
- Props: title, description, products[], categories[]
- Grid 3 columnas de ProductCard
- Link "Ver todos" desktop/mobile

### ProductCard.astro
- Props: product, category, badge, badgeVariant
- Borde y glow por categoría (blue/pink/purple)
- Hover: translateY(-6px) scale(1.02)
- Precio: "desde X.XX €"

### ProductGrid.astro
- Props: products[], categories[]
- Grid responsive 1/2/3 columnas
- Empty state con link a /catalogo

### PriceDisplay.astro
- Props: minPrice, maxPrice, productName
- id="price-display" (target para JS)
- gradient-text-alt en el precio

### SizeSelector.astro
- Props: sizes[], prices{}, productName
- Grid 2/4 columnas de botones
- define:vars={{ productName }} para pasar dato al JS
- JS: actualiza priceDisplay.innerHTML y whatsapp URL

### Breadcrumb.astro
- Props: items[] ({label, href})
- Separador: "/"
- Último item: texto rosa

### TestimonialCarousel.astro
- Props: testimonials[] ({img, nombre})
- Carrusel infinito con máscara gradiente
- Duplica array para loop seamless

### NewsletterBanner.astro
- Sin props
- Gradient bg: pink → purple → blue
- Input + botón suscripción

### CTASection.astro
- Sin props
- Título + WhatsApp CTA
- "Envíos gratuitos a España"

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 6. PÁGINAS — Comportamiento
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### index.astro (Home)
- HeroSlider
- Marquee strip (envío gratis, vinilo premium, etc.)
- CategoryGrid
- CollectionSection (6 productos destacados)
- TestimonialCarousel
- NewsletterBanner
- CTASection

### catalogo.astro
- Filtros por categoría (JS: filter-btn)
- ProductGrid con todos los productos
- Contador de productos visible
- Filtro activo: borde rosa + bg rosa10

### categoria/[slug].astro (3 rutas)
- Hero con gradiente según categoría
- ProductGrid filtrado
- getStaticPaths genera 3 páginas

### producto/[slug].astro (24 rutas)
- Breadcrumb
- Imagen + info en 2 columnas
- PriceDisplay + SizeSelector + WhatsApp CTA
- 3 info boxes (Material, Plug&Play, Personalización)
- JS: size selection actualiza precio y WhatsApp

### contacto.astro
- 2 cards: WhatsApp + Bizum
- 4 pasos de compra
- Gradientes en números

### legal/*.astro (3 páginas)
- Privacidad, Términos, Cookies
- Texto legal completo
- Diseño limpio y legible

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 7. HISTORIAL DE INCIDENCIAS
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

### Bug #1: Títulos HeroSlider no se renderizaban
- Síntoma: {slide.accent} aparecía literal en HTML
- Causa: Expresiones Astro dentro de class="... {expr} ..." en .map() no se resuelven
- Fix: Clases CSS fijas en <style> (gradient-text-neon, etc.) + class:list

### Bug #2: Slider no arrancaba con slide activo
- Síntoma: Primer slide no visible hasta auto-play
- Causa: {idx === 0 ? 'active' : ''} literal en HTML
- Fix: class:list={['hero-slide', idx === 0 && 'active']}

### Bug #3: Precio no se actualizaba al seleccionar talla
- Síntoma: SizeSelector no modificaba priceDisplay
- Causa: Código de actualización faltaba en script
- Fix: priceDisplay.innerHTML en el click handler

### Bug #4: productName no se pasaba al script
- Síntoma: {productName} literal en JS
- Causa: Astro no procesa expresiones dentro de template literals en <script>
- Fix: define:vars={{ productName }}

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 8. COMANDOS ÚTILES
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# Desarrollo
cd "C:\Users\User\Desktop\Prueba 2"
npm run dev                    # Servidor local (puerto por defecto)
npm run dev -- --port 4323     # Puerto específico
npm run dev -- --host          # Acceso red local

# Build
npm run build                  # Compilar a dist/
npm run preview                # Previsualizar build

# Gestión
npx @astrojs/upgrade           # Actualizar Astro
npm install                    # Reinstalar dependencias

# Backup
xcopy "Prueba 2" "Prueba 2_backup" /E /I /H
# ZIP: Compress-Archive -Path "Prueba 2" -DestinationPath "Prueba 2.zip"

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 9. CARPETAS EN EL SISTEMA
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

C:\Users\User\Desktop\Prueba\
  ├── WEB/                  → V1 original (oscura, lujo editorial)
  ├── WEB-V2/               → V2 backup (primera versión colorida)
  └── opencode.jsonc        → Config OpenCode

C:\Users\User\Desktop\Prueba 2\   → 🎯 VERSIÓN ACTIVA
  └── CONTEXTO.md                  → Este archivo

C:\Users\User\Desktop\Prueba 2_backup_2026-05-29_133839\
  └── (copia de seguridad completa)

## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## 10. CONTACTO Y REDES
## ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

WhatsApp: +34 722 61 73 72
Web: https://theneonsyndicate.com (V1)
Pago: Bizum
Envío: Gratis a España peninsular
Producto: Vinilo premium LED, Plug&Play, personalizable
