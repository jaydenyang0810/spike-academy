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

Robot configuration is a single constant near the top of the script (`ROBOT`):
drive motors on ports C and D, attachment motor on E, colour sensor A,
distance sensor B, force sensor F.

## Running it

Open `index.html` in a browser, or serve it from any static host.
