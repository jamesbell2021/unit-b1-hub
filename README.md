# Unit B1 — Personal Progression (Hub)

A single self-contained HTML page that ties your whole B1 toolkit together: why the unit exists, every deliverable and why it matters, a live arcade linking out to your six practice tools, the AC1–AC5 grading criteria explorer, the Northern Ireland local scene, and a searchable glossary. Neo-brutalist paper theme, chiptune audio synthesised live via the Web Audio API — no external audio files, works offline once loaded.

**Live site:** https://jamesbell2021.github.io/unit-b1-hub/

## What's on the page

- **01 Why** — the honest pitch for why the unit matters, with the same "two years to Gamescom" and "45 seconds" hooks as the standalone version.
- **02 What you're making** — twelve expandable deliverable cards. Six of them now carry a **"▶ Practice in…"** button straight through to the matching standalone tool.
- **03 Your toolkit ("the arcade")** — six practice tools as arcade-cabinet cards, each linking out to its own live GitHub Pages app:

  | Tool | Covers | Live at |
  |---|---|---|
  | 🕹️ Press Start Britain | AC1 | [press-start-britain](https://jamesbell2021.github.io/press-start-britain/) |
  | 💰 RESPAWN | AC1 · AC2 | [bmet-respawn](https://jamesbell2021.github.io/bmet-respawn/) |
  | 🎬 Breaking In | AC2 · AC3 | [bmet-breaking-in](https://jamesbell2021.github.io/bmet-breaking-in/) |
  | 📄 The CV | AC3 | [bmet-the-cv](https://jamesbell2021.github.io/bmet-the-cv/) |
  | 🎙️ Interview Techniques | AC5 | [bmet-interview-techniques](https://jamesbell2021.github.io/bmet-interview-techniques/) |
  | 🗺️ The Roadmap | AC2 | [bmet-five-year-plan](https://jamesbell2021.github.io/bmet-five-year-plan/) |
  | 🎓 UCAS Decoded | AC1 | [unit-b1-hub/ucas](https://jamesbell2021.github.io/unit-b1-hub/ucas/) |
  | ✉️ Make Your Case | AC3 · AC5 | [unit-b1-hub/statements](https://jamesbell2021.github.io/unit-b1-hub/statements/) |

  **Note:** UCAS Decoded and Make Your Case live *inside this repo* at `ucas/` and `statements/`, not in their own repositories, so their toolkit links are relative paths (`./ucas/`, `./statements/`) rather than absolute URLs. If it is ever moved to a standalone repo, update that `url` value in `TOOLS` to match the others.

- **04 The five criteria** — all five ACs with a Pass/Merit/Distinction toggle showing the same evidence graded at three levels.
- **05 The local scene** — nine Northern Ireland studios, two local (non-games) entrepreneurs included specifically as a traceable alternative to "I admire Elon Musk," and four funding/support bodies, tied to an explicit AC1 task.
- **06 Glossary** — around 70 searchable, filterable terms.

## UCAS Decoded (`ucas/`)

Covers the *College and UCAS research* deliverable for AC1. Seven sections: what UCAS is and isn't, an interactive route decider (UCAS vs direct application), the six application steps, the 2027 entry timeline, a BTEC-grade-to-tariff-points calculator, the B1 research task with a weak-vs-strong worked example, and a 20-term glossary.

The teaching point students most often get wrong: **not every course goes through UCAS.** The app uses their own course code (`P00175-AE`) to show that a Belfast Met code is not a UCAS code, and that they already made a direct application without ever touching UCAS.

**Accuracy:** dates, the £34.50 application fee and the tariff values were taken from [ucas.com](https://www.ucas.com/applying/applying-to-university/dates-and-deadlines-for-uni-applications) in October 2026 and change between cycles. Before reusing in a later year, check the equal consideration deadline, the fee, and the `GRADES` array in `ucas/index.html`.

## Make Your Case (`statements/`)

Covers the *personal statement and cover letter* deliverable (AC3, AC5) and supports the real application (AC4). Seven sections: the three documents people confuse (UCAS statement, CV profile, cover letter) with a sorting quiz; the three-question UCAS format; cover letter structure; a weak-vs-strong openings quiz; a builder with live mechanical checks (cliché detector, named recipient, evidence, character counts for UCAS); a real application; and a glossary. Work is kept in the browser's localStorage only; nothing is uploaded.

**Section 06 is configurable.** The `PLAYTEST` object at the top of the script in `statements/index.html` holds the real application (currently playtester recruitment for *Forged in Formation*, addressed to James Bell at 3BL). Edit the recipient, how to submit, and what it counts towards, or swap the whole application.

**Accuracy:** the UCAS format (three questions, 350-character minimum per answer, 4,000 total) was checked against [Queen's University Belfast](https://hecate.qub.ac.uk/home/student-blog/applying/ucas-personal-statement.html) and ucas.com in October 2026. Check ucas.com before reuse in a later cycle.

## The Roadmap's link back here

[bmet-five-year-plan](https://jamesbell2021.github.io/bmet-five-year-plan/) has a small "← Unit B1 hub" button in its top-left corner pointing at `../unit-b1-hub/`. That now resolves correctly, since this repo and that one are both top-level GitHub Pages projects under the same account.

## If a tool moves or gets renamed

The six toolkit links (`TOOLS`, near the top of the `<script>` block) and the deliverable "Practice in…" links (`tools:` arrays inside `DLV`) are plain URLs — search for either and update the `url` values.

## Running it

No build step, no dependencies beyond three Google Fonts.

- **Online:** use the GitHub Pages link above.
- **Offline:** download `index.html` and open it in any browser.

## A note on the source file

Fixed the same paste-encoding issue as the rest of this toolkit. This file also carried six emoji icons for the toolkit cards; five decoded back to their exact original codepoints from the surviving bytes (🕹️ joystick, 💰 money bag, 🎬 clapper board, 🎙️ microphone, 🗺️ world map). The sixth, for "The CV," lost every distinguishing byte and was chosen from context as 📄 (page) — worth a quick check.

---

🤖 Built with [Claude Code](https://claude.com/claude-code)
