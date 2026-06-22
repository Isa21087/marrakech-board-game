# Marrakech — Board Game in C++

Implementation of the Marrakech board game for two players, developed in C++ as the final project for the Introduction to Programming course (1st semester, Systems Engineering — Pontificia Universidad Javeriana, 2025).

---

## Description

Marrakech is a strategy game where two merchants compete to dominate the carpet market in the plaza. Each player moves Hassam (the merchant) across a 7x7 board, places carpets, and collects coins from the opponent when they land on occupied tiles. The player with the most points when all carpets are placed wins.

---

## Gameplay

Each turn consists of three actions:

1. **Move Hassam**: the player chooses a direction (up, down, left, right) and the dice rolls automatically (1-4). If Hassam exits the board, he follows the border path and re-enters from the other side.
2. **Pay the opponent**: if Hassam lands on a rival carpet, the current player pays one coin per visible tile of that color, including adjacent carpets of the same color. If the player runs out of coins, they lose the game.
3. **Place a carpet**: the player places their carpet on two tiles adjacent to Hassam's position, following the allowed overlap rules.

At the end, each visible carpet half scores one point, plus remaining coins. Highest score wins.

---

## Features

- 7x7 board rendered in the console with ANSI colors
- Hassam displayed with current facing direction
- Random dice roll using `rand()` with `srand(time(0))` seed
- Full movement and carpet placement validation
- Payment system with adjacent same-color carpet calculation
- End-of-game detection by coins or carpets exhausted
- Final score calculation and winner declaration
- Game result exported to `resultado_partida.txt`

---

## How to compile and run

Requires Windows (`windows.h` is used for console color support).

**With g++:**
```bash
g++ Juego_de_Marrakech_Isabella_Hermosa_Losada.cpp -o marrakech
./marrakech
```

Or run the `.exe` file included in the repository directly.

---

## Files

| File | Description |
|---|---|
| `Juego_de_Marrakech_Isabella_Hermosa_Losada.cpp` | Full source code |
| `Juego_de_Marrakech_Isabella_Hermosa_Losada.exe` | Windows executable |
| `resultado_partida.txt` | Result of the last game played |
| `Instrucciones_marrakech.pdf` | Original project brief (Spanish) |

---

## Tech Stack

`C++` `Structs` `File I/O` `ANSI escape codes` `Random` `Console UI`
