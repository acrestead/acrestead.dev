# acrestead.dev

Content site at the intersection of homesteading and technology — practical writing on growing food, working land, and the tools (homelab, sensors, small scripts) that make small-scale farming smarter.

## Stack

- **Framework:** Astro (blog template, TypeScript strict)
- **Project root:** `./site/` (the Astro project lives in a subfolder; the repo root holds infra + this file)
- **Hosting:** Cloudflare Workers (Workers Builds) deploying static assets. Config in `site/wrangler.jsonc` — explicitly static-asset-only so Wrangler doesn't auto-install `@astrojs/cloudflare` and switch the build to server mode. Worker name: `acrestead`. Auto-deploys on push to `main`.
- **Domain:** acrestead.dev

## Brand

- **Tagline:** Homesteading × technology.
- **Palette (earthy & warm):**
  - Background: `#f7f3ec` (warm off-white)
  - Text: `#2b2a26` (warm near-black)
  - Accent: `#4a6b3a` (forest green)
  - Accent 2: `#b85c38` (terracotta)
- **Voice:** Grounded, practical, first-person notes. Not corporate, not breezy.

## Conventions

- Astro content collections live in `site/src/content/blog/`. Add new posts as `.md` or `.mdx` with frontmatter matching `site/src/content.config.ts`.
- Site-wide strings (title, description, tagline) live in `site/src/consts.ts` — update there, not in individual pages.
- SEO meta is centralized in `site/src/components/BaseHead.astro`.
