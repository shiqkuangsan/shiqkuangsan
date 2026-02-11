# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

GitHub profile README repository (`shiqkuangsan/shiqkuangsan`). The `README.md` in `main` branch is rendered directly on https://github.com/shiqkuangsan as the profile page.

Owner: shiqkuangsan — Frontend Engineer, Vue ecosystem contributor, currently working on antdv-next (Ant Design for Vue).

## Repository Structure

- `README.md` — The profile page content (Markdown + HTML, centered layout with badges, stats cards, and animated SVGs)
- `.github/workflows/snake.yml` — GitHub Actions workflow that generates contribution snake animation SVGs every 12 hours, pushes to `output` branch
- `output` branch — Auto-generated branch containing `github-snake.svg` and `github-snake-dark.svg` (do not edit manually)

## Key Details

- No build system, no dependencies, no tests — this is purely a Markdown/HTML profile page
- External services used for dynamic content:
  - `readme-typing-svg.demolab.com` — Typing animation header
  - `github-readme-streak-stats.herokuapp.com` — Streak stats
  - `github-profile-summary-cards.vercel.app` — Profile summary cards
  - `github-readme-activity-graph.vercel.app` — Contribution graph
  - `img.shields.io` / `komarev.com` — Badges
  - `capsule-render.vercel.app` — Waving footer
  - `Platane/snk` GitHub Action — Snake SVG generation
- Theme color: `#41B883` (Vue green), dark background: `#0D1117`
- The snake SVG uses `<picture>` tag with `prefers-color-scheme` for dark/light mode support

## Editing Guidelines

- Preview changes on GitHub directly — local Markdown renderers won't show the external SVG services correctly
- When adding/changing badge URLs, use `style=for-the-badge` and `labelColor=1a1a2e` for consistency
- Stats card theme: `tokyonight` or `github_dark` with `hide_border=true` and `background=0D1117`
