# REMSA — remsa-www

Sitio web para **REMSA (Maquinaria Servicio y Refacciones)**, empresa mexicana de mantenimiento y refacciones para maquinaria pesada (construcción y minería). Filial de Transportes Morla SA de CV, fundada 2023, base en Veracruz e Hidalgo.

## Repositorio

- **GitHub:** https://github.com/jsanjuan71/remsa-www.git
- **GitHub Pages:** https://jsanjuan71.github.io/remsa-www/
- **Rama:** `master`

## Objetivo del sitio

Generación de leads y contacto directo. Un humano da seguimiento a cada contacto. Sin automatización por ahora — se agrega después.

## Estructura del proyecto

```
remsa/
├── index.html              # Selector de propuestas (pantalla de entrada)
├── propuesta-a.html        # Propuesta A — Industrial Premium (dark)
├── propuesta-b.html        # Propuesta B — Confianza Técnica (light)
├── assets/
│   └── img/
│       └── icons/          # Logos de marcas (caterpillar.jpg, komatsu.png, etc.)
└── docs/
    ├── logo.jpeg           # Logo oficial REMSA
    ├── curriculum Remsa.docx
    └── BOLETINES REMSA.pptx
```

## Identidad visual del cliente

- **Paleta logo:** Negro, Amarillo (#F5C000), Rojo (#CC0000)
- **Tagline:** "Maquinaria servicio y refacciones"
- **Contacto:** 771 842 8884 / 771 238 8481 · gpo_remsa@hotmail.com
- **Horario:** L–V 9:00–17:30, Sáb 9:00–14:00
- **RFC:** TMO231228H92
- **Representante:** Ing. Hector Matus Pineda / Gerente: Ing. José E. Acosta R.

## Propuesta A — Industrial Premium

- Dark mode, fondo #0a0a0a
- Paleta: amarillo #F5C000, rojo #CC0000, blanco
- Tipografía: Bebas Neue (headings) + Inter (cuerpo)
- Hero: foto de maquinaria (Unsplash) con overlay oscuro, layout 2 columnas (headline izq, texto+CTA der)
- Headline hero: "Tu maquinaria **no** para. Nosotros tampoco." (`no` en rojo)
- Eyebrow: "Diagnóstico preciso · Refacciones certificadas · Servicio garantizado"
- Back-to-top: amarillo → hover rojo, esquina inferior derecha

## Propuesta B — Confianza Técnica

- Light mode, fondo #FFFFFF / #F4F6F9
- Paleta: azul #1A3A5C (primario), gris acero #4A5568, rojo #CC0000, amarillo #F5C000
- Tipografía: Montserrat (headings) + Open Sans (cuerpo)
- Hero: misma foto con overlay azul, patrón geométrico CSS
- Back-to-top: ya existía como `#scroll-top` (circular, azul) — no agregar otro
- Fix aplicado: `word-break: break-all` en `.ci-value a` y `min-width: 0` en `.contact-grid > *`

## Logos de marcas (`assets/img/icons/`)

| Archivo | Marca |
|---|---|
| caterpillar.jpg | Caterpillar |
| komatsu.png | Komatsu |
| case.png | Case |
| terex.png | Terex |
| sandvik.png | Sandvik |
| liebherr.png | Liebherr |
| atlas_copco.png | Atlas Copco |
| dynapac.png | Dynapac |
| ingersoll_rand.png | Ingersoll-Rand |
| jcb.png | JCB |

Nombres con **guión bajo** (no guión): `atlas_copco`, `ingersoll_rand`.

## Secciones en ambas propuestas

1. **Hero** — foto fondo + headline + CTA
2. **Servicios** — 4 cards: Mantenimiento, Hidráulica, Refacciones, Electrónica
3. **Por qué REMSA** — 3 diferenciadores: Capacitación Canadá, Software CAT SIS, Refacciones certificadas
4. **Marcas** — grid 5 cols con logos (grayscale → color al hover)
5. **Contacto** — formulario `mailto:` + datos de contacto + redes sociales
6. **Footer** — contacto, navegación, RFC, redes sociales, copyright 2026

## Redes sociales

- Facebook: `#` (placeholder)
- WhatsApp: `https://wa.me/527718428884` (número real)
- LinkedIn: `#` (placeholder)

## Pendientes / Próximos pasos

- [ ] Definir qué propuesta aprueba el cliente (o combinación de elementos)
- [ ] Conseguir foto real de maquinaria de REMSA (actualmente usa Unsplash placeholder)
- [ ] URLs reales de Facebook y LinkedIn
- [ ] Decidir dominio personalizado (actualmente en GitHub Pages)
- [ ] Construir versión final como sitio real (Astro / Next.js static / HTML puro)
- [ ] Agregar automatización de contacto (cuando el cliente esté listo)

## Notas técnicas

- Todo en HTML/CSS/JS vanilla — sin frameworks, sin build tools
- Formularios con `action="mailto:"` — sin backend
- Imágenes de logos: `onerror` detecta si no existe el archivo y muestra texto fallback
- `propuesta-b.html` ya tiene `#scroll-top` propio — no agregar `#btt` adicional
- Foto hero: `https://images.unsplash.com/photo-1746349526405-a280f827bc6b` (Troy Mortier, Unsplash)
- Deploy: `git push origin master` → GitHub Pages actualiza en ~1 min
