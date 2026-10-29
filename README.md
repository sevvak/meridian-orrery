# Meridian Orrery

A gravity sandbox you play like an instrument. Throw planets around a sun, and each one chimes as it crosses the meridian line. Closer orbits ring higher notes. Because orbital periods follow Kepler's third law (period² ∝ radius³), every system you build becomes a polyrhythm.

It is a single `index.html` file with no build step and no dependencies beyond two Google Fonts. Open it in a browser and press **Start sound**.

## How to play

- **Drag** anywhere to throw a planet. A dotted line predicts its path and shows the note it will play.
- **Tap** empty sky to drop a planet into a perfect circular orbit.
- To launch **comets** instead, set Throw to Comet in Tune, or hold Shift while you drag. A tap in comet mode starts a stretched orbit from that point.
- **Tap a planet** to choose it. A dashed ring and its name appear, and a bar offers **Add moon**, **Ride along** and **Remove**. Tap it again, or press Esc, to let go.
- Press **?** for a short How to play card.
- When most of the planets line up on one ray from the sun, a **conjunction** fires a beam through them and plays a chord.

## Systems

The Systems menu is grouped into rhythms, real systems and lessons. Each preset uses real period ratios, so you hear its actual rhythm.

| System | What you hear |
| --- | --- |
| Twelve-beat alignment | Periods 1 : 2 : 3 : 4 : 6. All five line up again every twelve beats. |
| Jupiter's moons, up close | Io, Europa and Ganymede in their 1 : 2 : 4 Laplace resonance, with Callisto running free, with Jupiter in the middle. |
| Moons of Earth and Jupiter | Earth with its Moon and Jupiter with Io, Europa and Ganymede, all going round the Sun. Moons chime an octave above their planet at every full moon. |
| TRAPPIST-1 | Seven Earth-sized planets chained in resonances of 8:5, 5:3, 3:2, 3:2, 4:3 and 3:2. |
| Inner planets | Mercury to Mars at their true relative distances, read in au. |
| Einstein's rosettes | Three eccentric orbits with relativity turned up. Each ellipse slowly turns, so its meridian note walks through the scale. |
| Kepler's laws | One very eccentric planet and one circular planet with Kepler mode on. Equal-time wedges have equal areas; the ticks rush together near the sun. |
| Jupiter's Trojans | A heavy Jupiter with two camps of asteroids at its L4 and L5 points, seen from a camera that turns with it. The asteroids loop in tadpoles and strum softly as they pass the meridian. |
| Dance of Venus | Venus and Earth with Strings on. In 8 Earth years (about 30 seconds) the lines between them weave a five-petal rose. |
| Ptolemy's sky | Venus, Earth and Mars seen from Earth. The Sun circles us, Venus traces its five-petal rose, and Mars loops backwards. |
| Comets | Halley (going round backwards, as the real one does), Encke and a sungrazer among Earth and Jupiter. Each strums the rings as it falls in and climbs back out. |
| Random resonant chain | A new set of simple period ratios each time. |

## Tune

Tune opens as a drawer (a bottom sheet on phones), grouped into Sound, Gravity, Overlays and Camera. The Tune button shows how many settings differ from the defaults.

- **Scale**: D minor pentatonic, major pentatonic, hirajōshi, lydian or whole tone
- **Voice**: Bell (FM synthesis), Marimba or Glass
- **Meridians**: 1 to 4 chime lines; more lines mean denser rhythms
- **Tempo** and **Sun mass**
- **Planet mass**: None (weightless), Real (true mass ratios), ×10 or ×100. Heavier planets tug on each other and on the sun, and resonant systems drift into chaos.
- **Einstein**: Off, 3°, 10° or 30° of perihelion turn per orbit at 1 au. See below.
- **Kepler**: shows equal-time wedges and a ticking 30° dial. See below.
- **View**: Fixed; Turning, where the camera turns with the chosen planet so it stays at the top; or From planet, where the camera rides on it without turning. **Ride along** on the chosen-planet bar switches to From planet.
- **Lagrange**: marks the five Lagrange points of the chosen planet. See below.
- **Strings**: draws faint lines from the chosen planet to its neighbours. See below.

**Choosing a planet:** tap it in the sky, click its name in the orbit log, or press F to step through them. The view, Lagrange points and strings all follow it. Until you choose, the heaviest planet is used, and the orbit log says which.

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

## Planetary roses

Two old ways of drawing the solar system, both of which turn orbits into flowers.

