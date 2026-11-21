# Part 2: Lighthouse Audit and Fix (Q4 and Q5)

Goal: audit a deliberately broken responsive page with Lighthouse, fix it, and reach a
**mobile score of 80+** in every category.

## How I ran Lighthouse

- Browser: Chrome ___ (version) in an **Incognito** window
- Mode: **Mobile**, categories: Performance, Accessibility, Best Practices, SEO
- Page served with Live Server at `127.0.0.1`
- Date: ___

## Q4: The broken page (`Q4-Broken-Starter/`)

### The five flaws

| # | Flaw | Where | Why it breaks mobile |
| --- | --- | --- | --- |
| 1 | No viewport meta tag | `index.html`, `<head>` | The phone shows a zoomed-out desktop page |
| 2 | Fixed-width container | `style.css`: `.container { width: 1200px; }` | The page is wider than the screen and scrolls sideways |
| 3 | Fixed-width banner image | `style.css`: `.banner img { width: 1000px; }` | The image overflows the screen |
| 4 | Tiny, low-contrast text | `style.css`: `font-size: 12px; color: #aaaaaa;` and `.price { color: #bbbbbb; }` | Hard to read, fails the contrast check |
| 5 | Tiny tap targets | `style.css`: `.nav a { padding: 2px; margin-right: 4px; }` | Links are too small and too close to tap |

### Before scores (Q4)

| Category | Score |
| --- | --- |
| Performance | ___ |
| Accessibility | ___ |
| Best Practices | ___ |
| SEO | ___ |

### Flagged audits, linked to the code

| Audit Lighthouse flagged (copy the name from your report) | Caused by | File and line |
| --- | --- | --- |
| ___ | Flaw ___ | `___` |
| ___ | Flaw ___ | `___` |
| ___ | Flaw ___ | `___` |

### What breaks at 390px

______________________________ (for example: the page scrolls sideways, the banner image is cut off, the text is hard to read)

Screenshot: `screenshots/q4-lighthouse-before.png`

## Q5: The fixed page (`Q5-Fixed/`)

### Fixes applied

| # | Fix | Change |
| --- | --- | --- |
| 1 | Viewport meta tag | `<meta name="viewport" content="width=device-width, initial-scale=1">` |
| 2 | Container | `width: 90%; max-width: 75rem;` instead of `width: 1200px` |
| 3 | Images | `max-width: 100%; height: auto;` instead of a fixed 1000px |
| 4 | Text | `font-size: 1rem` and `color: #1f2937` (high contrast) |
| 5 | Nav links | `padding: .875rem 1rem` and full-width links |

Extra performance and best-practice changes: small compressed JPEGs, `width` and `height` on every image, `fetchpriority="high"` on the banner image, `loading="lazy"` on the card images, and an empty favicon link so the browser doesn't log a 404.

### Before and after scores

| Category | Before (Q4) | After (Q5) | What improved it |
| --- | --- | --- | --- |
| Performance | ___ | ___ | ___ |
| Accessibility | ___ | ___ | ___ |
| Best Practices | ___ | ___ | ___ |
| SEO | ___ | ___ | ___ |

Screenshot: `screenshots/q5-lighthouse-after.png`

### Responsive checks on the fixed page

- [ ] 320px: no horizontal scrolling
- [ ] 768px
- [ ] 1440px

## Git and pull request

- Q1 to Q4 committed on `main`.
- Q5 committed on the branch `fix/mobile-responsive` and merged through a pull request.
- Pull request: ___ (paste the link)

## Reflection

A high Lighthouse score is evidence that the page passes a set of automated checks on a simulated device, not proof that it works well for every real user on every real device.