# Midtown Pizzeria & Pub — Bill of Fare

A print-ready, four-page HTML menu for **Midtown Pizzeria & Pub** in Liberal, Kansas.
Designed in the style of a classic framed restaurant menu — warm cream paper,
barn-red category bars, muted gold dividers, dense organized columns,
and a brand-anchored cover page mirroring the Red Crow menu structure.

> **Fresh. Different. Better.** — 1,048,576 different pizza combinations.
> Right in the Heart of Good Times — Liberal, Kansas.

---

## Live preview

Once GitHub Pages is enabled on this repository, the menu is viewable at:

`https://mastellar.github.io/midtown-pizza-menu/`

---

## What's inside

| File | Purpose |
| --- | --- |
| `index.html` | The complete 4-page menu, semantic markup with `data-section` attributes |
| `styles.css` | All visual styling — typography, layout, page-break print rules |
| `assets/logo.png` | Midtown brand seal (the gold-on-barn-red circle) |
| `LICENSE` | MIT license |

The menu is **four US Letter portrait pages**:

1. **Cover** — Beverage menu (beer, wine, cocktails, signatures, non-alcoholic) flanking a centered Midtown brand block
2. **Pizzas** — The Magnificent 7, Specialty Pizzas, Build Your Own, Lunch Specials
3. **Pub Kitchen** — Appetizers, Wings, Sandwiches, Sliders, Pasta + By-the-Bucket family meals, Sweet Stuff, Sides & Drinks, plus a featured Fresh Salad Bar banner
4. **Calendar** — May 2026 events grid, "Why Midtown" callout, brand reinforcement

---

## How to print as PDF

1. Open `index.html` in any desktop browser (Chrome, Edge, Safari, Firefox).
2. Press `Cmd + P` (Mac) or `Ctrl + P` (Windows).
3. In the print dialog set:
   - **Destination:** Save as PDF
   - **Paper size:** US Letter (8.5 × 11 in)
   - **Layout:** Portrait
   - **Margins:** None or Minimum
   - **Background graphics:** ✅ ON  ← **critical**, otherwise red bars and colors won't print
4. Click **Save**.

You'll get a clean four-page PDF with one page per surface.

---

## Brand palette

| Token | Hex |
| --- | --- |
| Barn Red | `#7C0A01` |
| Bean | `#3D0C01` |
| Chinese Gold | `#CC9901` |
| Goldenrod | `#DAA520` |
| Black Chocolate | `#1B1811` |
| Warm Cream | `#F4E6C3` |
| Tabletop Brown | `#5D4432` |

---

## Typography

Loaded via Google Fonts:

- **Archivo Black** — page titles and big headers
- **League Spartan** — section headings, item names, small caps
- **Libre Baskerville** — italic descriptions and serif body
- **IBM Plex Mono** — tabular prices
- **Allura** — script accent for *Fresh. Different. Better.*
- **Pacifico**, **Lobster**, **Yellowtail**, **Dancing Script**, **Great Vibes** — alternative scripts wired in for easy swapping

---

## Customization

### Changing menu items, prices, or descriptions

All menu data lives directly in `index.html`. Find the section by its
`data-section` attribute — for example:

```html
<section data-section="magnificent-7"> ... </section>
<section data-section="appetizers"> ... </section>
<section data-section="wine-cocktails"> ... </section>
```

Each item row follows a consistent shape:

```html
<div class="item">
  <div class="item-name">Buffalo Chicken</div>
  <div class="item-price">$23.99</div>
  <div class="item-desc">Buffalo sauce, chicken, bleu cheese, ranch.</div>
</div>
```

For three-tier pizza pricing, use:

```html
<div class="item pizza">
  <div class="item-name">The Midtown</div>
  <div class="item-prices">
    <div class="tier"><span class="tier-label">SM</span><span class="tier-price">$19.99</span></div>
    <div class="tier"><span class="tier-label">MED</span><span class="tier-price">$21.99</span></div>
    <div class="tier"><span class="tier-label">LRG</span><span class="tier-price">$24.99</span></div>
  </div>
  <div class="item-desc">Pork belly, pulled pork, onions, cilantro, mango, balsamic glaze</div>
</div>
```

### Replacing the cover beverage filler

The cover page beer / wine / cocktail / signature drink lists are
clearly labeled as **placeholder filler** in the HTML and on the page itself:

> *Sample beverage layout — final beer, wine, cocktail, and signature drink list to be confirmed by Midtown bar.*

There is also a hidden HTML comment block at the bottom of the cover
section flagging every placeholder section. Replace those entries with
the confirmed Midtown beverage program when ready.

### Updating the calendar month

The calendar page (`data-section="calendar"`) currently shows **May 2026**
with no events listed. To roll the calendar to a new month:

1. Update `<h2 class="cal-month">` to the new month and year.
2. Adjust the day numbers in `.cal-cell` blocks so the grid matches the
   first day-of-week for that month (Sun – Sat columns).
3. Update or remove the `.cal-num.today` highlight to reflect today's date.

### Magnificent 7 and Specialty Pizzas (note)

The **April 2026 Menu Changes** memo from Midtown asked to *change* the
Magnificent 7 and Specialty Pizza lists, but did not provide replacement
items. Per project rules, the existing items from `MT Menu Back.pdf` were
retained verbatim. Hidden HTML comments mark the spots where the new
content should be dropped in.

---

## Project rules followed

- ✅ No invented menu items, prices, hours, events, or claims (cover beverage list is clearly marked as filler)
- ✅ All April 2026 menu changes applied (apps, wing sauces, sandwich service, fresh salad bar, pasta, by-the-bucket meals, sliders, desserts, side of tater tots)
- ✅ Citrus Yuzu Cheesecake removed from desserts
- ✅ Brand callouts on every page
- ✅ Print-ready with `@page` rules and `page-break-after: always`
- ✅ Semantic `data-section` attributes for every category

---

## License

MIT. See `LICENSE`.
