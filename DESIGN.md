---
version: "alpha"
name: "ayayai"

colors:
  primary: "#f5a623"
  bg: "#0f0f1a"
  surface: "#1a1a2e"
  text: "#e0e0e0"
  text-muted: "#999"
  blue: "#4fc3f7"
  green: "#81c784"
  yellow: "#ffd54f"
  red: "#e57373"

typography:
  base:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.5
    color: "{colors.text}"
  heading:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "1.15em"
    fontWeight: 700
    color: "{colors.accent}"
    letterSpacing: "0.5px"
  subheading:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "1em"
    fontWeight: 600
    color: "{colors.blue}"
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "0.75em"
    fontWeight: 400
    color: "{colors.text-faint}"
    letterSpacing: "1px"

spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "20px"
  xl: "32px"

rounded:
  sm: "4px"
  md: "6px"
  lg: "10px"
  full: "9999px"

components:
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg}"

  button-primary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: "{spacing.sm} {spacing.lg}"

  button-ghost:
    backgroundColor: "{colors.bg}"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.md}"
    padding: "{spacing.sm} {spacing.md}"

  badge-success:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.green}"
    rounded: "{rounded.sm}"
    padding: "2px {spacing.sm}"

  badge-danger:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.red}"
    rounded: "{rounded.sm}"
    padding: "2px {spacing.sm}"

  callout:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    padding: "{spacing.md}"

  header:
    backgroundColor: "{colors.surface}"
    padding: "{spacing.md} {spacing.lg}"
---

## Overview

ayayai is a family AI learning community led by Edgar. Dark-themed, warm amber accent. Built for non-technical audiences — warmth and clarity over complexity.

Projects under this system:
- **quiniela** — FIFA 2026 prediction tracker
- **neurofitness** — Parkinson's fitness companion (fitnessparkinson)
- **lessons** — Reveal.js slide decks for family sessions
- **plaza** — TBD

Tone: accessible, human, warm. Spanish-first content. Never cold or technical-looking.

## Colors

- `accent` (`#f5a623`) — amber gold. Primary CTA, headings, bullet markers, highlights. The brand color.
- `blue` (`#4fc3f7`) — secondary accent. Subheadings, info highlights, secondary interactive elements.
- `bg` (`#0f0f1a`) — deepest dark. Page backgrounds only.
- `surface` (`#1a1a2e`) — card/panel background. One level above bg.
- `border` — barely visible white. Separators, card outlines.
- `green` / `yellow` / `red` — status colors only (win/draw/loss in quiniela; good/warn/bad states).
- `text-faint` (`#666`) — metadata, nav hints, decorative labels.

Never use raw hex in new components — always reference tokens.

## Typography

System font stack everywhere. No web fonts — fast, native feel on all devices.

- Headings: amber (`accent`), bold, slight letter-spacing
- Subheadings: blue (`blue`), medium weight
- Body: `#e0e0e0`, 14px, 1.5 line-height
- Labels/metadata: `#666`, small caps style, 1px letter-spacing

## Layout

Mobile-first. Single column on small screens, max-width ~900px centered on desktop.
Sticky header pattern used across all apps.

## Elevation & Depth

Two-level system only:
1. `bg` (`#0f0f1a`) — base
2. `surface` (`#1a1a2e`) — elevated (cards, header, modals)

No shadows — depth via border + background difference.

## Shapes

Subtle rounding. `rounded.md` (6px) for buttons and badges. `rounded.lg` (10px) for cards. Never sharp (0px), never pill except truly circular actions.

## Components

### Card
Dark surface, thin border, 10px radius. Padding 20px. No shadow.

### Button (primary)
Amber ghost style — transparent amber background, amber border, amber text. On hover, slightly more opaque background. Never solid filled amber button (too harsh on dark bg).

### Callout / Quote block
Left amber border, subtle amber background tint, italic body text. Used for key takeaways in lessons.

### Badge
Green badge for positive states (correcto, ganó). Red for negative. Yellow for draws/neutral.

### Table
Header row: barely-there background, uppercase muted labels. Rows: no background, thin bottom border only.

## Do's and Don'ts

- DO use `accent` for exactly one focal element per screen — it must pop
- DO write Spanish-first UI labels (the audience is Spanish-speaking)
- DON'T add drop shadows — depth comes from the two-level bg/surface system
- DON'T use solid filled buttons — the amber ghost style is the standard
- DON'T use more than two accent colors on one screen (`accent` + `blue` max)
- DON'T use white text — use `text` (`#e0e0e0`) to stay soft on dark bg
