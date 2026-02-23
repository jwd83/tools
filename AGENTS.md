# AGENTS.md

## Purpose
This repo is a static homepage for Jared's web tools.

## Key Files
- `apps.js`: Tool list data (`tools` array / tool registry).
- `index.html`: Main page UI, styles, and desktop behavior (imports `apps.js`).
- `favicon.svg`: Site favicon (hammer icon).
- `CNAME`: Custom domain configuration for GitHub Pages.

## How To Add A Tool
1. Add a new object to the `tools` array in `apps.js`.
2. Include `title`, `description`, and `link`.
3. Keep descriptions short and action-focused.

## Experimental Tools
- Add unstable projects to `experimentalTools` in `apps.js`.
- Move them into `tools` once they are stable.

## Editing Notes
- This is plain static HTML/CSS/JS. No build step is required.
- Keep the visual style consistent with existing cards and gradients.
- Prefer small, targeted edits over broad refactors.
