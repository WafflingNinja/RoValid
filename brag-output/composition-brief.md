# Hyperframes Composition Brief: RoValid

## Objective
Create a short launch-style brag video for RoValid, the Roblox username checker and
its live board.

## Output
- Composition directory: `brag-output/composition/`
- Rendered video: `brag-output/brag.mp4`
- Format: landscape — 1920x1080, 30fps
- Duration: 23.6s

## Source Material
- Project root: `/home/user/RoValid`
- Primary files read: `README.md`, `docs/index.html`, `docs/hits.json`, `rarity.py`,
  `watchlist.py`, `BENCH.md`
- Product name: RoValid / RoValid Live
- Tagline / strongest claim: *Free names are not scarce. What is scarce is a name
  anyone would want.*
- Key UI to recreate: the board's feed rows (`.line` / `.nm` / `.tag.len` / `.when`)
  and the block-glyph counter (`GLYPH` + `bigNumber` in `docs/index.html`).
- Copy that must appear verbatim or near-verbatim:
  - `stage 1 — screen · 200 names / request`
  - `stage 2 — confirm · 1 name / request`
  - `stage 2 is not optional.`
  - `free names are not scarce.` / `good ones are.`
  - `0 released.` / `still watching.`
  - `RoValid Live` · `rostikcermak-pixel.github.io/RoValid`

## Creative Direction
- Tone preset: `default`
- Creative direction: a late-night terminal readout doing its job.
- Interpretation: monospace lowercase for the tool's voice, Archivo uppercase only for
  labels, colour spent on rarity and nowhere else. Hard-ish cuts that read as a
  terminal repainting.
- Angle: free names are not scarce — good names are. The tool stopped hunting and
  started waiting.
- Hook: `every good roblox name is taken.` typed one character at a time on black.
- Outro: `0 released. still watching.` → `RoValid Live` → `that is the game.`
- Avoid: generic SaaS language, abstract filler, any redesign of the board's look,
  and any invented username or released name.

## Visual Identity
- Background: `#07090D`; panels `#0E131C` / `#131A26`; rail `#0A0F17`
- Lines: `#1D2532` / `#161D29`
- Text: `#DCE3EF`, dim `#8E9AB4`, muted `#67728C`, dead `#3C4557`
- Accent `#4C9AFF`, green `#35D07F`, gold `#F5B72E`
- Display font: Archivo 600/800, localized to `assets/fonts/`
- Body font: IBM Plex Mono 400/500/600, localized to `assets/fonts/`

## Storyboard
Creative contract: `brag-output/brag-plan.md`.

1. the premise — 3.18s — `every good roblox name is taken.` types out on black.
2. how it screens — 4.21s — the two-stage table arrives row by row + the caveat.
3. the board — 5.26s — real feed rows land one by one; the block-glyph counter runs to
   `185.3K FOUND`; `900,000 SCREENED` tile.
4. the turn — 4.20s — `free names are not scarce.` / `good ones are.` + watchlist tiles.
5. the wait — 4.20s — the empty gold release band, `0 released.` / `still watching.`
6. outro — 2.54s — `RoValid Live`, URL, `that is the game.`

## Audio
- Audio role: warm-but-dry working bed with sparse motion-matched accents.
- Audio arc: keys → two dry drops → card slides + stacking ticks → bed thins for the
  turn → one bell on the release check → fade under the outro.
- Music: `assets/music/happy-beats-business-moves-vol-9-by-ende-dot-app.mp3`
- Music treatment: 0.30 baseline, up to 0.42 across the board scene, ducked to 0.24
  for the turn, fade to 0 across the last 1.2s.
- Music cue guidance: `assets/music/happy-beats-business-moves-vol-9-by-ende-dot-app.music-cues.json`
  (114.84 BPM, 0.523s grid). Strong-cue locks: 11.5984 (counter settles), 12.6549
  (the turn), 20.5264 (the release check). Feed rows on every other beat.
- Audio-reactive treatment: subtle — per-frame RMS drives the background glow and the
  counter's green bloom. No waveform, no equaliser bars.
- Audio-coupled moments:
  - scene 1 typing — randomised-but-deterministic keypress ticks
  - scene 2 rows — one soft drop each
  - scene 3 feed rows — card slides on the beat grid
  - scene 3 counter — chip-stack tick as it settles
  - scene 4 turn — one soft impact
  - scene 5 release check — one heavy bell, rings into the outro
- SFX selection guidance: keyboard/keypress-*, interface/drop_*, casino/card-slide-*,
  casino/chips-stack-2, impact/impactSoft_medium_000, impact/impactBell_heavy_000.
- Audio files: copied into `brag-output/composition/assets/`.

## Hyperframes Instructions
Built with `hyperframes-core` (composition contract), `hyperframes-animation` (motion),
`hyperframes-creative` (audio-reactive), `hyperframes-cli` (check/render).

Requirements:
- Show real UI from the board: the feed rows and the block-glyph counter, both ported
  from `docs/index.html`.
- All text readable in the final render.
- Duration inside 15-25s.
- `npx hyperframes check` must pass before render.
