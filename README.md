# 🔐 The Enigma Vault — A CSP Treasure Hunt

A small desktop game built with Python's Tkinter where you unlock 8 doors by solving
constraint-satisfaction-style puzzles (sequences, arrangements, ciphers, logic grids)
to find the hidden treasure.

## Features

- 8 hand-crafted logic puzzles, each modeled as a small constraint satisfaction problem
- Hints (3 per playthrough) and a "See Solution" reveal for every level
- Player name entry (dropdown remembers past players)
- Persistent leaderboard (`leaderboard.json`) showing everyone's scores, ranked
- Simple to edit — every puzzle is just a dictionary entry, no other code changes needed

## Requirements

- Python 3.8+
- Tkinter (bundled with most Python installs; on Linux you may need `sudo apt install python3-tk`)

No external pip packages are required.

## How to Run

```bash
python main.py
```

## How to Play

1. Click **START GAME** and enter your name (or pick one from the dropdown).
2. Solve each puzzle to unlock its door — solving Level *N* unlocks Level *N+1*.
3. Use **HINT** if you're stuck (3 hints total).
4. Use **SEE SOLUTION** to reveal the full worked-out answer for a level.
5. Unlock all 8 doors to find the treasure and save your score to the leaderboard.
6. Check **LEADERBOARD** from the home screen anytime to see top scores.

## Editing Puzzles

All puzzles live in the `LEVELS` list near the top of `main.py`. Each level is a
dictionary with:

```python
{
    "title": "LEVEL 1 • NUMBER PATTERN",
    "text": "Complete the sequence: 2, 4, 8, 16, ?, ?",
    "answer": "32,64",          # or a list of accepted answers, e.g. ["3,5,7", "9,5,1"]
    "hint": "Each number is multiplied by 2.",
    "solution": "32, 64\n\nEach term doubles the previous one..."
}
```

To change, add, or remove a puzzle, just edit this list — no other code changes are needed.

## Project Structure

```
enigma-vault/
├── main.py            # game source code
├── README.md
├── assets/            # (optional) images/icons if you add any
├── ui_preview.png      # screenshot preview
└── leaderboard.json    # auto-created on first completed run (not tracked in git)
```

## License

Feel free to use, modify, and share this project.
