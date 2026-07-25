# curso02ay — ayayai Season 2

ayayai is Edgar's technology and AI program for family and friends: we learn together, nobody gets left behind. Season 2 centers on **Claude Code**.

## Format
- Group session on Zoom, Saturdays 11am Chicago time, recorded. Day/time shifts week to week with Edgar's and participants' availability.
- Individual sessions per person, scheduled by project and availability.
- No fixed number of weeks — the course runs open-ended.
- Attendance is never 100%. Plan each session to stand alone; assume someone missed the previous one.
- Edgar sends invitations and reminders by WhatsApp: the ayayai group plus three family groups.

11am Chicago = 12pm Venezuela, 1pm Argentina, 6pm Barcelona (summer). Barcelona is the hard one — Sebastian is expected at some sessions only.

## Participants

| Person | Location | Project |
|--------|----------|---------|
| Edgar (creator) | Chicago, US | Planetario3 (working name) — business helping small companies with technology |
| Nersy | Venezuela — needs VPN | Parkinson's fitness: marketing, exercise videos, neuroplasticity guides, neuroplasticity app |
| Zenaida | Venezuela — needs VPN | Marketing for her nursing Instagram channel @tuenfermera.val |
| Sebastian | Barcelona, Spain | Project/process manager agents for a car seat factory. Attends some sessions |
| Elvira | Argentina | Launch her business, Elvisness |
| Olga | Florida, US | No project yet |
| Carlos | Florida, US | No project yet |

## Language
- Everything shown to participants: **Spanish**. No exceptions.
- Edgar's own notes and internal files: English.
- All participants are Venezuelan — Venezuelan Spanish and local expressions are welcome, not "neutral" Spanish.

## Working rules
- Venezuela (Nersy, Zenaida): cover VPN and Anthropic access before any tooling step. Without it nothing else works.
- Tie every exercise to that person's own project, not generic demos.
- Audience is non-technical: simple, visual, example-driven.

## Session 1 — Saturday 2026-07-25, 11am Chicago, Zoom
1. Sign up for the paid Claude plan (US$22).
2. Install VPN — Venezuela participants.
3. Install Claude Code.
4. Explain a few terminal commands and a few Claude Code commands.

## Folder layout
```
ayayai/                    repo boadaedgar/ayayailessons — PUBLIC
  index.html               landing page
  curso02ay/
    index.html             season 2 hub
    archivo-temporada-1.html
    sesiones/              one page per session
    guidesmix/             all guides and lessons, season 1 and 2
    neurofitness/          Nersy: Parkinson's app + Gumroad assets
    enfermeria/ elvisness/ aiforvenezuela/ learningtools/ elclon/
                           local workspace stubs, not in git
```

## This repo is public — what does NOT belong here

Published via GitHub Pages (`.nojekyll` at repo root), so everything committed
is world-readable. Before adding anything, ask: **what happens if this becomes
public tomorrow?** If the answer isn't "nothing", it goes in a private repo.

| Content | Goes to |
|---|---|
| Participant work with real data (Sebastián's factory files) | `ayayai-privado` — private, at `claude/ayayai-privado/` |
| Edgar's personal projects | Their own private repos |
| Session records, project status | Notion |
| Edgar's ideas and frameworks | Obsidian vault |

Never `git add -A` here — stage paths explicitly. A blanket add is what nearly
published `creators/` and `xfreezer/`.

## Links and archiving

Moving or renaming any HTML file changes its public URL and breaks links already
sent over WhatsApp. **Files never move.** Archiving means removing the link from
the season index and listing it in `archivo-temporada-1.html` instead.

At the end of a season: `git tag temporada-N-final && git push --tags`. That tag
is how retired material is recovered later (`git show temporada-1-final:path`).
