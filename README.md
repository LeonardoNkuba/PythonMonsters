# PythonMonsters

A 2D monster RPG built with Python, Pygame Community Edition, and PyTMX. Explore maps, talk to characters, battle trainers and wild monsters, and grow your team through catching, leveling, and evolution.

## Setup and run

Install Python 3 (tested with Python 3.14). From the project folder, run these commands in PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe src/main.py
```

If the virtual environment is already set up, only the last command is needed. In your IDE, select `.venv/Scripts/python.exe` as the Python interpreter and run `src/main.py`.

On macOS or Linux, use `.venv/bin/python` instead of `.venv\Scripts\python.exe`.

The project uses `pygame-ce`, which provides the `pygame` import. Asset paths are resolved from the source files, so the game can also be launched from another working directory.

## Controls

- **Arrow keys:** Move the player or navigate menus.
- **Space:** Talk, advance dialogue, or confirm a selection.
- **Enter:** Open or close the monster index outside battles and dialogue.
- **Escape:** Go back in battle menus.

## Project structure

```text
PythonMonsters/
|-- src/                 # Python game code
|   |-- main.py          # Entry point and game loop
|   |-- settings.py      # Display settings and asset paths
|   |-- game_data.py     # Monsters, attacks, and trainer definitions
|   |-- battle.py        # Battle logic
|   |-- entities.py      # Player and characters
|   |-- monster.py       # Monster stats and progression
|   |-- monster_index.py # Team menu
|   |-- evolution.py     # Evolution animation
|   |-- dialog.py        # Character dialogue
|   |-- sprites.py       # Game sprites
|   |-- groups.py        # Rendering groups
|   |-- support.py       # Asset loading and helpers
|   |-- timer.py         # Timers
|   `-- debug.py         # Debug display helper
|-- assets/
|   |-- graphics/        # Sprites, tiles, fonts, backgrounds, and UI
|   |-- audio/           # Music and sound effects
|   `-- data/
|       |-- maps/        # Tiled map files (.tmx)
|       `-- tilesets/    # Tiled tileset definitions (.tsx)
|-- requirements.txt    # Python dependencies
|-- .gitignore
`-- README.md
```

Keep the folders inside `assets/` together: the Tiled files reference graphics through relative paths. The local `.venv/` and Python cache files are ignored by Git.
