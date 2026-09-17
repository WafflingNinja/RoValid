# Brag Plan: RoValid

## What is this app?
RoValid is a Roblox username availability checker that screens 200 names in a single
request, confirms the survivors one at a time, and publishes everything it finds to a
live board that a GitHub Action refreshes every 15 minutes.

## The angle
The joke the project itself makes, straight-faced: free names are not scarce — good
names are. RoValid has screened 900,000 names and the board is full of things like
`2b6b2` and `q6s6q`. So the tool stopped hoping to stumble on a good name and started
waiting for someone to give one back. A terminal readout, running at 3am, watching
3,600 names nobody is going to release. That is the game.

## Hook (first 2-3 seconds)
Near-black terminal. One line types itself in IBM Plex Mono, cursor blinking:
`every good roblox name is taken.` Nothing else on screen. The line is the premise and
the punchline of the whole video.

## Key moments (the middle)
- The two-stage table from the README arriving row by row: **stage 1 — 200 names /
  request**, then **stage 2 — 1 name / request**, with the honest caveat under it —
  *stage 2 is not optional.*
- The real board feed: rows sliding in one at a time exactly as `docs/index.html` draws
  them — `·` mark, monospace name, `5-CHAR` tag, `2d` on the right — using real names
  from `docs/hits.json`.
- The block-glyph counter from the desktop tool, drawn in `▀ █ ▄` characters, glowing
  green, landing on **185,280 FOUND** beside the `900,000 SCREENED` fact tile.
- The turn: the feed is all junk, and the watchlist tile reads `3,600 ON WATCHLIST /
  0 RELEASED` — a gold band with nothing in it yet.

## Outro / punchline
The gold `LEGENDARY` slab drops into the empty band, then the masthead:
`RoValid Live` with the accent-blue *Live*, the URL, and the site's own footer line —
*A name here may be gone by the time you read it.*

## User flow worth showing
1. **Entry** — the hunter screens a batch: 200 names go out in one request.
2. **Key action** — survivors get confirmed one at a time; the rest are free.
3. **Result** — finds land on the live board, newest and rarest first, click to copy.

## Tone
- Preset: `default`
- Creative direction: a late-night terminal readout doing its job — dry, confident, no
  marketing voice anywhere.
- Interpretation: 5 scenes, comfortable pacing, hard-ish cuts that match a terminal
  repainting rather than a deck transitioning. Lowercase monospace for the tool's own
  voice; Archivo uppercase only for labels, exactly as the site uses it. Colour is spent
  on rarity and nowhere else.

## Format: landscape — 1920x1080
## Duration: 20 seconds

## Visual identity (from the project)
- Background: `#07090D` (`--ground`), panels `#0E131C` / `#131A26`, rail `#0A0F17`
- Accent: `#4C9AFF` (`--accent`); green `#35D07F`; gold `#F5B72E`
- Text: `#DCE3EF` (`--ink`), dim `#8E9AB4`, muted `#67728C`, dead `#3C4557`
- Display font: Archivo 600/800 (uppercase labels, letter-spacing .16–.19em)
- Body font: IBM Plex Mono 400/500/600
- Strongest visual element: the feed row — `✦`/`·` mark, name, rarity tag, time-ago —
  with the gold `.slab` gradient and 2px inset bar for legendary hits.

## Share copy (draft)
RoValid has screened 900,000 Roblox usernames. Every single free one looks like
`2b6b2`. So it stopped hunting and started waiting for someone to rename.

## Audio direction
- Role: warm-but-dry bed with sparse, motion-matched accents.
- Music: `happy-beats-business-moves-vol-9-by-ende-dot-app.mp3` (or the closest cue
  preset available), low under the whole piece.
- Music treatment: starts under the hook at low volume, opens up on the counter reveal,
  holds under the feed, fades under the final masthead so the gold slab hit rings out.
- Music cue guidance: read the bundled cue preset from `assets/music/cues/`; lock the
  counter reveal and the gold-slab drop to strong cues (±0.15s). Feed rows snap to the
  beat grid but never faster than ~0.55s apart so each name stays readable.
- Audio-reactive treatment: subtle; drive the green glow behind the counter and the
  panel depth with music RMS. No waveform, no equaliser bars.
- SFX posture: sparse-to-moderate, motion-matched. Keypress ticks for the typed hook,
  card-slide per feed row, chip-stack ticks under the counter, one bell for the gold
  slab.
- Audio-coupled moments: typed hook (per-character keys), stage rows (two dry drops),
  feed rows (card slides on the beat grid), counter (stacking ticks), gold slab (single
  bell that rings into the outro).
- Restraint rule: nothing comedic, nothing stacked. The tool is not excited about
  itself; the sound should read as a machine working, not as an ad.

