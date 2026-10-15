# NEURAL_FORGE

A browser-native electronics universe you can play as a kid and trust as a first-order lab for learning and prototyping.

**This is a public beta (v0.0).** It is meant for community testing. Expect rough edges. Please report what breaks.

**Live:** [https://kxz0tn.github.io/neural-forge/](https://kxz0tn.github.io/neural-forge/)

## 30-second quick start

1. Open the [live app](https://kxz0tn.github.io/neural-forge/), or download `NEURAL_FORGE_v0.0_beta.html` and open it locally.
2. Use a modern browser (Chrome, Edge, Firefox, Safari). No install. Works offline.
3. Tap a part in the left **LIBRARY**, then tap the grid to place it. Drag a pin to another pin to wire.
4. Press **Space** (or **RUN**) to simulate.
5. Switch **KID** / **ENG** in the top bar. Open **MISSION** for a guided climb from lighting an LED to mixed-signal.

On a phone: **LIB** opens the part drawer (scroll it), **INS** opens the inspector.

## What it is, and who it is for

NEURAL_FORGE is a single original HTML file: schematic editor, Modified Nodal Analysis solver, oscilloscope, optional low-poly 3D view, procedural sound, save/load, and a mission path.

- **Kids and beginners** get large targets, plain-language physics, light, and sound.
- **Students and early engineers** get numeric parameters, live voltages, netlist text, DC / transient / AC / logic, and an expandable part registry.

Same engine. One switch.

## Educational-models disclaimer

This is **not** a commercial SPICE clone and **not** a foundry compact-model tool.

Semiconductor models are educational first-order implementations of public textbook equations (Shockley diode, simplified bipolar transport, long-channel FET). They are trustworthy for learning, homework, and first-order design checks. They are **not** for tape-out, safety-critical hardware, or replacing a professional simulator.

Op-amp, 555, transmission-line, VLSI-gate, and antenna blocks are **conceptual / lumped** teaching models.

If a number must be tape-out accurate, use a professional simulator after you understand the circuit here.

## Known limitations (honest)

- Op-amp output is referenced to implicit ground (no dedicated negative-rail pin).
- BJT collector uses a saturable switch on top of a BE junction model — good as a switch, not a full curve-tracer.
- Zener reverse knee is \(V_Z\) plus ohmic series resistance.
- AC analysis is small-signal about the DC operating point.
- Matrix size is capped (about 40 unknowns on phones, 80 on desktop) so mid-range devices stay usable.
- LED hue is the only intentional color; the rest of the UI is black and white.
- On a phone the library is a drawer: open **LIB**, then scroll.

## How to report bugs / feedback

This beta is for testers. When something fails, please include:

- What you were trying to do (Kid or Engineer, 2D or 3D)
- The circuit (use **SAVE** and attach the JSON) or a clear pin-by-pin description
- What you expected vs what happened
- Browser and device (for example: “Edge on Windows”, “Safari on iPhone”)

Open an issue at [github.com/kxz0tn/neural-forge/issues](https://github.com/kxz0tn/neural-forge/issues).

## Copyright hygiene (summary)

| Check | Status |
| --- | --- |
| External dependencies | **NONE** |
| External assets (fonts, images, samples, icons) | **NONE** |
| Implementation | **Fully original** (HTML5 + CSS3 + vanilla JS + raw WebGL + Web Audio) |
| Residual copyright risk | **Negligible** |

No third-party library, font file, icon pack, audio sample, or simulator source was used. Mathematics are original implementations of public-domain scientific knowledge.

## License

MIT License. Copyright (c) 2026 kxz0tn. See [LICENSE](LICENSE).

You may use, copy, modify, merge, publish, distribute, sublicense, and sell copies, provided the copyright and permission notice stay with the software.

## This release

**NEURAL_FORGE v0.0 (beta)** is the beta build intended for community testing. Sandbox is always free. Missions are a guided path, not a lock. Extend it locally by registering a part and giving it a stamp function — no framework required.

Open the HTML. Build a circuit. Teach someone younger than you.
