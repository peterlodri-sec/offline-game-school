# Lesson 3 — Memory Match

**Game:** `games/memory-match.html` · **Short:** https://youtu.be/40dcJc7to5c

## What it is

16 cards, 8 pairs, face down. Flip two; if they match they stay up. The
lesson: the most useful idea in programming — the **array** — and how to
shuffle it.

## The idea — arrays and shuffling

An array is a numbered list: `deck[0]`, `deck[1]`, … Computers keep almost
everything in arrays — a queue of people, a list of songs, the pixels of a
screen. The shuffle here (Fisher-Yates) is famous: walk the list from the end
and swap each item with a random earlier one. One pass, perfect randomness.

## Map it in the code

- `faces.concat(faces)` — makes `[A,B,C,D,E,F,G,H,A,B,C,D,E,F,G,H]`: the
  pairs. Then `shuffle` mixes it.
- `open.push({...})` — remembers the two flipped cards so we can compare.
- `document.querySelectorAll('.matched').length === deck.length` — "all 16
  cards are matched" is just counting.

## Try this

1. Change `['A','B',...]` to 12 pairs (change `4` to `6` in the grid CSS and
   add letters I–L). Bigger board, same rules.
2. Instead of letters, use your own symbols or pictures.
3. Count the moves and try to beat 12 moves.

## Make it yours — a project

Build a **flashcard game**: one side shows a question (e.g. "5 x 7"), the
other shows the answer. When you flip a card and answer correctly, mark it
`matched`. This is the same array-and-state structure — and now it is a study
tool your whole class can use.
