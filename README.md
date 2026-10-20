# Space Invaders

A Space Invaders clone built with TypeScript + Vite, using React purely as the renderer.

```bash
npm install
npm run dev
```

## Controls

| Key              | Action          |
| ---------------- | --------------- |
| ← / → (or A / D) | Move            |
| Space (or ↑ / W) | Fire            |
| P / Esc          | Pause           |
| Enter            | Start / restart |

## Structure

- `src/game/` – framework-free engine: state, `update(state, input, dt)`, collisions, sprites as pixel bitmaps.
- `src/components/GameView.tsx` – pure render of the state as SVG at the original 224×256 resolution.
- `src/App.tsx` – `requestAnimationFrame` loop + keyboard input; re-renders once per frame.

Features: 5×11 formation that speeds up as it thins, bottom-row-only alien fire, erodible shields,
mystery UFO, extra life at 1500, increasingly lower/faster waves, hi-score saved in `localStorage`.

## Scripts

- `npm run lint` – ESLint (typescript-eslint, react-hooks, react-refresh; Prettier-compatible)
- `npm run format` / `npm run format:check` – Prettier
