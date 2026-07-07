# CNC Lathe Threading Studio

A single-file, offline web app that programs **any kind of lathe thread** and outputs **G-code** as an `.nc` file.

## Features
- **Thread types**: Metric ISO (M, coarse & fine), Unified (UNC / UNF), Trapezoidal (Tr, 30°), Acme (29°), NPT (tapered pipe), BSPP parallel pipe (G, 55°)
- **Auto geometry**: major / minor / pitch / pitch-diameter / thread height / depth / lead / TPI
- **G-code output** in three styles:
  - Fanuc **G76** threading cycle
  - **G92** repeated multi-pass
  - **G33** single-pass (ISO)
- **Multi-start** threads, right/left hand, custom sizes
- Tuneable: stock Ø, length, lead-in, RPM, 1st/min cut, spring passes, finish allowance, chamfer
- Download `.nc` or copy to clipboard

## How to use
1. Pick a thread type and standard size (or enter a custom major Ø & pitch).
2. Set geometry (stock, length, starts) and cutting parameters.
3. Choose a G-code style and press **Regenerate**.
4. **Download .nc** and run it on your lathe (always dry-run / single-block first!).

## Run it
It is a **single self-contained `index.html`** — no server, no build, no dependencies.
- Open `index.html` directly in any browser (works offline), **or**
- Host it on any static host (GitHub Pages, Netlify, Cloudflare Pages, etc.).

## Safety
Constants suit typical stock; verify spindle direction (RH = M03, LH = M04), tool nose angle,
stock turned to major Ø, and lead-in/out before running on a machine.

## License
MIT — free to use, modify, and redistribute.
