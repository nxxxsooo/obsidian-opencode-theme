# obsidian-opencode-theme

## Overview
Dark theme for Obsidian inspired by the OpenCode terminal aesthetic. Published to Obsidian community themes.

## Architecture
- Single `theme.css` file
- `manifest.json` for Obsidian theme registry

## Key Files
- `theme.css` — All styles
- `manifest.json` — Theme metadata
- `screenshot.png` — Community listing screenshot (512x288)

## Patterns & Conventions
- Screenshot must be 512x288 per Obsidian community guidelines
- Terminal-inspired color palette with font support for terminal plugins
- Tag format: bare version (`1.3.0`), not `v1.3.0`
- Two repos must stay in sync: this one (community source) + `opencode-themes` monorepo (`obsidian/` subdir)
- `--file-line-width` uses fixed `900px`, not viewport-relative units
- Width-constraining rules (`.cm-sizer`, `.markdown-preview-sizer`) must be scoped under `.is-readable-line-width` to not break readable line length toggle

## Resolved Issues
- Resized screenshot to 512x288 as recommended by community
- v1.2.0: Fixed readable line length toggle not working — `max-width: 80vw !important` was unconditionally applied, overriding Obsidian's `.is-readable-line-width` class toggle
- v1.3.0: Full palette realignment to OpenCode TUI default theme (opencode.json). Previous colors were Tokyo Night-derived; now exact match: primary=#fab283, secondary=#5c9cf5, accent=#9d7cd8, bg=#0a0a0a gray scale. All syntax, callout, table, and markdown colors updated.
