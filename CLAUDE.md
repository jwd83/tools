# Tools Desktop

Static single-file site (index.html) — classic Mac OS System 7 desktop UI that launches Jared's web tools.

## Stack

- Plain HTML/CSS/JS, no build step, no dependencies
- Hosted on GitHub Pages at tools.jwd.me

## Architecture

Everything lives in `index.html`:
- CSS variables in `:root` control the System 7 gray/black theme
- `tools` array holds all tool entries (title, description, link, category)
- Desktop icons are generated from the tools array, double-click (or tap) opens a draggable/resizable window with an iframe
- Favicons are resolved with a waterfall strategy and cached in localStorage
- Windows have subtle open animations and titlebar line patterns for authentic System 7 feel
- Hover/focus transitions on icons, menu items, and buttons for polish

## Conventions

- Keep everything in the single `index.html` file
- Preserve the classic Mac OS System 7 aesthetic (gray panels, black borders, Geneva/APL386 font, crosshatch resize handles, titlebar stripes)
- No external JS/CSS libraries or CDN imports
- Prefer CSS shorthand where possible (e.g. `background` over separate properties)
- Prefer small, targeted edits over broad refactors
- To add a tool: add an object with `title`, `description`, `link`, and `category` to the `tools` array
- Experimental/unstable tools go in `experimentalTools` and get moved to `tools` when stable
