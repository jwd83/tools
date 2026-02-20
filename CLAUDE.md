# Tools Desktop

Classic Mac OS System 7 desktop UI that launches Jared's web tools.

## Stack

- Plain HTML/CSS/JS, no build step, no dependencies
- Hosted on GitHub Pages at tools.jwd.me

## Architecture

- `apps.js` — the `tools` array registry of all tool entries (title, description, link, category, optional `blank`)
- `index.html` — all HTML, CSS, and JS for the desktop UI
- CSS variables in `:root` control the System 7 gray/black theme
- Desktop icons are generated from the tools array, double-click (or tap) opens a draggable/resizable window with an iframe
- Tools with `blank: true` open in a new tab instead of an iframe window; omit the property for in-window tools
- Favicons are resolved with a waterfall strategy and cached in localStorage
- Windows have subtle open animations and titlebar line patterns for authentic System 7 feel
- Menu bar dropdowns are populated from tool categories and support hover-switching

## Conventions

- Preserve the classic Mac OS System 7 aesthetic (gray panels, black borders, Geneva/APL386 font, crosshatch resize handles, titlebar stripes)
- No external JS/CSS libraries or CDN imports
- Prefer CSS shorthand where possible (e.g. `border-block` over separate `border-top`/`border-bottom`)
- Prefer small, targeted edits over broad refactors
- To add a tool: add an object with `title`, `description`, `link`, and `category` to the `tools` array in `apps.js` (add `blank: true` only if the tool must open in a new tab)
