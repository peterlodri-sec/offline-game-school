# Lesson 4 — Tic Tac Toe

**Game:** `games/tic-tac-toe.html` · **Short:** https://youtu.be/c7WVp_OSUuM

## What it is

Two players, X and O, three in a row. The lesson: a **2D array** and how a
computer checks a win by trying every winning line.

## The idea — grids and win lines

A board is a grid. A grid is an array of arrays: 3 rows, each with 3 cells.
There are only 8 ways to win (3 rows, 3 columns, 2 diagonals). The computer
stores those 8 lines as a list, then for each line asks: "are all three cells
the same mark and not empty?" If yes — someone won.

## Map it in the code

- `var grid = [['','',''],['','',''],['','','']]` in the game becomes a flat
  `grid = ['','','',...]` with `wins` listing the 8 lines as cell numbers.
- `grid[line[0]] === mark && grid[line[1]] === mark && grid[line[2]] === mark`
  — the whole win check is one line per line-of-3.
- `grid.indexOf('') === -1` — the tie check: no empty cell left.

## Try this

1. Count: why are there only 8 winning lines? (3 + 3 + 2.)
2. Change the marks to your initials.
3. Add a score board: wins for X, wins for O, draws.

## Make it yours — a project

Make the computer PLAY. Simplest rule: after the human moves, the computer
picks the first empty cell that would make a win for itself; otherwise the
first empty cell. You will write a `bestMove()` function that scans the 8
lines — the same scan as `checkWin`, but looking one move ahead. This is the
start of **artificial intelligence**: looking at the board and choosing.
