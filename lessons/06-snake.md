# Lesson 6 — Snake

**Game:** `games/snake.html` · **Short:** https://youtu.be/9LHvaEiANSw

## What it is

A snake that moves by itself, eats food, grows longer, and dies if it hits a
wall or itself. The lesson: the **array-as-the-body** trick, **timers**, and
**collision** — the three ideas behind almost every moving game.

## The idea — moving by adding and removing

The snake is just an array of cells. Every tick:

1. Put a new head cell in front (`snake.unshift(head)`).
2. If it ate the food, leave the tail (the snake grows).
3. Otherwise remove the tail (`snake.pop()`).

That single add-front / remove-back step IS the motion. Nothing else moves.

## Map it in the code

- `setInterval(tick, 140)` — a timer that runs `tick` 7 times a second.
  Games are timers: draw, update, repeat.
- The collision check — one `if` tests the wall, and `snake.some(...)` tests
  the body.
- The `turn()` guard `if (dir.x !== -x || dir.y !== -y)` — the snake cannot
  reverse into itself. A tiny rule that prevents a whole class of bugs.

## Try this

1. Change `140` to `70`. Speed. Change `20` (grid size) to make it harder.
2. Make the food worth more points the longer the snake gets.
3. Add walls so the snake wraps around (head leaves right → comes back left).
   That removes the wall death entirely.

## Make it yours — a project

Build a **catch-the-falling-items** game: items fall from the top; a basket
moves left and right at the bottom; catching adds points, missing loses a
life. You will reuse all three ideas: an array of falling items, a timer, and
collision checks between the basket and each item. It is Snake, turned upside
down — and now you own a second genre.
