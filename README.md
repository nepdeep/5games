# Pip's Puzzle Island

A 3D thinking game for 4 and 5 year olds. Pip the chick guides children through five
mini-games, each built around one logic skill that comes before numbers. Everything is in a
single file, `index.html`, using [three.js](https://threejs.org) for the 3D.

**To play:** open `index.html` in a modern browser (Chrome, Safari, Edge or Firefox) on a
tablet, laptop or phone, then tap the big green button. It needs an internet connection the
first time, to load three.js and the fonts from a CDN. Landscape works best on phones.

## The five games

| Game | Skill | What the child does |
| --- | --- | --- |
| Pattern Train | Patterns, prediction | Picks what comes next on a train (AB, AAB, ABB, ABC, AABB), by colour, shape and size, later with the gap in the middle. Each item plays a note, so patterns can be heard as well as seen. |
| Hungry Monsters | Sorting, classification | Drags cookies to the monster that eats them: by colour, then shape, then size, then by two rules at once (for example red *and* square). |
| Bunny Hop | Planning, early coding | Builds a sequence of arrow cards, presses Go, watches Bunny follow it, then finds and fixes mistakes. Later boards add rocks, two carrots, and no path preview. |
| Odd One Out | Comparing, reasoning | Finds the one that is different. Later puzzles hide the clue among other differences, and Pip explains the answer ("The others are all red!"). |
| Tower Builder | Ordering (seriation) | Stacks rings from biggest to smallest, then builds stairs from shortest to tallest so Bunny can climb to a star. |

## How it teaches

- **No reading needed.** Pip speaks every instruction using the device's built-in speech,
  and the text also appears in a bubble. The yellow speaker button repeats the instruction.
- **No failing.** A wrong answer gets a gentle, funny response and a hint. After two tries,
  the right answer glows. There are no timers and no scores.
- **Adapts to the child.** Each game has 5 to 7 levels. After a round, the level goes up if the
  child found it easy, stays the same otherwise, and eases back if it was too hard.
- **Rewards that grow the world.** Every finished round earns a star. Stars unlock surprises
  on the island: balloons, a rainbow, butterflies, hats for Pip, a hot air balloon, fireworks.
- **Explore and play.** On the island, children can spin the island and tap Pip, trees, the
  sun, clouds and the pond just to see what happens.

## For grown-ups

Press and hold the purple gear on the island for about a second to open the grown-ups panel.
It explains each game and has switches for Pip's voice, music and sound effects, plus a
button to erase progress. Progress is saved in the browser on this device only.

## Technical notes

- One HTML file with inline CSS and JavaScript (ES module). three.js `0.170.0` is imported
  from jsDelivr, with unpkg as a fallback.
- All models (characters, train, monsters, scenery) are built from three.js primitives in
  code. All sound effects and the background music are synthesized with the Web Audio API.
  There are no image or audio files.
- Works with touch, mouse and pen. Buttons are large for small hands, and the layout adapts
  to any screen size.
- `window.__pip` exposes a few helpers for automated testing (for example
  `__pip.go('train')` or `__pip.solve()`).
