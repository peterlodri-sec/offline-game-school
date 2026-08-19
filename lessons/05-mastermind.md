# Lesson 5 — Mastermind

**Game:** `games/mastermind.html` · **Short:** https://youtu.be/wSMxHZgRt8k

## What it is

The computer hides a 4-color code. You guess; it answers with how many pegs
are right (position correct) and how many are the right color but wrong
place. Crack the code in 10 tries. The lesson: **deduction** and comparing
lists.

## The idea — compare two lists, two passes

You have a guess and a secret, both arrays of 4. Feedback is two numbers:
`exact` (same color AND same spot) and `loose` (same color, wrong spot).
The trick is to count in TWO passes:

1. First pass: find exact matches, and REMOVE those cells from both lists so
   they are not counted again.
2. Second pass: for each remaining guess color, check if the secret still
   contains it — that is a loose peg.

This "remove after counting" is a classic programming habit: it stops double
counting.

## Map it in the code

- `remaining = current.slice()` and `remSecret = secret.slice()` — working
  copies, so the real arrays stay untouched.
- `remaining.splice(i, 1)` and `remSecret.splice(k, 1)` — removing used cells
  so nothing is counted twice.
- The hint line builds black and white dots from the two numbers.

## Try this

1. Why does the code loop backwards (`for (var i = 3; i >= 0; i--)`) when
   removing cells? (Hint: removing changes the indexes.)
2. Change 6 colors to 8. Much harder code.
3. Play with a pencil and paper: can you crack it in fewer tries by making
   guesses that test many colors at once?

## Make it yours — a project

Flip it: let the HUMAN hide a code and the COMPUTER guess it. The computer
starts with a guess, reads your two numbers, and must keep a list of all
still-possible codes — removing any that would not give those numbers. This is
**elimination search**, the same idea behind spam filters and chess engines:
keep only what matches the evidence.
