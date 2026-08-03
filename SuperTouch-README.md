# SuperTouch

A Megatouch-style bundle of classic bar arcade mini-games, all recreated
as single self-contained HTML pages, part of the marcitech.is-a.dev
arcade cabinet.

## Games included

| Page | Game |
|---|---|
| `SuperTouch.html` | Main cabinet menu / launcher |
| `11rounds.html` | 11 Ball billiards puzzle (canvas physics) |
| `squares.html` | SameGame-style tile-clearing puzzle |
| `tripillars.html` | Tri Pillars solitaire (scoring, streaks, leaderboard) |
| `photofind.html` / `loadphotofind.html` | Photo Hunt-style spot-the-difference |

## Shared features

- Shared sound effects (`fx/`) and helper scripts (`sfx.js`, `js/main.js`,
  `js/answers.js`) used across the individual games
- `localStorage`-backed leaderboards where applicable
- Bootstrap + animate.css for shared UI chrome (`css/`)
- Links out to the shared arcade wallet (`../wallet/index.html`)

## Structure

```
SuperTouch-main/
├── index.html        # cabinet entry point
├── SuperTouch.html    # cabinet menu
├── 11rounds.html
├── squares.html
├── tripillars.html
├── photofind.html
├── loadphotofind.html
├── sfx.js
├── fx/                # sound effects (ticking, correct/wrong, boosts, etc.)
├── css/               # bootstrap.min.css, animate.css, style.css
└── js/                # main.js, answers.js
```

## Running locally

Serve the folder (audio and cross-game/wallet links assume same-origin
hosting):

```bash
python -m http.server
```

Then visit `http://localhost:8000/index.html`.
