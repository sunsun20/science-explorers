# Science Explorers

A Grade 5 science teaching website by **Deenish Ramdial** — one self-contained page with
interactive 5E lessons, printable Bronze/Silver/Gold worksheets, vocabulary flip-cards and
quick-check quizzes.

**Live site:** https://sunsun20.github.io/science-explorers/

## Units
1. **Matter: Properties and Interactions** — live (Standards 1 & 2)
2. **Forces** (Gravity) — live
3. **Energy** (Energy from the Sun) — live
4–7. Sound Waves · Organisms · Ecosystems · Earth's Interactions — coming soon

## How to change things

Everything is in **one file: `index.html`**. Open it in any text editor — no install, no build step.
To preview your edits, just double-click `index.html` to open it in a web browser.

Where to look inside the `<script>`:

| What you want to change | Where it is |
|---|---|
| Lesson content (objective, success criteria, slides, tasks, assessment) | the data arrays `MATTER_S1`, `MATTER_S2`, `FORCES`, `ENERGY` |
| Quiz questions (10 per lesson) | `window.MCQS_EXTRA` (Lesson 1 of Matter uses `mcqs`) |
| Each unit's colour theme | the `THEME` map |
| Pictures (realistic SVG icons) | the `ICONS` object — use a picture in text by writing `[[name]]` |
| The home welcome message | the `vHome()` function |
| Printable resource cards | the `RESOURCES` object |

Each lesson object looks like:

```js
{
  id, title, grade,
  lo: 'We are learning to …',        // learning objective
  sc: [{ band: 'Remembering', items: ['I can …'] }, …],
  vocab: ['Solid', 'Liquid', …],
  slides: [{ tag, h, body }, …],     // 6 slides: Engage, Explore, Explain, AFL, Elaborate, Evaluate
  tasks: { bronze, silver, gold, gt },
  assessment: { title, items, check }
}
```

## Fonts
`fonts/` holds the Comic Neue web font so the page looks the same even offline.
