# Soother App

**[soother.app](https://soother.app)**

An abstract sensory playground. Touch anywhere and light and sound answer. There
are no words, no buttons, no menus, no score and nothing to win.

It is built for autistic children, and it is built to be left running unattended
in a doctor's office, a respite room or on a museum table. Everything in it is
discoverable by touching the screen, so it works for a child who cannot read,
cannot aim precisely, or has never seen it before.

---

## The rules it is built to

These are constraints, not goals. Every change has to keep all of them.

- **No text and no interface.** Nothing on screen is a label, a button or a menu.
- **100% touch-discoverable.** If it cannot be found by touching, it does not exist.
- **Purely abstract.** No characters, no faces, no objects from the real world.
- **Nothing to achieve.** No goals, no failure, no skill gates, no timers.
- **No strobing** and no sudden loud sounds.
- **Always in tune.** Every note is an anhemitonic pentatonic over a moving drone,
  so nothing anyone does can sound wrong.
- **Position is pitch.** Where you touch decides the note, exactly and invertibly:
  left to right is the scale, up and down is the octave.
- **One file.** `index.html` is the whole app. No build step, no libraries, no
  network calls. All audio is synthesised live in Web Audio; all graphics are
  Canvas 2D and WebGL 1.

---

## What you can do

Nothing here has to be learned, and nothing has to be done accurately.

### With one finger

| Do this | And this happens |
| --- | --- |
| **Tap open space** | The note of that spot sounds and a ripple spreads |
| **Tap a creature** | It answers in its own voice, one of a dozen different ways |
| **Press and hold** | You wind up a wave. Rings contract inward and creatures spiral in; let go and it releases |
| **Drag a creature** | Pick it up and carry it. Let go and it drifts on |
| **Swipe** | You disturb the field. Fast swipes scatter, gentle ones draw creatures along |
| **Draw a shape** | The stroke is measured on release: a closed loop gathers what it encircled, a long straight cuts a current, a scribble churns, a spiral leaves a whirlpool, a zigzag throws sparks |
| **Tap a lit diamond** | Plays the phrase it belongs to. Untouched phrases play themselves eventually |
| **Pop a bubble** | Bubbles drift up in rafts and pop when touched |

### With more than one finger

The app tells the difference between a finger **placed and left** and a finger
**travelling**, and that single distinction drives everything below.

It is decided once, when the finger lands, and then it holds until that finger
lifts. A finger that settled is holding the instrument, so you can carry your
hands anywhere on the screen as fast as you like and the web comes with you,
stretching and changing pitch as it goes. A finger that arrived already moving
is a sweep for its whole life, even if it stops, so it can strum but it can
never accidentally join in.

| Do this | And this happens |
| --- | --- |
| **Place two fingers and hold** | A thread stretches between them and sings continuously. How far apart your hands are is the pitch: wide is low, close is high |
| **Place three or more** | The threads join into a web and a **beat** starts, playing the notes of the places you are touching. Each finger keeps its own colour so a child can point and say which light is theirs |
| **Swipe across the threads** | You strum them. Every thread you cross flares thick and settles back |
| **Sweep with a whole hand** | The field is raked into furrows, one per finger, and a chord sounds. More fingers means a bigger chord |

**Known not to work reliably:** pinching two creatures together to pair them,
and pulling one apart to split it. Both are in the code, but neither is
dependable in the hand. Left undocumented as a feature until that is fixed.

### The beat, in more detail

Three or more placed fingers start it, and it never repeats and never stops
while you are there.

- Every finger is a note, and it is the note of the place it is on.
- Octaves are spread automatically so the set comes out as a chord rather than a
  cluster, whatever four hands happen to land on.
- It plays in bars of eight. The downbeat belongs to the lowest note on the table,
  so there is always a bass holding the floor.
- A figure is chosen, played a few times over with small changes, then replaced.
  That is what makes it sound composed rather than shuffled.
- Notes are dealt round-robin, so everybody's finger is played before anybody's
  is played twice. Nobody waits.
- Sometimes a ribbon of light leaps out of one finger, arcs over the field, and
  sounds another when it lands.

### The echo

Tap a rhythm in open space and then stop. After a moment a light appears where
you first touched, travels to each place in turn arriving on your rhythm, and
sounds each one an octave up. Sometimes it replays the same figure somewhere
else on the screen, which transposes it.

- It answers **every** phrase, up to 32 taps long.
- It will not speak until you have genuinely stopped.
- No two replies treat your phrase the same way. Each one decides how fast to
  take it, whether to play all of it or pick its way through the middle,
  whether to linger on a note it liked, and once in a while whether to run the
  whole thing backwards. The notes are always yours and always in the scale, so
  none of it can come out wrong.
- Most replies end with a small cadence of their own: a run up the scale, a
  fall that lands on the root, or the root breathed twice an octave apart.
  Each note is placed where that pitch lives, so a rising ending is also a
  light climbing the screen.
- Touch anything and it stops mid-note. The turn is yours again.
- A phrase can only **begin** in open space. Drumming on a creature is a
  conversation with that creature, and does not seed one.

---

## What lives in the world

- **Creatures** drift, react to each other and to you, pair up, merge, split,
  age and eventually go. A touch travels outward as a wavefront rather than
  applying at once, so you watch the answer sweep across the field.
- **Elders** are old creatures. They always answer, and always properly.
- **Embers** are a creature wearing a hard rim. They wander, and eventually
  explode.
- **Bubbles** rise in rafts and pop.
- **Diamonds** are phrases waiting to be played. Tap the head to start one.
- **Planets** appear one at a time and live a while. Each has a face you can
  recognise across a room, and each one always does the **same** thing when you
  tap it:

  | Planet | Tap it and |
  | --- | --- |
  | Rocky (icy poles) | It skips stones out across the field. Each hop is shorter than the last until they sink |
  | Banded | It launches rockets. Some burst early, some get a long way out, some corkscrew, some never leave |
  | Ringed | It puts up a firework: one shell, a clean rise, a proper ring |
  | Dotted | It sends one arc of light out to a creature, which lights up and sometimes passes it on, and on again. Wherever it lands, that creature often sets off stones or a firework of its own |

  Planets gather moons, and swiping at one builds up energy until it breaks apart.

---

## The three controls

Top right corner, small and easy to forget. They are the only interface, and
they are glyphs rather than words. **Press and hold** the activity dial to open
it.

| Control | What it does |
| --- | --- |
| **Speaker** | Mute |
| **Moon** | Night mode. Dims everything for 12 hours, then lets itself out |
| **Dots with arrows** | Activity level. Drag to set how busy the world is. The world reacts as you drag |

All three remember their setting in that browser.

---

## Options

There is no settings screen and there never will be, so the address is the
settings surface. A school can bookmark one link per child and never see a menu.

| Address | Effect |
| --- | --- |
| `?vol=0..100` | Master volume |
| `?kiosk=1` | Unattended install: goes fullscreen on first touch, swallows the browser back gesture |
| `/full` | **Museum mode.** Keeps the settings this browser already has and takes the three controls off the screen so nobody can move them. `?full` and `#full` do the same |
| `?level=0..3` | How much has to be aimed at (see below) |
| `?scan=1` | Single switch: a highlight travels, one press takes it |
| `?scan=2` | Two switches: one key moves the highlight, the other takes it |
| `?scanms=2000` | How long the highlight rests on each one |
| `?dwell=1` | Eye gaze: look to pick up, look elsewhere to put down |
| `?debug=1` | Log what the audio is doing to the browser console. Use this first if a screen goes silent |

### The ladder (`?level=`)

The same activity offered at several levels of demand, so a child who cannot yet
aim is not locked out of it.

| Level | Meaning |
| --- | --- |
| `0` | **Watching.** Nothing is required. The world is livelier on its own and any input at all is answered generously wherever it lands |
| `1` | **Anything.** Any input does something. A press that lands on nothing still wakes whatever is nearest, so it is never possible to miss |
| `2` | **Touching.** The direct mechanics only: tapping and carrying. No drawn shapes, no piles |
| `3` | **Everything.** The whole thing. The default |

It is also adaptive. If presses keep landing on empty space, the app quietly
becomes more generous about what counts as a hit.

### Museum mode, in practice

Set night mode, mute and the activity level the ordinary way on that device,
then send the room to `/full`. Those settings live in the browser's own storage,
not in the address, so they survive. There is deliberately no way out from
inside the page. To undo it, go back to the plain address on that device.

**It renews itself.** After eight hours of uptime, once nobody has touched it
for thirty minutes, the page reloads. Both conditions are required, so it can
never reload under someone's hands. That clears anything that has accumulated
over a long run and quietly picks up the latest deployed version, which matters
for a screen nobody visits.

Kiosk mode cannot defeat the device's own home gesture. For that, use Guided
Access on an iPad, or a kiosk browser on Android or Windows.

---

## Deploying

The site is a static GitHub Pages deployment of the `sootherapp/website` repo,
served at the apex domain `soother.app` with `www` redirecting to it.

Files that need to be uploaded:

| File | Why |
| --- | --- |
| `index.html` | The entire application |
| `manifest.webmanifest` | Home-screen install, icons |
| `og.jpg` | The picture a shared link shows (1200x630) |
| `full/index.html` | A tiny redirect page. GitHub Pages serves files, not routes, so `/full` needs a file; it hands straight over to `../?full` |

DNS: apex `A` records to the four GitHub Pages addresses, `www` as a `CNAME` to
`sootherapp.github.io`. HTTPS is enforced and the certificate covers both names.

---

## How it is built

Enough to orient someone opening the file for the first time. The file itself is
heavily commented, and the comments explain **why** rather than what.

- **One IIFE**, ES5-style, no modules, no dependencies, no build.
- **Layers.** A WebGL fluid field at the back, then an accumulating trail buffer,
  then the screen canvas. The trail buffer is **never cleared, only veiled**, which
  is what gives everything its smoke. The consequence, and the single most common
  bug in this file's history: anything drawn repeatedly at a spot that does not
  move burns a permanent hole there. Fingers, held threads and stationary
  planets are therefore drawn on the screen canvas, fresh every frame.
- **Audio** is a tiered bus. Phrases get their own path around the shared limiter
  and reverb so they are always audible; player actions duck the scenery.
  Voice counts are capped, because the target hardware includes old iPads.
- **Sizing.** The stylesheet owns the canvas size (`100vw` by `100vh`, fixed,
  under `viewport-fit=cover`). The script owns only the drawing buffer and must
  never write width or height back onto the element.

---

## Keeping this file honest

This README is maintained alongside the app. When behaviour changes, this
changes in the same commit. If something described here does not match what the
app does, the README is the thing that is wrong.
