# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio site built with Astro 5, Tailwind CSS 4, and MDX. Deployed to GitHub Pages at `https://annaleviy.github.io/portfolio`.

## Commands

- `pnpm dev` — Start dev server (localhost:4321)
- `pnpm build` — Production build to `./dist/`
- `pnpm preview` — Preview production build locally

Package manager is **pnpm** (v9 in CI). No test or lint scripts are configured.

## Architecture

- **Astro 5** with strict TypeScript config
- **Tailwind CSS 4** integrated via `@tailwindcss/vite` plugin (not PostCSS), imported in `src/styles/global.css`
- **MDX** support via `@astrojs/mdx` integration
- `src/layouts/Layout.astro` — Base HTML layout with `<slot>` and named `<slot name="head" />`
- `src/pages/` — File-based routing (Astro and MDX files)
- `astro.config.mjs` — Site config with `base: "/portfolio"` for GitHub Pages subpath deployment
- CI deploys on push to `main` via `.github/workflows/deploy.yml`

## Notes

- The site language is Russian (`lang="ru"`)
