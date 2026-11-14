# Website projects

Applies when the brief says `Category: website`. Read together with everything in `core/`.

## Stack
- Default: Next.js + React + TypeScript. Vite + React for small single-page tools. Ask before choosing anything else.
- Next.js and other fast-moving frameworks: read the installed version's docs first (`node_modules/next/dist/docs/`). Your memory may be outdated.

## Skills

Choose by what the idea needs:
- Any page or UI (always check): ui-ux-pro-max
- Design tokens, CSS variables, spacing and type scales: design-system
- Project uses Tailwind or shadcn/ui: ui-styling
- Brand voice, identity, style guide: brand
- Banners, hero visuals, social graphics: banner-design
- Presentation or slides page: slides
- Broad design task no other skill covers: design
Path for each: types/website/skills/<name>/SKILL.md
If a skill conflicts with the project's own design direction (for example DESIGN_DIRECTION.md), the project's design direction wins.
Read a skill's SKILL.md only when its use case applies:
- types/website/skills/ui-ux-pro-max/SKILL.md: designing or reviewing any UI (styles, colors, fonts, accessibility, responsive layout)
- types/website/skills/design-system/SKILL.md: building design tokens, CSS variables, spacing and type scales
- types/website/skills/ui-styling/SKILL.md: only if the project uses Tailwind or shadcn/ui
- types/website/skills/brand/SKILL.md: brand voice, visual identity, style guides
- types/website/skills/banner-design/SKILL.md: banners, hero images, social media graphics
- types/website/skills/slides/SKILL.md: HTML presentations
- types/website/skills/design/SKILL.md: broad design tasks that no other skill covers
If a skill conflicts with the project's own design direction (for example DESIGN_DIRECTION.md), the project's design direction wins.
## Structure
- Pages in `src/app/`, reusable UI in `src/components/`, content in `src/data/`, styles and design tokens in `src/styles/`.
- Colors, fonts and spacing live in one tokens file. Never hard-code them inside components.
- Every text, link and list that may change goes in `src/data/`, not inside components.

## Content and honesty
- No invented testimonials, numbers, clients or logos. Show an empty state until real content exists.
- Real images only, with `alt` text and real width and height.

## Fonts, assets, third parties
- Self-host fonts. No external fonts, scripts or trackers unless the brief says so.
- Images in WebP or AVIF.

## Accessibility
- Semantic HTML, one `h1` per page, labeled inputs, visible focus, readable contrast.
- Respect reduced motion. Everything must work by keyboard.
- Animation only where it helps understanding. Content must be readable without JavaScript.

## SEO and sharing
- Unique title and description per page, Open Graph image, `sitemap` and `robots`.
- Unpublished or draft pages return 404.

## Testing
- Check at 390, 768 and 1440 px.
- Playwright smoke tests for main pages and the main action. Run axe for accessibility.
- Run lint, typecheck and build before saying "done".

## Deploy
- Vercel or Netlify for apps, GitHub Pages for purely static sites.
