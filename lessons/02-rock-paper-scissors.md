# Lesson 2 — Rock Paper Scissors

**Game:** `games/rock-paper-scissors.html`

## What it is

You and the computer both pick. Rock beats scissors, scissors beat paper,
paper beats rock. The lesson: how a computer "decides" and how a small table
of rules replaces many words.

## The idea — conditions and random

A computer has no free will. Every "decision" is a check: `if`, `else if`,
`else`. The `beats` table is a tiny database the program looks up. Randomness
comes from `Math.random()`, which returns a number between 0 and 1 — we turn
it into one of three choices.

## Map it in the code

- `var beats = { rock: 'scissors', paper: 'rock', scissors: 'paper' };`
  — one line that holds all the rules. Cleaner than three long ifs.
- `Math.floor(Math.random() * 3)` — random 0, 1, or 2 → one of `options`.
- The `if / else if / else` chain — exactly one outcome happens.

## Try this

1. Add a "lizard and Spock" rule (lizard eats paper, Spock smashes scissors…).
   Add the two options to `options` and two rows to `beats`.
2. Change the message so it also shows how many rounds were played.
3. Make "best of 5" — the game stops when someone reaches 3 wins.

## Make it yours — a project

Turn it into **Rock Paper Scissors Lizard Spock** (5 choices, 10 rules in the
`beats` table). This is a real lesson in **finite-state logic**: every pair
of choices has exactly one winner, and the whole game fits in one table.
