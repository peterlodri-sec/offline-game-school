# Lesson 1 — Guess the Number

**Game:** `games/guess-the-number.html` · **Short:** https://youtu.be/UPD9-e7b21Y

## What it is

A number is hidden from 1 to 100. You guess; the computer says HIGHER or
LOWER. The lesson: you can find any number in at most 7 tries — if you always
guess the middle of the range.

## The idea — binary search

Cut the problem in half every time. 1..100 → guess 50 → if LOWER, the answer
is 1..49 → guess 25 → and so on. Each guess halves the possibilities, so 100
possibilities need at most 7 halvings (2^7 = 128). This is how computers
search phone books, dictionaries, and databases: **binary search**.

## Map it in the code

Open the file in a text editor. Look for these:

- `low` and `high` — the range. `low = 1; high = 100;` at the start.
- `if (g < secret) { low = g; ... }` — one guess shrinks the range.
- `Math.random() * 100 + 1` — how the computer picks the secret.

## Try this

1. Play with the "guess the middle" strategy. Count tries. It never passes 7.
2. Change `100` to `1000` (in `newGame`). How many tries now? (Answer: 10.)
3. Guess randomly instead of middle. How many tries on average?

## Make it yours — a project

Change the game so the COMPUTER guesses and the HUMAN says HIGHER or LOWER.
Swap the roles: keep `low`/`high`, let the computer print its middle guess,
and add three buttons: Higher / Lower / Correct. Now you have written your
first searching program.
