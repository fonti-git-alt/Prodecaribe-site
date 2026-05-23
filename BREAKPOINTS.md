# Breakpoints Documentation

## Overview

This document defines the responsive breakpoints used in the Prodecaribe landing page. These breakpoints allow you to make device-specific changes without affecting other viewports.

## Breakpoint Definitions

| Name | Min Width | Max Width | Typical Devices | Tailwind |
|------|-----------|-----------|-----------------|----------|
| Mobile | — | 767px | Phones | `max-md` |
| Tablet | 768px | 1023px | Tablets, iPad | `md` |
| Desktop | 1024px | — | Laptops, Desktops | `lg` |

## Usage in CSS/Tailwind

### Tailwind Utility Classes

Use these standard Tailwind responsive prefixes:

- `max-md:` - Mobile only (up to 767px)
- `md:` - Tablet (768px to 1023px) 
- `lg:` - Desktop (1024px and up)

### Examples

```html
<!-- Hide on mobile, show on desktop -->
<div class="hidden lg:block">Desktop only</div>

<!-- Show only on mobile -->
<div class="block md:hidden">Mobile only</div>

<!-- Different padding per device -->
<div class="p-4 md:p-8 lg:p-12">Responsive padding</div>

<!-- Device-specific background -->
<div class="bg-white md:bg-gray-50 lg:bg-slate-100">Adaptive background</div>
```

### Custom Media Queries (CSS)

```css
/* Mobile only (up to 767px) */
@media (max-width: 767px) {
  .hero-title {
    font-size: 1.5rem;
  }
}

/* Tablet only (768px to 1023px) */
@media (min-width: 768px) and (max-width: 1023px) {
  .hero-title {
    font-size: 2rem;
  }
}

/* Desktop and up (1024px+) */
@media (min-width: 1024px) {
  .hero-title {
    font-size: 2.5rem;
  }
}
```

## Device Detection Classes

The Layout.astro includes body classes for JavaScript-based device detection:

- `.device-mobile` - Applied on mobile devices
- `.device-tablet` - Applied on tablet devices  
- `.device-desktop` - Applied on desktop devices

These classes are automatically updated on window resize.

## Common Patterns

### Conditional Element Display

```html
<!-- Element visible only on mobile -->
<div class="block md:hidden">Mobile content</div>

<!-- Element visible only on tablet -->
<div class="hidden md:block lg:hidden">Tablet content</div>

<!-- Element visible only on desktop -->
<div class="hidden lg:block">Desktop content</div>
```

### Different Image Sources Per Device

```html
<picture>
  <source media="(max-width: 767px)" srcset="/image-mobile.jpg">
  <source media="(min-width: 768px) and (max-width: 1023px)" srcset="/image-tablet.jpg">
  <source media="(min-width: 1024px)" srcset="/image-desktop.jpg">
  <img src="/image-desktop.jpg" alt="Responsive image">
</picture>
```

### JavaScript Device Detection

```javascript
// Check current device type
if (document.body.classList.contains('device-mobile')) {
  // Mobile-specific logic
}

if (document.body.classList.contains('device-tablet')) {
  // Tablet-specific logic
}

if (document.body.classList.contains('device-desktop')) {
  // Desktop-specific logic
}
```

## Testing Breakpoints

To test responsive behavior:

1. Chrome DevTools → Toggle Device Toolbar (Ctrl+Shift+M)
2. Test the following widths:
   - Mobile: 375px, 414px (iPhone sizes)
   - Tablet: 768px, 1024px (iPad sizes)
   - Desktop: 1280px, 1440px, 1920px

---

**Last updated:** May 2026
**Maintained by:** Development Team