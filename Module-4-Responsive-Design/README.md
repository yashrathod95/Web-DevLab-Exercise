# Module 4: Responsive Design and Lighthouse

Worksheet 14 (BTBC124): Responsive Web Design and Lighthouse.
Project: **CampusBite**, a canteen menu page (header, nav, "Today's Special" banner, six menu cards, footer).

## Structure

| Folder | Questions | Contents |
| --- | --- | --- |
| `Part-1-Responsive-Layout/` | Q1 to Q3 | Mobile-first base, breakpoints, intrinsic grid |
| `Part-2-Lighthouse-Audit-Fix/` | Q4 to Q5 | Broken page, Lighthouse audit, fixed page |

Each question folder has an `index.html` and a `style.css`. Each part has its own `images/` folder.

## How to run

Open the page with VS Code **Live Server** (Go Live), then open the link in Chrome or Safari.

## Part 1 summary

### Q1: Mobile-first base
- Viewport meta tag, 90% container (`max-width: 75rem`), `1rem` base text.
- Images: `max-width: 100%; height: auto`, with `width`, `height` and `alt` set.
- One-column card grid with a 1rem gap, and full-width nav links with about 52px tap targets.
- Checked at 320px and 390px: no horizontal scrolling.

### Q2: Breakpoints
- Breakpoint 1: `37.5em` (600px). The cards become 2 per row and the nav becomes a row.
- Breakpoint 2: `60em` (960px). The cards become 3 per row, and `grid-template-areas` puts the banner beside the menu, with the header and footer full width.
- Why these widths: ______________________________ (write what you saw while widening from 320px)

### Q3: Intrinsic grid
Cards use `repeat(auto-fit, minmax(220px, 1fr))` with no breakpoint.

| Width | Q2 columns | Q3 columns |
| --- | --- | --- |
| 390px | ___ | ___ |
| 768px | ___ | ___ |
| 1280px | ___ | ___ |

- **Needs a media query:** the nav (stack to row) and the banner/menu layout, because the design itself changes.
- **Does not need one:** the card grid, because only the number of cards per row changes.
- **Which works better:** ______________________________ (my choice was Q3 for the cards, because it needs less CSS and has no fixed widths)

## Part 2 summary

See `Part-2-Lighthouse-Audit-Fix/README.md`.