## Music cue guidance
- Track: bundled `happy-beats-business-moves-vol-9`; read tempo from its preset JSON.
- Strong-cue targets: counter reveal (~7s), gold-slab drop (~16.5s).
- Beat-grid window: feed rows, ~9.5s–14s, every other beat.
- Restraint: at most 2 strong-cue locks; readability wins over the grid.

## Storyboard

Cut points are beats from the track's cue preset (114.84 BPM). Total **24.10s**.

### Scene 1 — the premise — 0.00-3.18s
Full-bleed `#07090D`. A green `>` prompt and one monospace line typing itself out:
`every good roblox name is taken.` A green block caret blinks beside it.
Sequential/interaction: yes — 32-step character reveal over 1.42s, then a 1.5s hold.
Audio intent: a machine starting, not a video starting.
Audio-coupled idea: ten keypress ticks under the typing (0.24s-1.55s).
Music: bed fading in from 0.06 to 0.30.
Transition mood: hard cut -> Scene 2

### Scene 2 — how it screens — 3.18-7.40s
The README's two-stage table as two panels. `stage 1 — screen · 200 names / request ·
users.roblox.com`, then `stage 2 — confirm · 1 name / request · auth.roblox.com`, then
the caveat `stage 2 is not optional.` with `not optional` in gold.
Sequential/interaction: yes — rows slide in from the left at 3.70s and 4.75s
(beat grid), caveat at 5.81s, full set holds 1.6s.
Audio intent: dry and procedural.
Audio-coupled idea: one soft `interface/drop_*` per row.
Transition mood: clean -> Scene 3

### Scene 3 — the board — 7.40-12.65s
The live board rebuilt from `docs/index.html`: masthead (`RoValid Live`, the site's own
blurb, a green hunting pip), the hero row with the block-glyph counter running to
`185.3K FOUND` beside `900,000 SCREENED / 3,600 ON WATCHLIST / 0 RELEASED`, and the feed
panel below with four real names from `docs/hits.json`.
Sequential/interaction: yes — feed rows arrive on every other beat (7.92, 8.96, 10.01,
11.06) with the site's blue arrive flash; the counter counts up and settles on the
strong cue at 11.60s.
Audio intent: the tool visibly working.
Audio-coupled idea: a card slide per row; a chip-stack tick as the counter settles.
Transition mood: clean -> Scene 4

### Scene 4 — the turn — 12.65-16.86s
`free names are not scarce.` then, in gold, `good ones are.` Under them the measured
pair from `watchlist.py`: `183 free names sampled` / `0 without digits`.
Sequential/interaction: yes — line 1 at 12.65s (strong cue), line 2 at 14.22s, the
fact strip at 15.28s.
Audio intent: the bed thins out; space for the point to land.
Audio-coupled idea: one soft impact under line 1.
Transition mood: hard cut -> Scene 5

### Scene 5 — the wait — 16.86-21.59s
The gold release band, empty, labelled `watchlist — 3,600 names, re-checked every 15
minutes`, holding `waiting for a release`. Under it,
`they only come back when somebody renames.` A gold scan sweep crosses the band at
19.48s. The line clears, and the verdict lands: `0 released.` / `still watching.`
Sequential/interaction: yes — band 16.90s, note 17.38s, sweep 19.48s, verdict 20.53s
(strong cue).
Audio intent: one resonant hit on the verdict.
Audio-coupled idea: `impactBell_heavy_000` at 20.53s, ringing into the outro.
Transition mood: clean -> Scene 6

### Scene 6 — outro — 21.59-24.10s
`RoValid Live` in Archivo 800 with the accent-blue *Live*,
`rostikcermak-pixel.github.io/RoValid` beneath, then `that is the game.`
Audio intent: the bed fades to zero across the last 1.2s.
Transition mood: hold to black.

**Music mood for this video:** upbeat but restrained — a working bed, not a trailer.
**Audio summary:** keys start it, two dry drops explain it, card slides and a stacking
tick carry the working middle, one bell lands the verdict, and the bed fades out under
the outro.

**Duration check:** 3.18 + 4.21 + 5.26 + 4.20 + 4.74 + 2.51 = **24.10s**

## Deviations from the original plan
- Six scenes rather than five: the payoff ("0 released, still watching") earned its own
  beat rather than sharing the outro.
- Scene 3 became the whole board — masthead, hero row, feed — instead of a feed panel
  beside a counter. It shows more real UI and fills the frame.
- The site's footer line, *a name here may be gone by the time you read it*, was cut
  from the video: at 11 words it needs ~3.3s of hold and would have pushed past 25s.
  It lives in the share copy instead.
- The video never shows a legendary or released name, because the board has never held
  one. The empty gold band is the honest version of that beat.
