# Serpentine

<img width="1290" height="2056" alt="IMG_2604" src="https://github.com/user-attachments/assets/ca39763f-ad97-4016-965d-121ea832f5fc" />

A rhythm snake game that mixes *Dancing Line* with *Snake*. It's one HTML file with no build step and no dependencies beyond Google Fonts.

## How to play

- **Drag** (or use the arrow keys / WASD) to turn.
- **Tap** (or press Space) to jump over low teal hurdles. Rose pillars and walls can't be jumped.
- Eat gems to grow and to reach each level's gem goal. Don't run into your own tail.
- You get 3 lives per run. A crash restarts the level; lose them all and the run is over.

## Levels

| Level | Name | Gem goal | Music |
|---|---|---|---|
| 1 | Open Floor | 12 | Lo-fi |
| 2 | Four Pillars | 16 | Synthwave |
| 3 | Corridors | 20 | Chiptune |
| 4 | Rooms | 24 | Drum & bass |
| 5 | Gauntlet | 30 | Techno |

## Snakes

- **Classic**: balanced.
- **Glider**: jumps twice as far and clears pillars, but grows faster.
- **Magnet**: pulls in nearby gems, then recharges for 3 seconds. Shorter jumps.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

The repo includes a `render.yaml`, so Render can deploy it as a static site with no build step.
