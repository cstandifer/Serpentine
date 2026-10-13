# Serpentine

<img width="322" height="514" alt="IMG_2604" src="https://github.com/user-attachments/assets/ca39763f-ad97-4016-965d-121ea832f5fc" />

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

## Serpentine 3D (big screen + phone controller)

`serpentine-3d.html` is the same game, levels and music, but you *are* the snake. It's built for a big screen, with your phone as the controller (`controller.html`).

- **Views**: Eye (from inside the snake's head), Chase (just above and behind), or Top (the original board). Press **C** or use the View button on the phone to switch. In the 3D views a minimap in the corner shows your tail.
- **Steering is smooth and analog**: the snake curves instead of making 90° turns. Tip the phone a little for a gentle curve, more for a tight one. Left and right mean *your* left and right.
- **Phone**: scan the QR code on the menu (or open `/controller.html` and type the 4-letter code). Tip the phone to steer, and **jump for real** to jump. The phone spots a jump from the push-off spike followed by a moment of near-weightlessness while you're in the air. Left, Jump and Right buttons are always there as a backup (hold Left or Right to keep turning), and a Sensitivity panel tunes how far you tip for a full turn and how big a jump needs to be.
- **Versus (2 players)**: pick any level and race for 60 seconds in one shared arena on a split screen. Each player gets 3 lives; crash into anything, including the other snake, and you lose a life and respawn a moment later. Highest score wins. Two phones can join the same code (first is Player 1, second is Player 2), or share a keyboard: A / D / W and ← / → / ↑.
- **Leaderboard**: a top 10 per difficulty, saved on the big screen. If a solo run makes the board, type your name on the phone or the keyboard.
- **Comet**: a fourth snake, about 25% faster, with a wider turning circle.
- **Keyboard**: hold ← → to steer, Space jumps, C changes view. In the top view, arrow keys point the snake toward that direction and it curves round to face it.

The phone and screen connect through [PeerJS](https://peerjs.com) (its free cloud server only handles the handshake; game data goes directly over WebRTC), so it still works as a static site. Phones only share motion sensors over **HTTPS**, so test the controller on the Render URL rather than a local `http://` address. Uses [three.js](https://threejs.org) for the 3D views; if it can't load, the game falls back to the top view.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

The repo includes a `render.yaml`, so Render can deploy it as a static site with no build step.
