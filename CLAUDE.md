# Late Byte

Nicola's personal indie-dev studio brand — not a single app, the umbrella
under which his own apps get released. First project under it: **Apex
Lifter** (native Android gym-tracking app, separate repo
`C:\Users\Nicola\Projects\APEX-LIFTER`, package `com.apexlifter.app`,
domain apexlifter.app/apexlifter.ch). This repo/folder is for the studio's
own identity (logo, brand assets, studio landing page) — not for any one
app's code.

**Now a real GitHub repo** (`Project-Icarus-Tactical/SAVE-STATE-Studio`,
GitHub repo names are case-insensitive so `save-state-studio` resolves
the same) — the repo's own name still says "SAVE-STATE-Studio" even
though the brand itself has been renamed to Late Byte (see below); it
was not renamed on GitHub as part of this rename, only the content was.
If asked to rename the actual GitHub repo too, that's a separate,
explicit ask — don't assume it's implied by a content rename.

## Rename: Save State Studio → Late Byte (2026-09-23)

The studio launched under the name **Save State Studio** (see the
"Save State Studio — retired name" section below for that whole design
history) and was renamed to **Late Byte** the same day the landing page
and brandbook were first built, before any of it shipped publicly.
Same founder, same story, same first product — only the name, wordmark,
and icon changed.

- **Why**: the founder wasn't fully happy with "Save State Studio" and
  asked for alternatives "die in die selbe Kerbe schlagen" (same vein:
  Feierabend/Nerd-Dad/No-Bullshit/Indie-Dev). Several names were
  brainstormed and checked (via web search + RDAP domain lookups against
  `nic.ch` and Verisign — not a full legal trademark search):
  - **Rejected — real conflicts found**: "Lullaby Logic" (an actual
    trading LLC selling paid AI baby-sleep-coaching, exact name match),
    "Lullaby Byte"/"LullaByte" (a live Google Play sleep-sounds app plus
    an older "Lullabytes" bedtime app — both close enough to be
    confusing).
  - **Rejected — thematically strong but real studios already use them**:
    "Night Shift Studio" (a solo indie dev with near-identical
    positioning already uses this exact name), "Moonshift" (an existing
    AI app-builder with the eerily similar tagline "Build Software While
    You Sleep"), "Moon Studios" (the real, known Ori-series game studio
    — avoid "Moon" as a studio name for this reason specifically).
  - **Picked: Late Byte** — domain (`latebyte.ch`) free, only a loose,
    different-category collision found ("The Latebyte", an unrelated
    tech blog/media brand, not a software studio). Given the founder's
    explicit low-stakes framing (no plans to scale beyond maybe future
    merch, and even that "in ferner Zukunft, wenn überhaupt"), that
    residual risk was judged acceptable — but this was a web search, not
    a trademark register check; redo that properly (e.g. Swissreg)
    before ever registering this as a real business entity.
- **What changed**: the wordmark ("SAVE STATE"/"STUDIO" → "LATE BYTE"/
  "STUDIO"), the icon (8-bit pixel-art floppy disk → a night scene: moon,
  a child asleep in bed, a parent still coding at a glowing laptop — see
  "Logo" below), the name-origin copy in `index.html`'s "Über mich"
  section, the contact email domain (`savestate.ch` → `latebyte.ch`).
- **What did NOT change**: the gold+red-only color decision, the
  three-principle "no bullshit" section, the two project cards (Apex
  Lifter live / Games-Backlog-Tracker in Konzeption), the tri-color→now
  two-color accent bar mechanism, the voice/tone rules, the "no violet in
  studio chrome, except a depicted product's own logo mark" exception.
  All of that is still accurate as originally documented and carries over
  unchanged — see `BRANDBOOK.md`.
