# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install       # install dependencies
npm run dev       # start dev server at http://localhost:3000 (auto-opens browser)
npm run build     # production build → build/ directory (not dist/)
```

There is no test runner or lint script configured.

## Architecture

This is a single-page React 18 + TypeScript app built with Vite (SWC). All game logic lives in [src/App.tsx](src/App.tsx).

**Game mechanics:**
- 3 treasure chests, one randomly assigned `hasTreasure: true` on each game init
- Clicking a chest opens it: +$100 for treasure, -$50 for skeleton
- Game ends when the treasure chest is opened OR all chests are opened
- State: `boxes: Box[]`, `score: number`, `gameEnded: boolean`

**Audio assets** (`src/audios/`): `chest_open.mp3` for treasure, `chest_open_with_evil_laugh.mp3` for skeleton — these are imported in App.tsx but audio playback is not yet wired up.

**UI components** in `src/components/ui/` are shadcn/ui components built on Radix UI primitives — treat them as library code, not game logic.

**Path alias**: `@` resolves to `src/` (configured in [vite.config.ts](vite.config.ts)).

**Animations** use `motion/react` (the Motion library, not `framer-motion` — import from `motion/react`).

**Styling** uses Tailwind CSS with an amber/treasure theme. Global styles are in [src/styles/globals.css](src/styles/globals.css).
