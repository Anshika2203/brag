# PR Context: #1 — Show a Stable Match score on the profile card

- Repo: Anshika2203/brag (fork; PR opened against the fork's own main, not upstream)
- Author: Anshika2203        State: open (not draft)
- Base → head: main → test/stable-match-score
- Merge base: 4068e38cb0733e42beeb74df5e3c5eee1b4e9163
- Size: +59 / -0 across 2 files
- URL: https://github.com/Anshika2203/brag/pull/1
- Metadata source: gh (addressed by URL — a bare `--pr 1` would resolve against
  the upstream parent and fail)

## What the PR says it does
"Riders had no idea why a horse was being suggested to them. The card showed a name, a
distance and a bio — nothing about fit — so every match decision came down to the photo."
The card now leads with a Stable Match percentage and the three signals behind it.

## Linked issue / request
None linked. The "why" comes from the PR body's first paragraph.

## The user-visible change
A rider swiping through horses now sees, at the top of every profile card, a
compatibility score — a filled amber ring reading **92%** next to the label **Stable
Match** and the reasons behind it: *Same turnout hours · both grazers · 2 mutual
pastures*. Before this, the card gave a name, a distance, a bio and two tags, so the
only basis for swiping was the photo. The score sits above the bio, separated by a
rule, so it is the first thing read on the card.

## Before → after
- Before: `.card-body` opened directly with `.card-bio` ("Emotionally available
  stallion...") followed by two tags. No compatibility signal anywhere on the card.
- After: `.card-body` opens with a new `.card-score` block — a 38px `conic-gradient`
  ring filled to `--score: 92`, the number `92%` in Figtree semibold ember, the label
  "Stable Match", and a one-line reason string — then the bio and tags, unchanged.

## Files that carry the change
- `examples/horse-tinder/index.html` (+9) — the `.card-score` markup inside `.card-body`
- `examples/horse-tinder/styles.css` (+50) — `.card-score`, `.score-ring` (conic-gradient
  fill driven by the `--score` custom property), `.score-num`, `.score-label`, `.score-why`

## Deliberately ignored
- Nothing. The diff is two files and 59 lines, all of it user-visible.

## Change class
ui-surface — a visible component on the product's primary screen.

## Must not claim
- No better matches, higher match rates, or more swipes — the PR renders a score, it
  does not change matching.
- The 92% is hardcoded demo content in a static mockup; there is no scoring algorithm
  in this diff.
- The match modal and the filters are untouched (the PR body says so explicitly).
