# سرّ شجرة المانجو — Noah and the Mango Tree Mystery

An interactive Arabic children's story with mini-games, built for ages 5–10.
A **كان يا ما كان (Kan Ya Ma Kan)** story.
Scan the QR code printed in the book to open it on any phone browser — no app, no login.

**Live:** https://shiba3006.github.io/Mago_tree_game/

## The story

Every night the mangoes vanish from the golden mango tree, and nobody knows why.
Noah, a young detective with a magnifying glass, and Lulu the parrot follow the clues
and listen to every animal in the jungle — Fifi the elephant, Zizi the giraffe,
Coco the monkey and the sloth — until they discover the truth: hungry fruit bats
whose valley has dried up.

The reader chooses what Noah does next. The book has **3 happy endings** and a
"try again" page, plus fact pages about the animals. The lesson: a good detective
doesn't rush — collect the evidence first, and listen to everyone.

## What's inside

**📖 Read the story and choose your ending**
- Every page of the printed book, shown exactly as designed.
- Each choice in the book is a big tap button; endings award a collectible
  (🧺 💧 🤝) that is remembered on the device.
- Page-turn animation in the right-to-left reading direction; arrow keys on desktop.

**🎮 The Detective Noah game** (easy and hard modes)
1. **The magnifying glass**: drag the lens through the dark jungle to find 5 clues.
2. **Who ate the mango?**: use the clues to rule out each suspect.
3. **Night guard**: tap the hungry bats to give them mangoes, but not the owl or the butterflies.

**🏃 Run with Noah**: a one-tap runner game. Jump to catch mangoes and leap over rocks.

## Tech notes

- One self-contained `index.html` (~4.4 MB): plain HTML, CSS and JavaScript, no build step,
  no dependencies (Google Fonts is optional and falls back to system fonts offline).
- Story pages are rendered from the PDF with `pdftoppm`, resized to 1100 px and embedded
  as WebP data URIs (quality 76).
- Hash routing (`#menu`, `#story/N`, `#game`, `#runner`) so the phone's back button works.
- The runner game is embedded in a sandboxed `iframe` (srcdoc) so its styles never clash.
- Right-to-left and responsive for phones, tablets and laptops: side-by-side layouts on landscape screens
  (menu in two columns, story page beside its choices), larger text on big monitors, and the runner
  scaled up uniformly on large screens. Large tap targets; respects `prefers-reduced-motion`.
- Only data stored: found endings and chosen level, in `localStorage`. No tracking, no ads.
- Branding: the كان يا ما كان logo is embedded as the favicon, home-screen icon, loading splash and menu logo.
- `og-image.png` (1200×630) is the link-preview image for WhatsApp/Facebook; keep it in the repo root next to `index.html`.
- Hosting: GitHub Pages, from the repo root.

## Credits

- **Story & illustrations:** كان يا ما كان (Kan Ya Ma Kan)
- **Development:** [@Shiba3006](https://github.com/Shiba3006)
