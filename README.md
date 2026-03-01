# MyShop - Product Page

## What is this?
A simple product listing page for a simulated shop called MyShop. The project was handed to me with several bugs and accessibility issues that I had to find, fix and document.

## Files
- `index.html` - The main page structure
- `styles.css` - All the styling
- `script.js` - Handles the cart and newsletter interactions

## What I fixed

### Accessibility
- Added alt text to all images
- Replaced divs with semantic HTML like `header`, `nav`, `main` and `footer`
- Added labels to form inputs
- Changed div/a buttons to real `button` elements
- Added ARIA labels where needed
- Fixed color contrast to meet WCAG AA
- Removed `outline: none` so keyboard navigation works
- Fixed heading order (h1 → h2 on product cards)
- Added `lang="en"` and meta tags

### Performance (LCP)
- Added `width` and `height` on all images
- Added `fetchpriority="high"` on the hero image
- Added `loading="lazy"` on product images
- Removed a blocking busy-loop in script.js
- Added `defer` to the script tag

## LCP Results
| | Chrome | Firefox |
|---|---|---|
| Before | 0.40s | 0.50s |
| After | 0.228s | 0.057s |
| Improvement | ~43% | ~89% |

## Accessibility Testing (axe-core)
| | Before | After |
|---|---|---|
| Violations | 5 | 0 |
| Passes | 15 | 34 |