# Rebecca Kraft — Editorial Photography Site

A hand-coded, editorial-style site in plain HTML/CSS/JS. No build step, no framework, no dependencies — just open `index.html` and it works.

## Files
- `index.html` — Home / front page (hero, services, selected work, CTA)
- `about.html` — About Me (your original bio content, refined)
- `portfolio.html` — Full portfolio with category filters, mini-doc feature, digital + film galleries
- `contact.html` — Contact info + inquiry form
- `styles.css` — All styling (one stylesheet, CSS variables at the top)
- `script.js` — Mobile menu, portfolio filter, form stub, scroll reveals

## Design system (all at the top of `styles.css`)
- **Palette:** warm cream `#F5F0E6`, deep ink `#1C1814`, rust accent `#8B3A1E`
- **Type:** Cormorant Garamond (display) + Inter (UI), loaded from Google Fonts
- Edit the `:root` variables to re-skin the whole site at once.

## Customizing

### Replacing photos
The site currently pulls images from the original Wix URLs so it works out of the box. For production, download the photos and put them in an `/images` folder, then replace the `src=` attributes in the HTML files (search for `wixstatic.com`).

### Changing the text
All copy lives in the `.html` files as plain text — no JS templating, no CMS. Edit directly.

### The contact form
Currently the form submits client-side only (it just resets and shows a thank-you note). To actually receive submissions, point it at:
- **Formspree** (easiest): change `<form id="contactForm">` to `<form id="contactForm" action="https://formspree.io/f/YOUR_ID" method="POST">` and remove the JS stub.
- **Netlify Forms**: if hosting on Netlify, add `netlify` attribute to the form tag.
- **Your own backend**: replace the `fetch` comment in `script.js`.

### Deploying
Drop all files into any static host — Netlify, Vercel, GitHub Pages, Cloudflare Pages. All free. No build command needed.

## Notes
- Fully responsive down to mobile
- Hover effects and reveal animations built in
- Accessible nav (keyboard navigable, aria-expanded on mobile toggle)
- All external links open in new tabs with `rel="noopener"`
