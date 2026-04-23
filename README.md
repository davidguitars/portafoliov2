# David Urdaneta — Portfolio v2

Portfolio personal construido con Astro, diseño técnico/editorial minimalista orientado a marca personal y captación de clientes enterprise.

<img width="1616" height="795" alt="image" src="https://github.com/user-attachments/assets/e8ff5776-572b-430c-8430-ae437b0c3f04" />


---

## Stack

- **[Astro](https://astro.build/)** — framework principal, generación estática
- **[Tailwind CSS](https://tailwindcss.com/)** — utilidades de estilo
- **[GSAP](https://gsap.com/)** — animaciones (ticker de tools, logos de clientes)
- **[IBM Plex Mono + IBM Plex Sans](https://fonts.google.com/)** — sistema tipográfico
- **[Remix Icon](https://remixicon.com/)** — iconografía

---

## Estructura

```
src/
├── components/
│   ├── Header.astro          # Nav sticky con menú mobile
│   ├── Hero.astro            # Canvas animado red global + foto
│   ├── Tools.astro           # Ticker de tecnologías con GSAP
│   ├── Service.astro         # Grid de servicios con stats
│   ├── Works.astro           # Proyectos seleccionados
│   ├── Reviews.astro         # Testimonios + ticker de logos
│   ├── CallToAction.astro    # Sección de contacto dark
│   ├── Footer.astro          # Footer minimalista
│   ├── Button.astro          # Componente de botón reutilizable
│   └── MarkdownPost.astro    # Layout para artículos del blog
├── layouts/
│   └── Layout.astro          # HTML base
├── pages/
│   ├── index.astro           # Home
│   ├── blog.astro            # Listado del blog
│   └── posts/               # Artículos en Markdown
│       └── *.md
├── styles/
│   └── global.css            # Tokens de diseño y utilidades
public/
└── images/                   # Imágenes estáticas y foto de perfil
```

---

## Comandos

```bash
npm install       # Instala dependencias
npm run dev       # Servidor local en localhost:4321
npm run build     # Build de producción en ./dist/
```

---

## Personalización rápida

**Datos personales** → `src/sample.ts`
```ts
const author = {
  name:     "Tu nombre",
  nickname: "Tu apodo",
  email:    "mailto:tuemail@dominio.com",
  ig:       "https://instagram.com/...",
  x:        "https://x.com/...",
  tiktok:   "https://tiktok.com/...",
}
```

**Proyectos** → `src/components/Works.astro`

**Servicios** → `src/components/Service.astro`

**Testimonios y logos** → `src/components/Reviews.astro`

**Artículos del blog** → crear archivos `.md` en `src/pages/posts/` con este frontmatter:
```md
---
layout: ../../components/MarkdownPost.astro
title: "Título del artículo"
image:
  url: "https://url-imagen.jpg"
  alt: "descripción"
tags: ["Tag1", "Tag2"]
pubDate: 'Abr 22, 2026'
---

Contenido en Markdown...
```

---

## Deploy en Hostinger

```bash
npm run build
# Sube el contenido de /dist a public_html/ en tu panel de Hostinger
```

---

## Diseño

Dirección visual: **técnico / editorial** — tipografía monoespaciada, grid de líneas finas, acento lima `#C8FF00`, fondo paper `#F5F4F0`.

Secciones incluidas: Hero con red global animada · Ticker de herramientas · Servicios con stats · Trabajos seleccionados · Testimonios · Blog con sidebar y CTA · Contacto dark · Footer.

---

Construido por **David Urdaneta** — [instagram](https://instagram.com/codetonero) · [x](https://x.com/codetonero)
