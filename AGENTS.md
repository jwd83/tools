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
- Preserve the classic Mac OS System 7 aesthetic (gray panels, black borders, Geneva/APL386 font, crosshatch resize handles, titlebar stripes).
- No external JS/CSS libraries or CDN imports.

## Tool Entry Conventions
- Tool objects in `apps.js` should include `title`, `description`, `link`, and `category`.
- Use `blank: true` only when a tool must open in a new tab instead of an iframe window.
- Desktop icons and menu items are generated from the `tools` array, so registry changes in `apps.js` drive the UI.
