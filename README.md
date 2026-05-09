# Memyrinth ⚡

Navigate a shifting labyrinth of numbers, patterns, and collisions where memory itself is constantly in motion.

A multilingual memory game showcasing the French Multilingual programming language compiled to browser-based reactive UI.

## Features

- **5 Progressive Difficulty Levels** — From 4×4 grids to 6×6 with escalating mechanics
- **Board Rotation** — Levels 3+ feature rotating game boards that shift every few matches
- **Collision Effects** — Cosmetic particle effects on incorrect matches (Levels 4+)
- **Bilingual Support** — Automatic English/French detection with manual language toggle
- **Dark Cyberpunk Theme** — Neon glowing cards, smooth animations, futuristic aesthetics
- **Responsive Design** — Plays on desktop, tablet, and mobile

## Game Levels

| Level | Grid | Cards | Pairs | Mechanics |
|-------|------|-------|-------|-----------|
| **1** | 4×4 | 16 | 8 | Classic matching |
| **2** | 5×4 | 20 | 10 | Increased complexity |
| **3** | 6×4 | 24 | 12 | Board rotates every 3 matches |
| **4** | 6×5 | 30 | 15 | Rotation + collision effects |
| **5** | 6×6 | 36 | 18 | Maximum chaos, all mechanics |

## How to Play

1. **Click cards** to reveal their numbers
2. **Find matching pairs** — when you match a pair, they lock in place
3. **Earn points** — 10 points per successful match, –1 per incorrect
4. **Master the rotation** — starting at Level 3, the board rotates 90° periodically, shifting card positions
5. **Watch for collisions** — wrong matches trigger neon collision effects (visual only)
6. **Complete all levels** to master the Memyrinth

## Technical Stack

- **Source**: `memyrinth_fr.multi` — Game logic written in French Multilingual keywords
- **Compiled to**: JavaScript reactive UI bundle via `build-ui-bundle`
- **Frontend**: Custom bilingual HTML with cyberpunk CSS
- **Deployment**: GitHub Pages (automatic via GitHub Actions)
- **Framework**: Multilingual Programming Language (https://github.com/multilingualprogramming/multilingual)

### Build Command

```bash
python -m multilingualprogramming build-ui-bundle memyrinth_fr.multi --lang fr --out-dir _build
```

This compiles the French Multilingual source to `bundle.js`, which is loaded by the custom `index.html`.

## Running Locally

### Requirements
- Python 3.12+
- `multilingualprogramming` package

### Setup

```bash
# Clone the multilingual package
git clone https://github.com/multilingualprogramming/multilingual.git
cd multilingual
pip install -e ".[wasm]"
cd ../
git clone https://github.com/multilingualprogramming/Memyrinth.git
cd Memyrinth

# Build the game
python -m multilingualprogramming build-ui-bundle memyrinth_fr.multi --lang fr --out-dir _build
cp _build/bundle.js bundle.js

# Serve locally
python -m http.server 8000
# Open http://localhost:8000 in your browser
```

## Project Structure

```
.
├── memyrinth_fr.multi          # Game source (French Multilingual)
├── index.html                  # Bilingual cyberpunk UI wrapper
├── bundle.js                   # Compiled JavaScript (generated)
├── .github/workflows/build.yml # CI/CD pipeline
└── README.md
```

## Language Support

The game automatically detects your browser's language:
- **French** (`fr-*`) → Displays in French
- **Other** → Defaults to English

Use the **EN/FR** buttons in the top-right to manually toggle languages.

## Features Showcase

### Multilingual Implementation

The entire game logic is written in **French Multilingual** keywords:
- `observer var` — reactive state management
- `asynchrone déf` — async handlers
- `si/sinon si/sinon` — conditional logic
- `pour … dans intervalle()` — loops
- `attendre asyncio.sleep()` — async delays
- `rendre:` — reactive UI rendering

This demonstrates the Multilingual framework's capability to handle complex, interactive applications in non-English languages.

### Cyberpunk Aesthetics

- **Colors**: Dark background (#050510), neon cyan (#00ffff), neon green (#00ff88), magenta (#ff00ff), neon red (#ff0044)
- **Typography**: Monospace font with letter-spacing for futuristic feel
- **Animations**: 3D card flips, glowing effects, rotation transitions, collision bursts
- **Responsiveness**: Adapts to any screen size

## Deployment

Automatic deployment to GitHub Pages happens on every push to `main`:

1. GitHub Actions builds the game bundle from `memyrinth_fr.multi`
2. Uploads `index.html` + `bundle.js` to Pages
3. Live at: **https://[username].github.io/Memyrinth**

## License

GPL-3.0-or-later

## Credits

Built with the [Multilingual Programming Language](https://github.com/johnsamuelwrites/multilingual) to showcase French language support and reactive UI capabilities.
