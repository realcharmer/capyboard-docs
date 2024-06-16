---
icon: material/space-invaders
---

# Game of Life

## Overview

Conway's Game of Life is a fascinating mathematical simulation created by John Conway in 1970. It simulates a world where cells live, die, and multiply based on a few simple rules. The game plays itself once you set it up, so you can just sit back and watch the action unfold. You can read more in the [original document](https://web.stanford.edu/class/sts145/Library/life.pdf) describing the game. You can also try playing the game in an [online simulator](https://playgameoflife.com).

The task is to create an implementation of Conway's Game of Life using Capyboard's Light Module.

## How It Works

- Every LED on the module represents square in a grid and is called a cell.
- Every cell can either be alive (LED on) or dead (LED off).
- Each cell interacts with its eight surrounding cells.

## The Rules

The fate of each cell from one moment to the next is determined by these simple rules:

- **Loneliness**: If a cell is alive and has fewer than two live neighbors, it dies.
- **Survival**: If a cell is alive and has two or three live neighbors, it continues to live.
- **Overcrowding**: If a cell is alive and has more than three live neighbors, it dies.
- **Reproduction**: If a cell is dead but has exactly three live neighbors, it becomes alive.
