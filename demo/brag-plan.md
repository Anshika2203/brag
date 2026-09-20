# Brag Plan: Horse Tinder — PR #1

## What is this app?
Horse Tinder is a swipe-based dating app for horses: profile cards with a photo, a
distance, a bio and hay preferences, and a "It's a neigh!" match moment.

## What changed
Riders can now see *why* a horse is being suggested — a Stable Match score sits at the
top of every profile card, above the bio.

## Before → after
- Before: `.card-body` opened with the bio ("Emotionally available stallion…") and two
  tags. Nothing on the card spoke to fit, so swipes came down to the photo.
- After: a 92% amber ring, the label "Stable Match", and the reasons behind it —
  *Same turnout hours · both grazers · 2 mutual pastures* — sit above the bio, divided
  by a hairline rule.
- Proof moment: the score block landing on the card the viewer has already been looking
  at for four seconds, with the ring filling 0 → 92.
- Must not claim: better matches, higher match rates, or any scoring algorithm. The
  diff renders a score on a static mockup. The match modal and filters are untouched.
- PR: #1 — open, in review.

## The angle
The viewer watches a rider stall on a card that tells them nothing, then watches the
card answer the question. No launch language, no metrics — the card does the arguing.

## Hook (first 2-3 seconds)
"Riders were swiping on the photo." Plain sentence, the product's cream background,
nothing else on screen.

## Key moments (the middle)
- The real card, as it shipped before: photo, "Thunder, 8", 2.4 mi away, bio, two tags.
  A cursor hovers over the like button and doesn't commit.
- The score block arrives above the bio: ring fills 0 → 92, "Stable Match" sets, the
  three reasons type in.
- The cursor commits to the like.

## Outro / punchline
"Tell a 92% from a 41% before you swipe." Then the PR marker: `#1 · in review`.

## User flow worth showing
Entry → the rider reads a card → the card now answers "why this horse?" → the swipe.
The centerpiece is the card itself, recreated from `examples/horse-tinder/index.html`
at both base and head.

## Tone
- Preset: changelog
- Creative direction: an honest product update — the card, before and after, and
  nothing else
- Interpretation: calm pacing, mixed-case type, one line of copy per beat. The
  before/after cut carries the emphasis instead of the typography. No exclamation, no
  claim the diff can't back.

## Format: landscape — 1920x1080
## Duration: 20.2 seconds

## Visual identity (from the project)
- Background: `oklch(96% 0.018 78)` (--cream)
- Accent: `oklch(73% 0.150 62)` (--amber); deep accent `oklch(50% 0.150 42)` (--ember)
- Text: `oklch(22% 0.034 50)` (--text); muted `oklch(56% 0.038 58)` (--text-3)
- Border: `oklch(87% 0.034 72)`
- Display font: Libre Baskerville (serif, italic for emphasis)
- Body font: Figtree
- Strongest visual element: the phone card itself — rounded photo, "Verified" pill,
  amber tag chips

## Share copy (draft)
Riders can finally see why a horse is being suggested — Stable Match now sits at the
top of the profile card, with the three signals behind it. Shipped in #1.

## Audio direction
- Role: warm bed, low and steady; sparse professional accents
- Music: `happy-beats-business-moves-vol-10-by-ende-dot-app.mp3` (110 BPM, 60s)
- Music treatment: in at 0.0s, volume 0.28, fade under the outro line from 17.5s
- Music cue guidance: preset read from `<skill-dir>/assets/music/cues/`. Beat grid
  0.545s apart. Lock the before→after landing to the beat at **7.79s**; lock the outro
  card to the strong cue at **15.82s**. Sequential reason lines use every other beat
  (~1.09s apart) so each stays readable.
- Audio-reactive treatment: none. The tone is restraint; a breathing UI would undercut
  the honesty of the before/after.
- SFX posture: sparse — one soft click for the score block landing, one lighter tick
  per reason line, one click on the like press. Nothing on the text scenes.
- Audio-coupled moments: the score block arrival, the three reason lines, the like press
- Restraint rule: no swells, no risers, no impact hits. This is a product update, not a
  trailer.

## Storyboard

### Scene 1 — The problem — 3.4s
Cream field. "Riders were swiping on the photo." sets in Libre Baskerville, holds.
Second line in Figtree, muted: "Nothing on the card said why."
Sequential/interaction: two lines, second at +1.4s
Audio intent: music establishes quietly, nothing else
Audio-coupled idea: none
Music: warm bed in
Transition mood: clean → Scene 2

### Scene 2 — Before — 4.4s
The real profile card, recreated from the base branch: photo, "Thunder, 8", "2.4 mi
away", "Verified", bio, two hay tags. A small "Before" chip sits top-left. A cursor
drifts to the like button and hesitates there — no commit.
Sequential/interaction: yes — cursor approaches the like button and stalls
Audio intent: unresolved, holding
Audio-coupled idea: none — silence around the cursor makes the stall read
Music: bed continues
Transition mood: hard cut on the beat → Scene 3

### Scene 3 — After — 6.8s
Identical frame, identical card position. The "Before" chip swaps to "After". The score
block pushes in above the bio: the amber ring fills 0 → 92 with the number counting up,
"Stable Match" sets beside it, then the three reasons arrive one at a time — Same
turnout hours · both grazers · 2 mutual pastures. The cursor commits to the like.
Sequential/interaction: yes — ring count-up, then 3 reason items on every other beat,
then the like press
Audio intent: arrival and resolution, still quiet
Audio-coupled idea: soft click on the block landing (beat-locked 7.79s), light tick per
reason line, click on the like press
Music: bed continues
Transition mood: clean → Scene 4

### Scene 4 — What it unlocks — 5.6s
Cream field. "Tell a 92% from a 41% before you swipe." Below it, small and muted:
`#1 · in review`. The card sits reduced at the right edge, still showing the score.
Sequential/interaction: line, then the PR marker at +1.6s
Audio intent: settle and fade
Audio-coupled idea: none
Music: fade from 17.5s to silence at 20.2s
Transition mood: hold to end

**Music mood for this video:** calm, warm, unhurried
**Audio summary:** A low warm bed runs the whole length, three small UI sounds mark the
only moments that matter, and the music fades out under the closing line.
