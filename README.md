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
- **Live simulation.** One grid square is one wheel rotation, which is what
  makes the distance sensor's centimetre readings real. The lessons are pinned
  to the 88 mm wheel they were written for, at 27.6 cm a square. A mat follows
  the wheel picked in Free Build, defaulting to 56 mm at 17.6 cm, since that is
  the wheel most teams drive on.
- **Adjustable split.** The divider between the code and the field can be
  dragged, double-clicked to reset, or moved with the arrow keys, and the
  field redraws as it moves.
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
- **Draggable start, with a heading.** The robot begins on the square centre
  nearest the home area and can be dragged anywhere to test one leg of a run.
  Drag snaps to square centres, alt-drag places it freely, the rotate buttons
  turn it 45 degrees a click and 15 with shift, and shift-drag aims it at the
  cursor. Turning re-zeroes the gyro, so a program's turns start from zero
  whichever way the robot is facing.
- **The field is drawn, not just tinted.** Each mat has its own terrain, a
  dark guide line to follow, and every mission is a small schematic object -
  a shark, a submersible, a dig site - so the field reads at a glance.
- **The models are references, not mechanisms.** Nothing scores and nothing
  collides: this is for rehearsing a path, not simulating a match.

On the 56 mm wheel a mat is 13.4 by 6.5 squares; on 88 mm it is 8.5 by 4.1.
The robot is declared in squares so that it fits inside one, so it is drawn
smaller on the smaller wheel. A real robot does not shrink when its wheels do,
so treat the 88 mm view as the one that is true to the robot's own size.

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