- **Strings.** Every 0.05 s of orbit time, a faint line joins the chosen planet to its nearest neighbours. Venus goes round the Sun 13 times while Earth goes round 8, so every 8 years the pair line up in the same five places, and the lines weave a five-petal rose. Try it in **Dance of Venus**. The meetings measured in the simulation land about 144° apart, which traces a pentagram.
- **From planet.** The camera rides on a planet without turning, which is how the sky looks from Earth. The Sun circles once a year, and other planets appear to stop and loop backwards whenever one overtakes the other. Ancient astronomers saw these retrograde loops, and Ptolemy explained them with circles on circles. In **Ptolemy's sky**, Venus loops backwards 5 times in 8 years, tracing its rose, and Mars loops about every 2 years. Measured in the simulation over 8 Earth years: Venus 5.0, Mars 3.5 and Mercury 25.5 loops, against about 5, 3.7 and 25 from their real orbital periods. Mercury is left out of the preset because its loops fill the middle; add it yourself to see.

## Moons

Choose a planet and press **Add moon** (or press O). A planet holds up to three.

- A moon has to stay well inside the region its planet controls, its Hill radius, or the sun pulls it away. Moons start at a quarter to two fifths of that radius. Earth's real Moon sits at about a quarter.
- That region is only a few pixels wide on screen, so moon orbits are drawn enlarged around their planet, like the Sun wobble plot. The orbit log says by how much for each planet.
- Moons chime an octave above their planet at every full moon, when the sun, the planet and the moon line up. Inner moons ring higher.
- In **Moons of Earth and Jupiter**, the simulation gives 12.2 full moons per Earth year (the real figure is 12.4), and Io, Europa and Ganymede keep close to their 1 : 2 : 4 rhythm.
- Planets close to the sun orbit too fast for the simulation's 240 steps per second to follow a moon, so they refuse one and say why. Moons also leave if planets become weightless or a planet passes too close.

## Comets

Comets are icy, weightless bodies on long, stretched orbits.

- **They strum the rings.** Crossing one of the instrument's rings plays its note on a harp-like voice. A comet falling toward the sun crosses them faster and faster, so you hear a quickening rising run, then a falling one as it climbs back out. A comet that crosses every ring plays 30 notes per pass.
- **Two tails, both pointing away from the sun.** The blue ion tail is gas blown straight outward by the solar wind. The dust tail is grains pushed by sunlight, which weakens the sun's pull on them, so they drift outward and curve behind the comet. Both grow as the comet nears the sun and vanish far out.
- **Each pass costs ice.** Comets that come close to the sun lose ice every pass, and after many passes the tail fades and only a dark lump remains, as happens to real comets over thousands of orbits (sped up here). The orbit log shows ice left, closest approach and passes.
- **Finer time steps.** A comet near the sun moves too fast for 240 steps per second, so each comet takes up to 48 smaller steps of its own, using the sun's and planets' positions in between. Over 20 orbits of the sungrazer, this cuts the false turning of its ellipse from 4.1° to 0.13°, which matters for Einstein mode.
- You can choose a comet and ride along on it, but it is too small to hold moons or have Lagrange points.

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
| S | Strings on / off |
| V | Next view: fixed, rotating, from planet |
| F | Choose the next planet |
| O | Add a moon to the chosen planet |
| Delete | Remove the chosen planet |
| Esc | Close the top panel, or let go of the chosen planet |
| Shift-drag | Throw a comet |
| ? | How to play |
| T | Open the tune panel |

## How it works

- Every body pulls on every other body, the sun included. Physics runs at a fixed 240 steps per second with leapfrog (kick-drift-kick) integration, which conserves energy to about one part in a million over minutes of play.
- Presets use real mass ratios: Jupiter's moons relative to Jupiter, the TRAPPIST-1 planets relative to their red dwarf, Mercury to Mars relative to the Sun. The twelve-beat system uses Neptune-sized planets so its rhythm holds.
- The camera follows the system's centre of mass, so the sun visibly moves. The **Sun wobble** plot in the orbit log traces its path, magnified. Measuring this wobble is how astronomers found many real exoplanets.
- Einstein mode adds the first post-Newtonian correction to the sun's pull, F = GMm/r² · (1 + 3L²/(c²r²)), where L is the planet's angular momentum per unit mass. The speed of light c is set so a circular orbit at 1 au turns by the chosen angle per lap. Circular orbits placed with a tap get the slightly higher speed this extra pull needs, so they stay circular.
- The rotating view turns the canvas so the chosen planet stays at the top; the from-planet view moves the camera onto it. Trails are stored as they looked when drawn, so they show paths in the rotating frame, which is where tadpoles appear. Text stays level.
- Strings keep the last 2,400 lines, drawn in a few dozen strokes grouped by colour and age so they cost little to draw.
- Moons are massless and feel their planet with full-strength gravity (planets soften each other's pull at very close range to avoid wild kicks). Orbital periods in the log come from each orbit's energy, so they show at once.
- A chime fires when a planet's position changes sign relative to a meridian ray. The note comes from the planet's distance at that moment, mapped onto 15 bands of the chosen scale.
- Sound is pure Web Audio: FM bells, a generated reverb impulse, stereo panning by pitch, and a compressor on the master bus. Asteroids play quiet glass notes an octave up, so a swarm crossing the meridian sounds like a strum.

See [ROADMAP.md](ROADMAP.md) for what's coming next.
