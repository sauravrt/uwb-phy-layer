# UWB PHY Layer Explorer

Interactive single-page visualization of the IEEE 802.15.4a/z Ultra-Wideband (UWB) physical layer structure.

## What it does

Lets you drill down through the UWB frame hierarchy — from a complete packet all the way to the ~2 ns pulse, the atomic unit of UWB transmission:

1. **Frame** — SHR + PHR + Payload overview
2. **Synchronization Header (SHR)** — Preamble and Start Frame Delimiter (SFD)
3. **Preamble** — Repeated symbol pattern (PSR configurable: 64–1024)
4. **Preamble Symbol** — Ternary code sequence (+1, -1, 0) with actual IEEE 802.15.4a preamble codes (codes 1–8 for 16 MHz PRF, codes 9–20 for 64 MHz PRF)
5. **Pulse** — Root Raised Cosine pulse shape with ~500 MHz bandwidth

Each level shows SVG visualizations with timing annotations, and clicking highlighted elements zooms into the next level. A side panel displays live configuration parameters, computed durations, and scale comparisons.

## Configuration

Adjustable via the side panel:

- **PRF** — 16 MHz (31-symbol codes) or 64 MHz (127-symbol codes)
- **Preamble Code** — selects specific ternary spreading code per IEEE spec
- **Preamble Length (PSR)** — 64, 128, 256, 512, or 1024 symbol repetitions

## Usage

Open `uwb-phy-explorer.html` in a browser. No dependencies or build step required.
