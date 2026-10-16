# Rogers & Garvie: About Page Restructure (Mockup)

Static HTML mockup of the proposed About section for https://www.rogersandgarvie.com/about/.
For dev handoff only. Not the production build.

## Pages (hash-routed in one file)

| Mock tab | Proposed URL | Contents |
|---|---|---|
| `#about` | `/about/` | Hub page. "Attorneys" section (Grant + Thomas feature cards linking to their pages, Kennedy inline), then "Staff" (Maggie, Madelyn) |
| `#grant` | `/about/grant-rogers/` | Grant Rogers bio page |
| `#thomas` | `/about/thomas-garvie/` | Thomas Garvie bio page |

## Build notes

- Attorneys/Staff split is the client's request, so the law clerk isn't presented as an attorney. Kennedy Templeton is an Associate Attorney and belongs under Attorneys.
- Bio pages need a WordPress template: headshot, sidebar (Education, Admitted to practice, Affiliations), bio body, Contact button, "Back to About Us," and a "Meet the Team" row.
- Add Person/Attorney schema to each attorney page (name, jobTitle, image, alumniOf, worksFor) and a unique title tag per page.
- The live "Contact Grant/Thomas" buttons are empty `mailto:` links. Point them at `/contact/`.
- Styling follows the live theme: rust `#8A461D`, cream `#FAF8F1`, Playfair Display / Merriweather / Arvo.

## Open items

- **Kennedy's bio is v1.** Grant sent an "Updated Bios.docx" with one edit to her bio. Get that file and swap in the new text.
- Headshots in `/images` are resized web copies (700px tall). Use the originals from Grant's email for production.

## Deploy

No build step. On Vercel: import the repo, Framework Preset "Other", leave build and output settings blank.
`vercel.json` sends `noindex, nofollow` so the mockup stays out of search.
