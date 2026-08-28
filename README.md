# SPIKE 積木教室 / SPIKE Block Academy

A bilingual (繁體中文 / English) LEGO SPIKE Prime block-coding trainer for FLL
beginners, built with [Blockly](https://developers.google.com/blockly).

Kids learn to program a simulated SPIKE Prime robot — motors, movement, loops,
the colour / distance / force sensors and the gyro — before they touch the real
hardware. 7 units, 21 lessons, 63 tasks, roughly two hours of class time.

- **Single self-contained file.** `index.html` has Blockly compiled in, so it
  runs from any static host with no build step and no network calls except the
  Google Fonts stylesheet.
- **One language on screen at a time**, switched by the button in the header.
- **Real SPIKE semantics.** Movement blocks carry motor travel, not robot
  travel: 180 motor degrees is a 90° turn on this robot's geometry.
- **Live simulation.** One grid square = one wheel rotation = 27.6 cm, which is
  what makes the distance sensor's centimetre readings real.
- **FLL competition mats** in Free Build. The mat is drawn to scale from its
  real 2362 x 1143 mm, which is 8.56 x 4.14 wheel rotations, so the robot,
  the grid and the mission models all share one measurement system.

## The FLL mats

Free Build can swap the practice grid for a SUBMERGED (2024-25) or UNEARTHED
(2025-26) mat, so a path can be planned without tying up the physical table.

- **Zoom** with the + and - buttons or the scroll wheel, 100% to 800%. The mat
  opens fully visible and zooms in far enough to read a model; drag to pan.
- **Guide grid in wheel rotations**, numbered along the top and left edge, so
  a route can be counted off in the same unit the movement blocks use.
- **Draggable start.** The robot begins in the launch area and can be dragged
  anywhere to test one leg of a run.
- **The field is drawn, not just tinted.** Each mat has its own terrain, a
  dark guide line to follow, and every mission is a small schematic object -
  a shark, a submersible, a dig site - so the field reads at a glance.
- **The models are references, not mechanisms.** Nothing scores and nothing
  collides: this is for rehearsing a path, not simulating a match.

Mission numbers, names and positions come from FIRST's own Field Setup Guide
for each season: the positions are read off the numbered callouts in its field
overview and normalised against the mat edges, so the layout matches the real
one closely. It is not surveyed, though, because a callout sits near its model
rather than exactly on it. FIRST's mat artwork is their copyright and is not
reproduced; the objects drawn here are original schematics that say what a
mission is, not what it looks like.

Unlock the models with the Lock button to drag them to their measured places;
the layout saves to the browser, and Export / Import moves a corrected layout
to the rest of the team.

Robot configuration is a single constant near the top of the script (`ROBOT`):
drive motors on ports C and D, attachment motor on E, colour sensor A,
distance sensor B, force sensor F.

## Running it

Open `index.html` in a browser, or serve it from any static host.
