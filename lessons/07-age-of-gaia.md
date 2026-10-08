# 07 — Age of Gaia (a tiny real-time strategy)

**What you learn:** entities and a game loop, resource economy, timers and
waves, simple collision and targeting, and the Dark → Feudal → Castle idea of
*progression* as a number that changes everything.

**Play it:** open `games/age-of-gaia.html`. One file. No internet.

## How to play

- **Gather:** click a **tree** (wood), **berry** (food), or **gold** node — the
  nearest idle villager walks over and gathers it until the node is empty.
- **Grow:** *train villager* (50 food), *build house* (30 wood, +5 pop).
- **Fight:** *train militia* (60 food, 20 gold). Militia walk out and meet the
  enemies on their own.
- **Age up:** Dark → Feudal (300 food, 100 wood) → Castle (600 food, 400 gold).
  Each age makes villagers gather faster and militia tougher.
- **Survive five waves.** If the town center hits 0 HP, you lose.

## The ideas in the code

1. **The loop.** `requestAnimationFrame(frame)` calls `step(dt)` then `draw()`.
   `dt` (seconds since last frame) is why things move at the same speed no
   matter how fast the computer is. Try changing `dt` — the whole world changes
   speed.
2. **Entities.** Villagers, militia, and enemies are just objects in arrays,
   each with `x`, `y`, `hp`. The game *is* those arrays.
3. **Economy.** Resources are numbers; actions subtract from them. Change
   `RATE = 3` (gather per second) and see how the game feels.
4. **Timers & waves.** `S.nextWave` is a clock: when `S.t` passes it, enemies
   spawn and the clock jumps forward. That is how "waves" work.
5. **Targeting.** Each soldier finds the nearest enemy with a loop over the
   array and moves toward it. That one idea — *nearest* — is most of game AI.

## Make it yours

- Change the starting resources to `1000` — what becomes easy?
- Make militia cost `0` — is the game still fun? Why or why not?
- Add a **fourth resource** (say, 🍇 berries) and a **fourth age**.
- Make enemies faster (`52` → `90`) and see how the balance breaks.

## For David

Made the day a friend in the Netherlands — who nudged us toward teamLab and
keeps asking the good questions — met the constellation.

*Age of Gaia is a fan homage; not affiliated with Age of Empires. The loop is
ages old: gather, build, defend, ascend. Fine touch from within · 0 + 1.*

## The samurai layer (Sengoku)

Toggle **⚔ samurai layer** for the Sengoku reskin:

- resources become **rice · timber · koku**,
- the ages read **Sengoku → Azuchi–Momoyama → Edo**,
- villagers are **ashigaru** (straw hats), militia are **samurai** (topknot + katana),
- the raiders are **rōnin** (banners), and the town becomes a **castle (城)**,
- a **patience (忍耐) meter** fills while your line holds and grants damage reduction;
  lose a unit and it halves. *Patience is the root of quietness.*

**Why it is here.** Tokugawa Ieyasu (1543–1616) — the third of the Great Unifiers and the
founder of the Tokugawa shogunate — won by outlasting. He was a hostage as a boy, waited
through Nobunaga and Hideyoshi, and took power at Sekigahara. The layer quotes his own words:

> Life is like unto a long journey with a heavy burden. … Forbearance is the root of all
> quietness and assurance forever.

(Source: the *Tokugawa Ieyasu* article on Wikipedia, CC BY-SA. A small homage, plainly credited.)