- **Known gap, not yet addressed**: the separate
  [SAVE-STATE-social](https://github.com/Project-Icarus-Tactical/SAVE-STATE-social)
  repo (LinkedIn/Instagram launch kit) still uses the old name and the
  old floppy-disk icon in its generated images. It was **not** renamed
  or regenerated as part of this pass — that would mean rebuilding all
  of its image assets from scratch, which wasn't asked for. Flag this to
  the founder before that kit is actually used to set up real social
  accounts; either regenerate it under "Late Byte" first, or treat it as
  abandoned in favor of a fresh kit later.

## Website (`index.html`) and Brandbook

Explicit ask: a landing page "vom Stil her" like `apexlifter-web`'s own
marketing site — same dark background, same eyebrow/section-title
rhythm, same card patterns — but **no login/backend at all** (no `api/`,
no `konto/`, no PHP), and about the studio itself rather than any one
app. Built as a single static `index.html`, no server dependency.

- **Sections**: sticky nav (footer-lockup logo + anchor links) → hero
  (full logo + "Vollzeit-Job tagsüber. Code nach Feierabend." + the
  accent bar, see Brandbook) → "Über mich" (the actual Feierabend/
  father-of-two story, in first person) → "Der Beweis" (real code
  snippets + real GitHub commit history, see its own section below) →
  "Prinzipien" (fairer Preis / keine Ads / selbst benutzt, three cards —
  currently gold/gold/red, not one-color-per-card) → "Projekte" (two
  project cards) → footer (lockup + `info@latebyte.ch` + link back to
  apexlifter.ch).
- **Projects section currently lists two entries**:
  - **Apex Lifter** — `status-badge live` (gold), links out to
    apexlifter.ch, description pulled from that app's own positioning.
    Its project-card icon is the one deliberate exception to this site's
    gold+red-only rule — see Color decision below.
  - **Games-Backlog-Tracker** — `status-badge concept` (neutral gray, not
    a brand color), **not built, not even scoped beyond the idea** noted
    further down this file (Steam-wishlist pain point + HowLongToBeat
    integration to estimate completion % and suggest what to finish
    next). Don't treat its presence on the live site as a commitment to
    a timeline — it's explicitly "in Konzeption", surfaced because the
    founder wanted it listed, not because design/scoping has started.
- **`BRANDBOOK.md`** is the higher-level brand reference (colors, type,
  voice/tone, logo-usage quick-rules) — this `CLAUDE.md` stays the
  detailed construction record (shape coordinates, exact colors, full
  history of both the retired and current logo). Read both if touching
  brand-facing work; they're deliberately not merged, same split as
  `APEX-LIFTER`'s own CLAUDE.md vs. its Obsidian Brandbook.md.

## "Der Beweis" section: real code + real commit history

A section between "Über mich" and "Prinzipien" giving the Feierabend-
developer story visual proof instead of just words: three Android-
Studio-style code windows (`.ide-window` in `index.html`) with real,
unmodified Kotlin snippets from the Apex Lifter codebase — the Epley
one-rep-max formula (`OneRepMax.kt`), the PR-detection check
(`ActiveSessionViewModel.kt`), the `ExerciseMood` enum — syntax-
highlighted with the studio's own gold (keywords), red (numbers), a
generic light blue (types, not a brand color, chosen only for realistic
IDE contrast), and muted gray-italic (comments). Below that, a GitHub-
styled commit list (`.gh-card`) using **real commit hashes and messages**
copied from `APEX-LIFTER`'s actual `git log` at the time this was
built — don't replace these with placeholder/fake commits if this
section is ever regenerated; pull fresh real ones instead.

- **The GitHub callout's copy is autobiographical, not a visitor
  explainer.** First draft explained "what GitHub is" for non-technical
  site visitors; explicit correction: it's meant to say that the
  *founder himself* didn't know what GitHub was when he started, as
  further proof of "started from zero." Written in first person
  ("„Was ist GitHub überhaupt?" — genau das habe ich mich am Anfang
  selbst gefragt...") — keep that framing if this copy is ever touched
  again, don't drift back into a generic "here's what GitHub is" tone.
- The section's eyebrow label is "Der Beweis", not literally "Coding
  Vibe" — an earlier take used that phrase as a literal on-page label
  before the founder clarified he meant the *section should have* that
  vibe/aesthetic (which the terminal-window/GitHub-commit-list treatment
  already delivers), not that the words needed to appear as a heading.

## Color decision: gold + red, explicitly NOT violet

Explicit ask, spoken alongside the original website request: **`#E2C766`
gold + a new red only.** A first pass at this section (and the first cut
of `index.html`/`BRANDBOOK.md`) mistakenly added Apex Lifter's violet
(`#D6BBF7`) as a third studio color — **wrong, corrected same-day**. The
actual instruction: violet + gold is Apex Lifter's own brand, and this
studio needs to look clearly different from the app it ships, not share
a palette with it. Violet must never appear in the studio's own chrome
(nav, buttons, section labels, accent bar) — reusing it would defeat the
entire point of having a distinct studio identity. Picked `#E2554C` for
red (provisional — the founder separately flagged that even the *font*
choice might still change, so treat every color/type decision here as
revisit-if-it-doesn't-feel-right, not locked-in). This decision survived
the Save State Studio → Late Byte rename unchanged.

- **Red touches the current logo too**: the laptop screen's glow in the
  night-scene icon is red (`#E2554C`) — see "Logo" below. In the
  now-retired floppy-disk icon, red lived in the corner rivet notches
  only; that detail is preserved here purely as history, since the
  floppy disk itself is no longer the shipped mark.
- **The accent bar** (`.accent-bar` in `index.html`) is the studio's
  signature motif: one bar, hard-split 50/50 gold/red — same "hard
  split, not a blended gradient" convention Apex Lifter itself uses for
  its own gold→violet lockup (see that repo's CLAUDE.md Brand section),
  just with this studio's own two colors instead.
- **One deliberate, narrow exception**: the Apex Lifter project-card
  icon (the mini mountain-peak polyline inside "Projekte") keeps that
  product's own real gold+violet duotone — it briefly got flattened to
  gold-only during the violet cleanup, then explicitly restored
  ("das Apex-Lifter-Logo soll exakt das Original sein, in seinen
  Farben. Aber nur das."). The reasoning: this one icon *depicts*
  Apex Lifter itself, a genuinely violet-branded product, so it should
  show that product's true colors — unlike every other violet use on
  this page, which was the *studio's own* chrome wrongly borrowing
  Apex Lifter's palette. Don't generalize this back out to "violet is
  okay here after all" — it's this one icon, nothing else.
- **`SAVE-STATE-social`** (LinkedIn/Instagram launch assets, separate
  repo) predates the red accent entirely and currently uses only gold +
  gray — no violet, so it was never wrong on the color question, just
  incomplete next to this brandbook. It's now also out of date on the
  *name* — see the Rename section above.

## Logo

**Source of truth**: `assets/logo/logo-full.svg` (hero lockup),
`assets/logo/logo-footer.svg` (compact lockup), `assets/logo/icon-only.svg`
(just the scene, no wordmark — for favicons/app icons). `assets/logo/preview.html`
renders all three via `<img>` tags for quickly eyeballing changes — not
itself a usage-ready asset. **If the logo needs changing, edit these
three SVG files directly (the shape coordinates are hand-tuned) rather
than redrawing from scratch**, and keep `index.html`'s three inline
copies (nav, hero, footer — it doesn't reference the SVG files, it
duplicates their markup inline for each spot) in sync manually if the
artwork changes.

- **Two lockups, not one.** "Hauptlogo" (hero use): two-line wordmark
  centered above the scene. "Fusszeile" (footer/compact use): scene on
  the left, two-line wordmark beside it. Both share the exact same scene
  artwork at different scales — keep them in sync if the scene changes.
- **Wordmark is always two lines**: "LATE BYTE" (off-white `#e8e8ea`,
  weight 800, small letter-spacing) on top, "STUDIO" (brand gold
  `#E2C766`, weight 700, wide letter-spacing ~4-6) below. Don't merge
  into one line or swap which word gets the gold — gold-for-STUDIO is
  the established accent placement, carried over unchanged from the
  retired Save State Studio wordmark.
- **Font: Manrope** (Google Fonts, SIL Open Font License — cleared for
  commercial/logo use). Same font family as the Apex Lifter app itself,
  keeping studio and first-product visually related without being
  identical.

### Icon: minimalist crescent moon (current, 2026-09-23)

**Third and current mark, replacing the night scene below** — a single
abstract symbol, arrived at after the night-scene illustration (moon +
sleeping child + coding parent) was explicitly rejected as "der falsche
Weg" once actually built and seen at size ("das baby sieht komisch aus,
woher kommt der kopf?... die darstellung des vater am notebook passt mir
gar nicht"). The founder asked for "einen minimalistischeren Ansatz" —
first tried as a single symbol *fusing* the moon with a second code-
themed element (cursor, chevron, slash, terminal-`>`; see
`draft4.html` in that session's scratchpad for all four), which was
also rejected as "zu unruhig... es soll simpler, ohne billig zu wirken".
The founder then picked variant "G" from a follow-up set of four
moon-only variants (`draft5.html`) with the direction "nimm dein
Favorit" — **a crescent moon alone, nothing else**: no bed, no parent,
no laptop, no second fused element. This is deliberately the *opposite*
direction from "make it more complex/3D" (an earlier, since-abandoned
ask during the night-scene phase) — don't reintroduce detail or a second
symbol into this mark without an explicit new ask; the whole point of
this iteration was paring down, not building up.

| Element | Value | Notes |
|---|---|---|
| Ambient glow | Radial gradient, `#E2C766` 45%→0% opacity | Centered behind the moon, `r` roughly 1.5–1.6× the moon's own radius — soft moonlight halo, not a hard-edged ring. |
| Moon fill | Linear gradient, `#D2A233` (bottom-left) → `#F9EBC0` (top-right) (`x1=0% y1=100%` → `x2=100% y2=0%`) | A diagonal gradient, not flat gold — this is what gives the crescent visual depth/"3D-adjacent" richness without any actual shading/bevel work, addressing the earlier "sieht billig aus" line-art feedback from a different angle (richer fill instead of more elements). |
| Moon shape | `<mask>`: white circle (`r=28`, full moon shape) minus a black circle (`r=24`, offset up-right) | **The established crescent technique for this project** — see the retired night-scene section below for why a subtractive same-background-color circle doesn't work (it paints a flat patch over the ambient glow instead of letting it show through). A `<mask>` keeps the bitten-out area genuinely transparent. |
| Self-glow filter | `feGaussianBlur` (`stdDeviation` 1.6 at 100-unit scale, 2.2 at the larger `logo-full.svg` scale) merged with the source shape | A soft blur-and-merge behind the crisp moon itself, not just the separate ambient radial glow behind it — this is what reads as the crescent gently glowing from within, distinct from the ambient ombré wash around it. Two separate glow layers, don't collapse them into one. |

- **Exact coordinates are per-file, hand-tuned to each viewBox**, not one
  shared number scaled uniformly — `icon-only.svg` (100×100 viewBox,
  moon at `cx=44 cy=50 r=28`), `logo-footer.svg` (260×70 viewBox, moon at
  `cx=35 cy=35 r=20`), `logo-full.svg` (220×260 viewBox, moon at
  `cx=102 cy=172 r=38`). If resizing any lockup, keep the mask's second
  (bite) circle's offset proportionally similar (~+13/-12 x/y relative to
  the main circle's radius) rather than reusing a raw pixel offset from a
  different-sized file.
- **Wordmark colors are unchanged from the two-line convention above**
  ("LATE" white `#e8e8ea`, "BYTE" red `#E2554C`, "STUDIO" gold
  `#E2C766`) — the founder confirmed these three exact color/word
  pairings explicitly ("aber die farben sind perfekt - bildschirm rot -
  mond gold und dann late weiss - byte in rot und studio in gold") while
  reviewing the (since-abandoned) night-scene draft; they carried forward
  unchanged into this minimalist mark. Note "BYTE" red is a **new,
  explicit split** from the wordmark's earlier single-color "LATE BYTE"
  treatment further up this file — if touching the wordmark text, keep
  "LATE " and "BYTE" as separate `<tspan>`s with different fills, don't
  collapse back into one uniform-color run.
- **`index.html`'s three inline copies (nav/hero/footer) and the three
  `assets/logo/*.svg` files were all updated together** to this mark —
  there is no remaining reference to the night-scene or fused-symbol
  concepts anywhere in the shipped site. Keep them in sync manually if
  this mark changes again (same manual-sync caveat as the "Logo" section
  above already documents).

### Icon: night scene — moon, sleeping child, coding parent (retired, 2026-09-23)

**Second mark, retired the same day it was built** — replaced by the
minimalist crescent moon above almost immediately after this direction
was actually seen at real size (not rejected on the concept, but on the
execution — see the rejection quotes in the section above). Kept in full
below purely as design history, same reasoning as the floppy-disk
section further down — a flat-color illustrated scene directly depicting
the studio's own story, drawn from the founder's own description: "ein
Mond, daneben Kind im Bett und Vater am Laptop am Coden." Built as plain
`<circle>`/`<rect>`/`<path>` shapes (no `<img>`, no external assets), so
it stays crisp at any size and matches the existing "hand-authored SVG,
not a raster export" convention this project already used for the
floppy disk.

| Element | Color | Notes |
|---|---|---|
| Ambient gold glow | `#E2C766`, low-opacity radial gradient | Centered behind the moon/bed side of the scene — this is moonlight, not a generic UI glow. |
| Ambient red glow | `#E2554C`, low-opacity radial gradient | Centered behind the laptop-screen/parent side — this is the laptop's own light, not a generic accent. Keep the gold/red split spatially tied to "moon side" vs. "screen side"; don't blend them into one central glow, that loses the narrative pairing documented in `BRANDBOOK.md`. |
| Stars | `#E2C766`, small circles (r≈1.3-1.8), varying opacity 0.5-0.8 | Purely decorative sky texture, scattered near the moon. |
| Moon | `#E2C766` crescent | **Built via an SVG `<mask>`, not a subtractive same-bg-color circle.** A first attempt drew a second circle filled with the flat background color (`#1C1C1E`) to "bite" a crescent out of a full gold circle — this looked wrong wherever the ambient glow gradient was behind it, since the flat bg-colored circle painted a visible dark patch over the glow instead of letting it show through. Fixed by using a `<mask>` (white circle = moon shape, black circle = the bite) applied to the gold circle instead — the masked-out area becomes truly transparent, so whatever glow is behind it shows through naturally. **Reuse the mask technique, not a subtractive same-color circle, for any future crescent/bite shape in this project.** |
| Bed frame + blanket | `#ece6d8` (bed), `#d8d4c8` (blanket fold/headboard) | Simple rounded-rect shapes, not a detailed illustration — same "abstracted pictogram, not a realistic figure" treatment as the sleeping child. |
| Child's head | `#d8d4c8` | A plain circle peeking above the blanket — deliberately not rendered in any specific skin tone or with facial features, kept as an abstract pictogram like the rest of the scene. |
| Parent's head + torso | `#3a3a40` | Reused directly from the retired floppy disk's own body color, for continuity between the old and new mark's silhouette tone. Plain circle (head) + rounded rect (torso) — same abstraction level as the child, no facial features. |
| Laptop base/frame | `#2a2a2e` | Reused from the floppy disk's shutter-slot color. |
| Laptop screen | `#E2554C` (studio red) | The one deliberate splash of full-opacity red in the mark — this is "the screen's own light," tying directly into the red ambient glow around it. |

- **Composition gotcha hit while building this**: the parent's torso and
  the laptop screen were first positioned to nearly overlap (same x/y
  footprint), and rendered as one confusing reddish blob instead of two
  readable objects. Fixed by giving them clearly separated x-ranges (torso
  to the left/behind, laptop screen to the right/in front, meeting only
  at the narrow "hands on keyboard" area) — if this scene is ever
  redrawn, keep the parent and the laptop visually distinct rather than
  stacking their bounding boxes.
- **The small icon-only variant drops the parent figure entirely**,
  keeping just the moon + bed + a small laptop-screen hint — at
  favicon/tiny-inline sizes a third silhouette made the composition too
  busy to read; the moon and bed alone (plus the red screen glint) still
  communicate "night, someone's still coding" at a glance. The full
  parent figure is reserved for the hero (`logo-full.svg`) and footer
  (`logo-footer.svg`) lockups, which have more room.
- No gradients on the silhouette shapes themselves (bed, parent, laptop
  base) — flat color blocks only, gradients are reserved for the two
  ambient glows. This keeps the same "flat pixel-art-adjacent" reading
  the floppy disk had, even though this mark isn't literally pixel-art.

## Save State Studio — retired name (history only, 2026-09-22 → 2026-09-23)

Everything below this point describes the **original** studio identity,
before the rename above. Kept in full because the reasoning (why the
floppy disk looks the way it did, what was tried and rejected) is
genuinely useful design history and the same lessons (e.g. the Vecteezy
stock-art caution, the mask-vs-subtractive-circle technique) generalize
to future work — but none of this describes what currently ships.

**Name origin (retired)**: "Save State" is the gaming term for a
save-point/snapshot — deliberate, since the founder described himself
(unprompted, while brainstorming studio names) as "im Grunde ein
absoluter Nerd, der für das Gaming liebt, lebt und stirbt", alongside
being a father of two working full-time who also lifts. The name was
meant to read as a nod to that gaming identity, not just a generic
"save"/productivity pun.

### Icon (retired): 8-bit pixel-art floppy disk

Final direction after several rejected approaches (see History below) —
a flat, hard-edged pixel-art floppy disk, explicitly chosen over a
realistic/detailed diskette illustration for a stronger "Gaming-Flair".
Built on an 80×80 local-unit grid using plain `<path>`/`<rect>` elements
(no curves), rendered with `shape-rendering="crispEdges"` so edges stay
hard rather than getting anti-aliased soft.

| Element | Color | Notes |
|---|---|---|
| Body | `#3a3a40` | Stepped top-right corner cut, drawn as an explicit path (not a rect + erase-hack), so its own outline traces the step correctly. |
| Outline | `#0d0d0f`, stroke-width 3 | Only on the body path and the shutter rect — not on every element. |
| Shutter (metal slider) | `#d8d4c8` | |
| Shutter's inner dark slot | `#2a2a2e` | No stroke. |
| Label | `#ece6d8` | Full, unbroken rectangle — see the corner-notch note below. |
| Label's top accent stripe | `#E2C766` (brand gold) | Deliberate substitution — generic floppy-icon art usually has a red stripe here; gold ties it to the brand instead. Inset 2 units in from the label's own top/left/right edges (`x=10,y=34,w=60,h=6` against a label of `x=8,y=32,w=64,h=44` with a 3-unit border stroke) — this inset is load-bearing: without it, the gold fill paints over the label's own black border stroke at the top corners, since SVG strokes are centered on the path. |
| Label "text line" dashes | `#a39d8c` | Decorative, suggest handwritten label text. |
| Corner rivet notches | `#E2554C` (studio red) | Sit on the disk body's own bottom edge (`x=2` / `x=74` in the 80-unit grid), outside the label's horizontal range (`x=8` to `x=72`). Originally `#2a2a2e` dark gray, recolored to studio red once the gold+red decision was made — the one place red touched this mark. Also: this was a real bug when the notches were gray — they originally overlapped the label's bottom corners, making the label look cut into. |

- No gradients, no glow, no 3D shading in the shipped version — flat
  color blocks only. This was a deliberate end state, not a placeholder:
  soft-3D bevel shading, then a full isometric-extrusion "rendered" look,
  then a monochrome technical-drawing/blueprint treatment (hatching,
  dimension lines, centerlines) were all tried and explicitly moved away
  from — see History below.

#### History (why the floppy disk looked like this, not something else)

Useful if a future project needs a similar pixel-icon design pass —
several directions were tried and rejected for specific reasons, not
arbitrarily:

1. Started from a Gemini-generated "diskette with a label" SVG mockup
   where the founder wanted the "SAVE STATE STUDIO" text properly
   centered on the label (it originally overflowed the label's edges).
2. Refined to calmer, thinner line art with a few "nerdy" authenticity
   details (corner rivets, brushed-metal hatch marks, a second HD-density
   hole, tiny "3.5" HD" micro-print) — explicit feedback was that the
   first pass's lines were too thick and the metal-shutter glow too
   flashy.
3. Tried a "leichtes 3D" soft-gradient bevel + a small film-visible window
   in the shutter. The window shape was corrected from a wide pill to a
   tall rectangle per feedback ("ein hohes Rechteck").
4. Tried a full isometric-extrusion 3D look (filled top/side faces with
   gradients suggesting real thickness, inspired by a stock isometric
   floppy-disk illustration the founder shared for reference).
   **Rejected**: lines too thick, 3D effect far too strong ("sollte
   vielleicht ein Viertel so stark sein").
5. Tried a monochrome "technical drawing / blueprint" treatment instead
   of shaded 3D: pure line art, 45°-hatch pattern fills on cut/exposed
   surfaces instead of gradients, plus an ISO-style dimension line and
   centerline. This was a legitimate, well-received direction on its own
   terms, but the founder then pivoted away from a detailed/realistic
   diskette illustration entirely in favor of approach 6.
6. **Pivot**: drop the detailed diskette illustration altogether, go
   with a two-line wordmark + a simple 8-bit pixel-art floppy icon
   instead, explicitly for more "Gaming-Flair". This shipped as the
   Save State Studio mark.
7. Founder supplied two Vecteezy stock "floppy disk" images (free-license
   downloads) as style inspiration for the pixel icon. **Important:
   the actual stock artwork/EPS files were never traced or reused** —
   Vecteezy's free license (per its own included license PDF) requires
   attribution and does not clear use as a trademark/logo; using someone
   else's stock art as a business's own logo would be a real risk
   regardless of the "free" download tier. Instead only generic, non-
   copyrightable genre conventions were carried over (bold dark outline,
   chunky pixel blocks, stepped corner cut, two-tone shutter with a dark
   slot, label with a colored top stripe and text-line dashes, small
   corner rivet notches), redrawn from scratch in the studio's own
   colors. **If more stock-site references get shared for this or any
   future project, take general style/composition inspiration only —
   never trace or directly derive artwork from the copyrighted file
   itself.** This caution applies regardless of which icon concept is
   current.
8. Two bugs found via direct visual feedback on the final pixel design
   and fixed (both documented in the icon table above): the corner rivet
   notches overlapping the label's edge, and the gold stripe bleeding
   over the label's border stroke.
9. **Retired entirely (2026-09-23)** in favor of the night-scene icon
   documented above, per the founder's own logo concept — which was
   itself retired the same day in favor of the current minimalist
   crescent moon (see that section above); this floppy disk was never
   actually live on the shipped site.

## Licensing / legal status

- The retired floppy-disk mark, the retired night-scene mark, and the
  current minimalist crescent-moon mark are all original artwork — not
  traced or derived from any stock asset (see History item 7 above for
  the specific care taken there).
- Manrope is SIL Open Font License — fine for commercial/logo use, no
  attribution required.
- **No trademark search or registration has been done** for either
  "Save State Studio" or "Late Byte" — the naming due-diligence
  described in the Rename section above was a web search + domain
  lookup, not a legal trademark search. Flagged to the founder as an
  optional future step (e.g. the Swiss IGE trademark register /
  Swissreg, or a lawyer if the studio grows beyond casual indie
  release) — not something either of us has done, don't imply otherwise
  if asked later.

## Other studio ideas mentioned in passing

Noted here only as background context, not a spec or commitment: the
founder mentioned a second possible future app idea under this studio —
a game backlog/wishlist tracker (motivated by Steam wishlists becoming
unmanageable), integrating with HowLongToBeat data to estimate
completion percentage and suggest what to finish first. This is now
also listed on the live site's "Projekte" section as "Games-Backlog-
Tracker, in Konzeption" — still nothing designed or built beyond the
idea itself.
