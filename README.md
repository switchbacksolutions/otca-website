# Open Trails Community Alliance (OTCA) Website

The website for the Open Trails Community Alliance — a volunteer-led organization
working to preserve and protect trail access in Meadow Vista, CA. The site publishes
community updates and links residents to the email list, GoFundMe, and Facebook page.

Built with Astro.js, Tailwind CSS, and CloudCannon CMS. Deployed on Netlify.

## Quick start

```bash
git clone <repo-url> otca-site
cd otca-site
npm install
npm run dev
```

Open [http://localhost:4321](http://localhost:4321).

## Tech stack

| Tool | Version | Purpose |
|------|---------|---------|
| [Astro](https://astro.build) | ^4 | Static site generator |
| [TypeScript](https://typescriptlang.org) | ^5 | Type safety |
| [Tailwind CSS](https://tailwindcss.com) | ^3 | Utility-first CSS |
| [@astrojs/mdx](https://docs.astro.build/en/guides/integrations-guide/mdx/) | ^3 | MDX support |
| [@astrojs/sitemap](https://docs.astro.build/en/guides/integrations-guide/sitemap/) | ^3 | Auto sitemap |
| [@astrojs/rss](https://docs.astro.build/en/guides/rss/) | ^4 | RSS feed |
| [Vitest](https://vitest.dev) | ^2 | Unit testing |
| [Playwright](https://playwright.dev) | ^1.49 | E2E testing |

## Scripts

```bash
npm run dev         # Start dev server at http://localhost:4321
npm run build       # Build for production → dist/
npm run preview     # Preview the production build locally
npm run check       # Run astro check + TypeScript
npm test            # Run Vitest unit tests
npm run test:e2e    # Run Playwright E2E tests
npm run test:all    # Run unit + E2E tests
```

## Project layout

```
src/
  components/     # Reusable Astro components
  content/blog/   # Markdown / MDX blog posts (community updates)
  layouts/        # Page shell layouts
  pages/          # File-based routes
  styles/         # Global CSS + Tailwind layers
tests/
  e2e/            # Playwright browser tests
  unit/           # Vitest unit tests
docs/
  TESTING.md      # Testing guide
  DEPLOYMENT.md   # Deployment guide
```

## Adding a blog post (community update)

Create a new `.md` or `.mdx` file in `src/content/blog/`:

```markdown
---
title: 'My Update Title'
description: 'A short description for SEO.'
pubDate: '2024-03-01'
tags:
  - trails
  - update
draft: false
---

Post content goes here.
```

## Deployment

Connected to [Netlify](https://netlify.com). The `netlify.toml` configures the
build command, publish directory, Node version, security headers, and caching
rules automatically.

See [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md) for full instructions.
