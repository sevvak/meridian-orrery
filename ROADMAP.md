# Roadmap

We build one step at a time. Each step is one release: it ships on GitHub Pages, works on a phone, and keeps everything that already works.

## Step 0 — New physics engine ✓

- [x] Every body has a mass, and the sun becomes a body that can move
- [x] Leapfrog integration (more accurate than the old method)
- [x] Camera follows the system's centre of mass, so the sun's wobble is real
- [x] "Planet mass" control (none, real, ×10, ×100) replaces "Planet pull"
- [x] Presets use real mass ratios (Jupiter's moons, TRAPPIST-1, inner planets)
- [x] Sun wobble plot in the orbit log

## Milestone A — Quick wins

- [ ] **1. Share links + record audio.** *(Postponed.)* The page link stores the whole system; a record button saves a sound loop.
- [x] **2. Einstein mode.** The general-relativity correction near the sun makes orbits precess and draw rosettes. Includes perihelion markers, a live turn-per-orbit readout and the Einstein's rosettes preset.
- [x] **3. Kepler's second law.** Equal-time wedges with a live equal-area readout, and ticks on a 30° dial that rush together as eccentric planets swing close to the sun. Includes the Kepler's laws preset.

## Milestone B — Three-body physics

- [x] **4. Lagrange points and Trojans.** L1–L5 marked for the heaviest planet, tap-to-drop asteroid swarms, a rotating view, a live stability readout and the Jupiter's Trojans preset. Asteroids at L4/L5 trace tadpoles. Horseshoes were left out: they are only stable around planets about 30× lighter, where they would take many minutes to trace.
- [x] **5. Planetary roses.** Choose any planet from the orbit log; a From planet view that rides on it (the geocentric sky, with retrograde loops); a Strings mode whose lines weave roses; and the Dance of Venus and Ptolemy's sky presets.
- [x] **6. Moons.** Up to three moons per planet, chiming an octave up at every full moon, drawn enlarged, with the Moons of Earth and Jupiter preset.

**Interface pass (with step 6):** tapping a planet chooses it instead of removing it, with an action bar (Add moon, Ride along, Remove); Tune became a grouped drawer and a bottom sheet on phones; a How to play card; grouped Systems menu; orbit periods shown at once; moons listed in the orbit log.

## Milestone C — A wilder sky

- [x] **7. Comets.** Weightless comets with their own finer time steps; blue ion tails and curved dust tails pointing away from the sun; ring strums that rise and fall with each pass; ice that runs out; Throw: Comet and Shift-drag; the Comets preset with a backwards Halley.
- [ ] **8. Collisions and the Roche limit.** Touching planets merge into a lower note; planets too close to the sun break into a ring.
- [ ] **9. Binary stars.** Two suns, a "Tatooine" preset, and a visible edge between chaotic and stable orbits.
- [ ] **10. Star types and habitable zone.** Red dwarf, Sun-like star or blue giant, each with its own mass, color, key and habitable zone.

## Milestone D — The real universe

- [ ] **11. Exoplanet catalog.** About 20 real systems built in (Kepler-90, HD 110067, 55 Cancri and more) with true periods.

## Dependencies

- Step 0 makes 4, 6, 8 and 9 possible.
- Step 4's rotating frame is reused in step 5.
