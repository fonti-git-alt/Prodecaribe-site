# Prodecaribe Landing

Landing page para Prodecaribe - Plataforma de inversión en el Caribe colombiano.

## 🚀 Stack

- **Astro** - Framework web (HTML-first, zero JS por defecto)
- **Tailwind CSS** - Estilado utility-first
- **GSAP** - Animaciones de grado cinematográfico
- **Lenis** - Smooth scroll premium
- **Cloudflare Pages** - Hosting (deploy directo)

## ✨ Características

- Smooth scroll con Lenis (efecto Apple-style)
- Parallax effects en el hero
- Animaciones de entrada con GSAP ScrollTrigger
- 100% responsive (mobile-first)
- SEO optimizado
- Zero JavaScript innecesario

## 📦 Instalación

```bash
# Instalar dependencias
npm install

# Desarrollo local
npm run dev

# Build para producción
npm run build

# Preview del build
npm run preview
```

## 🌐 Deploy a Cloudflare Pages

### Opción 1: Git Integration (Recomendado)

1. Subí este proyecto a GitHub/GitLab
2. conectá tu repo a Cloudflare Pages
3. Configurá:
   - **Build command**: `npm run build`
   - **Build output**: `dist`

### Opción 2: Wrangler CLI

```bash
# Instalar wrangler
npm install -g wrangler

# Login
wrangler login

# Deploy
wrangler pages deploy dist
```

## 📁 Estructura del proyecto

```
/
├── src/
│   ├── layouts/
│   │   └── Layout.astro      # Layout base con GSAP + Lenis
│   ├── pages/
│   │   └── index.astro       # Página principal
│   └── components/
│       ├── Hero.astro        # Hero con parallax
│       ├── QuickIntro.astro  # 8 industrias intro
│       ├── Problem.astro     # Sección emocional
│       ├── Industries.astro  # Grid de industrias
│       ├── Testimonials.astro # Social proof
│       ├── Trust.astro       # Por qué nosotros
│       ├── CTA.astro         # CTAs finales
│       ├── Footer.astro      # Footer
│       └── WhatsAppCTA.astro # Sticky WhatsApp
├── public/
│   └── favicon.svg
├── astro.config.mjs
├── tailwind.config.mjs
└── package.json
```

## 🎨 Personalización

### Colores (en `tailwind.config.mjs`)

```javascript
colors: {
  'prode-blue': '#0C4A6E',
  'prode-light': '#38BDF8',
  'prode-gold': '#F59E0B',
  'prode-gold-light': '#FCD34D',
}
```

### Links de WhatsApp

Buscar y reemplazar `https://wa.me/1234567890` con tu número real:
- Formato: `https://wa.me/NUMERO` (sin + ni guiones)

## 📝 Licencia

MIT
