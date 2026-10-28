# Meridian Orrery

A gravity sandbox you play like an instrument. Throw planets around a sun, and each one chimes as it crosses the meridian line. Closer orbits ring higher notes. Because orbital periods follow Kepler's third law (period² ∝ radius³), every system you build becomes a polyrhythm.

It is a single `index.html` file with no build step and no dependencies beyond two Google Fonts. Open it in a browser and press **Start sound**.

## How to play

- **Drag** anywhere to throw a planet. A dotted line predicts its path and shows the note it will play.
- **Tap** empty sky to drop a planet into a perfect circular orbit.
- **Tap a planet** to remove it.
- When most of the planets line up on one ray from the sun, a **conjunction** fires a beam through them and plays a chord.

## Systems

Each preset uses real period ratios, so you hear its actual rhythm.

| System | What you hear |
| --- | --- |
| Twelve-beat alignment | Periods 1 : 2 : 3 : 4 : 6. All five line up again every twelve beats. |
| Jupiter's moons | Io, Europa and Ganymede in their 1 : 2 : 4 Laplace resonance, with Callisto running free. |
| TRAPPIST-1 | Seven Earth-sized planets chained in resonances of 8:5, 5:3, 3:2, 3:2, 4:3 and 3:2. |
| Inner planets | Mercury to Mars at their true relative distances, read in au. |
| Random resonant chain | A new set of simple period ratios each time. |

## Tune panel

- **Scale**: D minor pentatonic, major pentatonic, hirajōshi, lydian or whole tone
- **Voice**: Bell (FM synthesis), Marimba or Glass
- **Meridians**: 1 to 4 chime lines; more lines mean denser rhythms
- **Tempo** and **Sun mass**
- **Planet mass**: None (weightless), Real (true mass ratios), ×10 or ×100. Heavier planets tug on each other and on the sun, and resonant systems drift into chaos.

## Keyboard

| Key | Action |
| --- | --- |
| Space | Pause / resume |
| N | New random system |
| C | Clear the sky |
| M | Mute / unmute |
| T | Open the tune panel |

## How it works

- Every body pulls on every other body, the sun included. Physics runs at a fixed 240 steps per second with leapfrog (kick-drift-kick) integration, which conserves energy to about one part in a million over minutes of play.
- Presets use real mass ratios: Jupiter's moons relative to Jupiter, the TRAPPIST-1 planets relative to their red dwarf, Mercury to Mars relative to the Sun. The twelve-beat system uses Neptune-sized planets so its rhythm holds.
- The camera follows the system's centre of mass, so the sun visibly moves. The **Sun wobble** plot in the orbit log traces its path, magnified. Measuring this wobble is how astronomers found many real exoplanets.
- A chime fires when a planet's position changes sign relative to a meridian ray. The note comes from the planet's distance at that moment, mapped onto 15 bands of the chosen scale.
- Sound is pure Web Audio: FM bells, a generated reverb impulse, stereo panning by pitch, and a compressor on the master bus.

See [ROADMAP.md](ROADMAP.md) for what's coming next.
