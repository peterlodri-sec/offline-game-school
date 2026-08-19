# Capstone — Build YOUR OWN game

You finished six games. Now build a seventh one that did not exist before.
This is the OSSU-style final project: take the parts you now know and combine
them into something of your own.

## What you now know

| Idea | Game that taught it |
|---|---|
| if / else, loops, counting | Guess the Number |
| random, tables of rules | Rock Paper Scissors |
| arrays, shuffle, state | Memory Match |
| 2D grids, checking lines | Tic Tac Toe |
| comparing lists, elimination | Mastermind |
| timers, collision, add/pop | Snake |

## Choose an idea (or invent one)

- A **quiz game**: ask a question, check the answer, keep score (Memory Match
  + Guess the Number).
- A **ladder game**: climb a grid, dodge falling rocks (Snake + Tic Tac Toe).
- A **logic riddle**: guess a hidden pattern with hints (Mastermind).
- A **two-player race**: first to the finish, dice roll decides the steps
  (Rock Paper Scissors randomness + a board).
- Your own idea. If you can say the rules in one sentence, you can build it.

## The recipe for any game

1. **State** — what changes? Write the variables: score, position, turn…
   (one `var` per thing that changes).
2. **Draw** — a function that shows the state on the screen.
3. **Update** — a function that changes the state when something happens
   (a click, a key, a timer).
4. **End** — a rule that stops the game (win, lose, time up).

Copy `games/snake.html` and change it, or start from an empty file:

```html
<!DOCTYPE html><html><head><title>My Game</title><style>...</style></head>
<body><script>
  // 1. state
  var score = 0;
  // 2. draw
  // 3. update (on click / key / timer)
  // 4. end
</script></body></html>
```

## The rules of the school

- ONE file. It must open by double-click, with no internet.
- It must work on a phone (big buttons, no mouse-only).
- Simple English. No ad, no account, no tracking.
- Copy it, change it, give it away — that is the point.

## Show your work

When it works, put it in `games/` and open a pull request, or share the file
with your class, your center, or anyone learning with nothing. Every game
someone can play is a lesson someone can keep.

*offline game school · learn by playing · fine touch from within*
