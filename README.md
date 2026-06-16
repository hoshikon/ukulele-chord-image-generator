# Ukulele Chord Diagram Generator

A single-file, client-side tool that draws ukulele chord diagrams as SVG (and exports
PNG). A 777-chord library is built in; you can also define your own shapes, save them in
your browser, and move them between machines via file export/import.

**Live:** https://hoshikon.github.io/ukulele-chord-image-generator/

Everything runs in `index.html` — no server, no build step, no dependencies. You can also
just open the file locally (double-click it, or `open index.html`).

## Usage

Type chord names in the textarea, one per line:

- **Built-in chords** — just the name: `C`, `Em7`, `F#m`.
- **Custom frets** (string order G C E A): `Em6: 0 1 0 2` — `0` = open, `x` = muted.
- **With finger numbers**: `Em: 0 4 3 2 | 0 3 2 1` (frets `|` fingers).

Each diagram has **SVG** and **PNG** download buttons. **Download all (PNG)** exports a
single sheet of everything currently shown.

### Custom chords

Use the **Add chord** form to name a shape and enter its frets/fingers. If the name
already exists (built-in or custom), your version **overrides** it.

Custom chords are saved to your browser's `localStorage`, so they persist across
sessions. To move them to another browser or machine, use **Export** to download a JSON
file and **Import** to load it elsewhere.

> Note: `localStorage` is per-origin, so chords saved while opening the file locally
> (`file://`) won't appear on the hosted page (or vice-versa). Export/import bridges them.

## Credits

- Diagram design based on [buzcarter/UkeGeeks](https://github.com/buzcarter/UkeGeeks).
- Built-in chord fingerings from the open-source [chords-db](https://github.com/tombatossals/chords-db).
