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
| Einstein's rosettes | Three eccentric orbits with relativity turned up. Each ellipse slowly turns, so its meridian note walks through the scale. |
| Kepler's laws | One very eccentric planet and one circular planet with Kepler mode on. Equal-time wedges have equal areas; the ticks rush together near the sun. |
| Jupiter's Trojans | A heavy Jupiter with two camps of asteroids at its L4 and L5 points, seen from a camera that turns with it. The asteroids loop in tadpoles and strum softly as they pass the meridian. |
| Random resonant chain | A new set of simple period ratios each time. |

## Tune panel

- **Scale**: D minor pentatonic, major pentatonic, hirajōshi, lydian or whole tone
- **Voice**: Bell (FM synthesis), Marimba or Glass
- **Meridians**: 1 to 4 chime lines; more lines mean denser rhythms
- **Tempo** and **Sun mass**
- **Planet mass**: None (weightless), Real (true mass ratios), ×10 or ×100. Heavier planets tug on each other and on the sun, and resonant systems drift into chaos.
- **Einstein**: Off, 3°, 10° or 30° of perihelion turn per orbit at 1 au. See below.
- **Kepler**: shows equal-time wedges and a ticking 30° dial. See below.
- **View**: Fixed, or Rotating, where the camera turns with the heaviest planet so it stays at the top.
- **Lagrange**: marks the five Lagrange points of the heaviest planet. See below.

## Einstein mode

In Newton's gravity, a lone planet traces the same ellipse forever. General relativity adds a small extra pull close to the sun, so each ellipse turns a little every lap. Mercury's orbit turns by 43 arcseconds per century more than Newton predicts. In the 1800s astronomers blamed an unseen planet they named Vulcan. In 1915 Einstein explained the extra turn with no new planet at all.

The real effect is tiny (Earth's orbit turns 0.04″ per lap), so the orrery exaggerates it by hundreds of thousands to millions of times.

- **Diamonds** mark each planet's closest approach to the sun. With Einstein off they pile up in one spot. With it on they march around the sun.
- The orbit log's last column switches to **Turn/orbit**, measured live. At the 3° setting it matches Einstein's formula, Δφ = 6πGM / (c²a(1−e²)), within about 5%.
- Because the ellipse turns, the distance at which a planet crosses the meridian changes, so its note slowly walks up and down the scale.

## Kepler mode

Kepler's second law says a line from the sun to a planet sweeps out equal areas in equal times. Kepler found it in 1609 from Tycho Brahe's observations of Mars. It is the same thing as conservation of angular momentum.

- **Shaded wedges** each take one twelfth of the planet's orbital period. Far from the sun they are long and thin; close in they are short and fat. Their areas match.
- The orbit log's last column switches to **Wedge area**: how far the twelve most recent wedges differ from their average. With Newton's gravity they agree to about ±0.02%. Einstein mode keeps them equal, because its extra pull still points straight at the sun. Heavy planets tugging on each other (Planet mass ×100) break the law, and the spread grows to over 1%.
- **Ticks** fire every time a planet passes one of the 12 dotted spokes of the brass dial. A circular orbit ticks steadily. An eccentric one ticks slowly far out and in a rapid burst at closest approach, because its angular speed grows with 1/r². In the Kepler's laws preset the ticks run about 26 times faster at closest approach.

## Lagrange points and Trojans

Around any planet there are five places where a small body can keep pace with it: the Lagrange points L1 to L5. L1, L2 and L3 lie on the line through the sun and the planet. L4 and L5 sit 60° ahead of and behind the planet, each making an equilateral triangle with it and the sun.

- Turn on **Lagrange** and tap any point to drop a swarm of asteroids there. Asteroids have no mass, so they feel the sun and planets but pull on nothing.
- **L4 and L5 are stable.** Asteroids dropped there stay, swinging back and forth in tadpole-shaped loops that only show up in the **Rotating** view. Jupiter has thousands of real ones, named after heroes of the Trojan War: the Greek camp at L4 and the Trojan camp at L5.
- **L1, L2 and L3 are unstable.** Asteroids dropped there slide away within seconds.
- L4 and L5 only hold while the star outweighs the planet by about 25 to 1 (Routh's criterion, 1875). The orbit log shows the ratio live. Set Planet mass to ×10 in the Jupiter's Trojans system and both camps break up.
- The preset's Jupiter is 10 times its real mass, so a tadpole loop takes about 20 seconds instead of about 150 years. The measured loop time matches theory, T / √(27μ/4), within 3%.
- Horseshoe orbits, which swing around L3 between L4 and L5, are only stable around much lighter planets, about 30 times lighter than this Jupiter. Real examples orbit with Earth and with Saturn's moons Janus and Epimetheus. Around a planet that light a horseshoe would take many minutes to trace, so the orrery leaves them out.

## Keyboard

| Key | Action |
| --- | --- |
| Space | Pause / resume |
| N | New random system |
| C | Clear the sky |
| M | Mute / unmute |
| E | Einstein mode on / off |
| K | Kepler mode on / off |
| L | Lagrange points on / off |
| V | Fixed or rotating view |
| T | Open the tune panel |

## How it works

- Every body pulls on every other body, the sun included. Physics runs at a fixed 240 steps per second with leapfrog (kick-drift-kick) integration, which conserves energy to about one part in a million over minutes of play.
- Presets use real mass ratios: Jupiter's moons relative to Jupiter, the TRAPPIST-1 planets relative to their red dwarf, Mercury to Mars relative to the Sun. The twelve-beat system uses Neptune-sized planets so its rhythm holds.
- The camera follows the system's centre of mass, so the sun visibly moves. The **Sun wobble** plot in the orbit log traces its path, magnified. Measuring this wobble is how astronomers found many real exoplanets.
- Einstein mode adds the first post-Newtonian correction to the sun's pull, F = GMm/r² · (1 + 3L²/(c²r²)), where L is the planet's angular momentum per unit mass. The speed of light c is set so a circular orbit at 1 au turns by the chosen angle per lap. Circular orbits placed with a tap get the slightly higher speed this extra pull needs, so they stay circular.
- The rotating view turns the canvas so the heaviest planet stays at the top. Trails are stored as they looked when drawn, so they show paths in the rotating frame, which is where tadpoles appear. Text stays level.
- A chime fires when a planet's position changes sign relative to a meridian ray. The note comes from the planet's distance at that moment, mapped onto 15 bands of the chosen scale.
- Sound is pure Web Audio: FM bells, a generated reverb impulse, stereo panning by pitch, and a compressor on the master bus. Asteroids play quiet glass notes an octave up, so a swarm crossing the meridian sounds like a strum.

See [ROADMAP.md](ROADMAP.md) for what's coming next.
