# Science Explorers

**Multi-grade:** the home page now has a **grade picker (Grades 1–5)**, built to the AERO/NGSS standards.
**All five grades (1–5) are now complete** — 58 lessons in total:
- **Grade 1** (4 units): Light & Sound, Plant & Animal Parts, Parents & Their Young, Patterns in the Sky
- **Grade 2** (4 units): Materials, Plants & Pollinators, Habitats, Earth Changes
- **Grade 3** (4 units): Forces & Motion, Life Cycles & Traits, Survival & Adaptations, Weather & Climate
- **Grade 4** (5 units): Energy, Waves & Information, Structures & Senses, Earth Surface & History, Natural Resources & Hazards
- **Grade 5** (6 units): Matter, Forces, Energy, Organisms, Ecosystems, Earth's Interactions

Each grade's units live in its own array (`GRADE1`…`GRADE4`, plus `UNITS` for Grade 5). Sort/classify activities shuffle their items so the answer order is not a giveaway; every slide has a Back button.

A Grade 5 science teaching website by **Deenish Ramdial** — one self-contained page with
interactive 5E lessons, printable Bronze/Silver/Gold worksheets, vocabulary flip-cards and
quick-check quizzes.

**Live site:** https://sunsun20.github.io/science-explorers/

## Units
1. **Matter: Properties and Interactions** — live (Standards 1, 2, 4 & 5)
2. **Forces** (Gravity) — live
3. **Energy** (Energy from the Sun) — live
4. **Organisms and Processes** (plants need air & water) — live
5. **Ecosystems and Sustainability** (food webs, decomposers, protecting nature) — live
6. **Earth's Interactions** (Earth's four systems, the water cycle, where water is) — live

All 6 Grade 5 units are now live.

## How to change things

Everything is in **one file: `index.html`**. Open it in any text editor — no install, no build step.
To preview your edits, just double-click `index.html` to open it in a web browser.

Where to look inside the `<script>`:

| What you want to change | Where it is |
|---|---|
| Lesson content (objective, success criteria, slides, tasks, assessment) | the data arrays `MATTER_S1`, `MATTER_S2`, `MATTER_S4`, `MATTER_S5`, `FORCES`, `ENERGY`, `ORGANISMS`, `ECOSYSTEMS` |
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
