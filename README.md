# Executive Tiling — Website

A fast, premium, multi-page website built with plain HTML, CSS and JavaScript.
No frameworks, no build step. Open `index.html` in a browser or upload the whole
folder to any host.

---

## Editing content (the easy part)

**Almost everything you'll want to change lives in one file:**

```
content/site-content.js
```

Open it in any text editor. It's plain, commented, and you change the text
between the quote marks. Updating it here updates every page automatically.

What you can edit there:

| Want to change…              | Edit this in `site-content.js`        |
|------------------------------|---------------------------------------|
| Phone number                 | `business.phoneDisplay` **and** `business.phoneDial` |
| Email                        | `business.email`                      |
| Service area / hours         | `business.serviceArea`, `business.hours` |
| Menu links                   | `nav`                                 |
| Services (add/remove/reword) | `services`                            |
| Gallery photos               | `gallery`                             |
| Reviews                      | `testimonials`                        |
| Stats / numbers              | `stats`                               |
| Form dropdown options        | `formOptions`                         |
| Footer text                  | `footer`                              |

> **Phone number:** change it in **two** places — `phoneDisplay` (what people
> see, e.g. `021 234 5678`) and `phoneDial` (what the Call button dials, no
> spaces, e.g. `+6421234567`).

The page **headlines and intro paragraphs** live directly in the `.html` files
(e.g. the big hero line on `index.html`). Open the file and edit the text.

---

## Using your own photos

1. Drop your images into `images/gallery/` (and `images/hero/`, `images/services/`).
2. In `content/site-content.js`, point an entry at your file, e.g.:

   ```js
   { title: "Ensuite, Fendalton", tag: "bathrooms", image: "images/gallery/ensuite-01.jpg" },
   ```

The placeholder photos currently use Unsplash URLs so the site looks complete
from day one. Swap them for real project photos whenever you're ready. Good
sizes: gallery ~1200px wide, hero/banners ~2000px wide, keep files under ~400KB.

---

## The quote form

The form validates the required fields, then opens the visitor's email app with
all the details filled in, addressed to your `business.email`. File attachments
(plans/photos) are added by the visitor in that email.

This works on any static host with nothing to configure. If you later want
submissions to arrive automatically without the email step (and capture file
uploads directly), connect the form to a free service like **Formspree** or
**Netlify Forms** — happy to set that up when you're ready.

---

## Pages

```
index.html          Home
about.html          About
services.html       Services
gallery.html        Projects / gallery
testimonials.html   Reviews
contact.html        Contact / quote
```

```
css/styles.css      All styling (colours, type, layout)
js/main.js          Builds the shared header/footer + interactions
content/            site-content.js  ← edit me
images/             logo + your photos
```

Brand colours are defined at the top of `css/styles.css` under `:root` if you
ever want to tweak the palette.

---

## Going live

Upload the **whole folder** to any host — Netlify, Cloudflare Pages, Vercel,
GitHub Pages, or traditional cPanel/FTP hosting. No server or database needed.
For a custom domain (e.g. executivetiling.co.nz), point the domain at your host
and you're live.

**Before launch, replace the placeholders:** phone number, email, and the
Unsplash photos with your own. Search the project for `executivetiling.co.nz`
to update the canonical/SEO URLs to your real domain.
