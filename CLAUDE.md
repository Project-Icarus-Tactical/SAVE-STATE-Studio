# Save State Studio

Nicola's personal indie-dev studio brand — not a single app, the umbrella
under which his own apps get released. First project under it: **Apex
Lifter** (native Android gym-tracking app, separate repo
`C:\Users\Nicola\Projects\APEX-LIFTER`, package `com.apexlifter.app`,
domain apexlifter.app/apexlifter.ch). This repo/folder is for the studio's
own identity (logo, brand assets, studio landing page) — not for any one
app's code.

**Now a real GitHub repo** (`Project-Icarus-Tactical/SAVE-STATE-Studio`,
GitHub repo names are case-insensitive so `save-state-studio` resolves
the same) — the "not a git repo yet" note below is stale, left in place
only because the History section below it still reads correctly as a
record of how the logo evolved.

## Website (`index.html`) and Brandbook (2026-09-23)

Explicit ask: a landing page "vom Stil her" like `apexlifter-web`'s own
marketing site — same dark background, same eyebrow/section-title
rhythm, same card patterns — but **no login/backend at all** (no `api/`,
no `konto/`, no PHP), and about the studio itself rather than any one
app. Built as a single static `index.html`, no server dependency.

- **Sections**: sticky nav (footer-lockup logo + anchor links) → hero
  (full logo + "Vollzeit-Job tagsüber. Code nach Feierabend." + the
  tri-color accent bar, see Brandbook) → "Über mich" (the actual
  Feierabend/father-of-two/gamer story, in first person) → "Prinzipien"
  (fairer Preis / keine Ads / selbst benutzt, three cards in
  gold/violet/red) → "Projekte" (two project cards) → footer (lockup +
  `info@savestate.ch` + link back to apexlifter.ch).
- **Projects section currently lists two entries**:
  - **Apex Lifter** — `status-badge live` (gold), links out to
    apexlifter.ch, description pulled from that app's own positioning.
  - **Games-Backlog-Tracker** — `status-badge concept` (violet), **not
    built, not even scoped beyond the idea** noted further down this
    file (Steam-wishlist pain point + HowLongToBeat integration to
    estimate completion % and suggest what to finish next). Don't treat
    its presence on the live site as a commitment to a timeline — it's
    explicitly "in Konzeption", surfaced because the founder wanted it
    listed, not because design/scoping has started.
- **`BRANDBOOK.md`** is the new higher-level brand reference (colors,
  type, voice/tone, logo-usage quick-rules) — this `CLAUDE.md` stays the
  detailed logo-construction record (grid, exact colors, rejected
  directions). Read both if touching brand-facing work; they're
  deliberately not merged, same split as `APEX-LIFTER`'s own CLAUDE.md
  vs. its Obsidian Brandbook.md.

### Color decision: gold + red, explicitly NOT violet

Explicit ask, spoken alongside the website request: **`#E2C766` gold +
a new red only.** A first pass at this section (and the first cut of
`index.html`/`BRANDBOOK.md`) mistakenly added Apex Lifter's violet
(`#D6BBF7`) as a third studio color — **wrong, corrected same-day**.
The actual instruction: violet + gold is Apex Lifter's own brand, and
Save State Studio needs to look clearly different from the app it
ships, not share a palette with it. Violet must never appear in the
studio's own chrome (nav, buttons, section labels, accent bar) —
reusing it would defeat the entire point of having a distinct studio
identity. Picked `#E2554C` for red (provisional — the founder
separately flagged that even the *font* choice might still change, so
treat every color/type decision here as revisit-if-it-doesn't-feel-
right, not locked-in).

- **Red never touches the logo icon itself** — the icon's gold label
  stripe is a deliberate brand substitution for the generic red stripe
  real floppy-disk icons usually have (History item 7 below); reusing
  red there would undo that specific choice. Red lives only in
  page-level accents: half the accent bar, one icon fill on the
  "Prinzipien" cards, the Games-Backlog-Tracker project icon.
- **The accent bar** (`.accent-bar` in `index.html`) is the studio's
  signature motif: one bar, hard-split 50/50 gold/red — same "hard
  split, not a blended gradient" convention Apex Lifter itself uses for
  its own gold→violet lockup (see that repo's CLAUDE.md Brand section),
  just with the studio's own two colors instead.
- **The Apex Lifter project-card icon is intentionally gold-only now**,
  not gold+violet — an earlier version echoed Apex Lifter's own
  gold/violet duotone on its mini mountain-peak icon inside the
  "Projekte" section, which was removed for the same reason as
  everywhere else: no violet on this site, full stop, even when the
  icon is *depicting* a violet-branded product.
- **`SAVE-STATE-social`** (LinkedIn/Instagram launch assets, separate
  repo) predates the red accent entirely and currently uses only gold +
  gray — no violet, so it was never wrong, just missing red. Add red
  there too if it's ever revisited; nothing needs undoing.

Name origin: "Save State" is the gaming term for a save-point/snapshot —
deliberate, since the user described himself (unprompted, while
brainstorming studio names) as "im Grunde ein absoluter Nerd, der für das
Gaming liebt, lebt und stirbt", alongside being a father of two working
full-time who also lifts. The name is meant to read as a nod to that
gaming identity, not just a generic "save"/productivity pun.

This folder is not a git repo yet — the user will create the actual
GitHub repository separately and drop this folder's contents into it.
Don't assume a remote exists.

## Logo

**Source of truth**: `assets/logo/logo-full.svg` (hero lockup),
`assets/logo/logo-footer.svg` (compact lockup), `assets/logo/icon-only.svg`
(just the disk, no wordmark — for favicons/app icons). `assets/logo/preview.html`
is a side-by-side preview of both lockups on the studio's dark background,
for quickly eyeballing changes — not itself a usage-ready asset.
**If the logo needs changing, edit these files directly (the path/rect
coordinates are hand-tuned, see below) rather than redrawing from
scratch.**

- **Two lockups, not one.** "Hauptlogo" (hero use): two-line wordmark
  centered above the icon. "Fusszeile" (footer/compact use): icon on the
  left, two-line wordmark beside it. Both share the exact same icon
  artwork at different scales — keep them in sync if the icon changes.
- **Wordmark is always two lines**: "SAVE STATE" (off-white `#e8e8ea`,
  weight 800, small letter-spacing) on top, "STUDIO" (brand gold
  `#E2C766`, weight 700, wide letter-spacing ~4-6) below. Don't merge
  into one line or swap which word gets the gold — gold-for-STUDIO is
  the established accent placement throughout every iteration of this
  logo.
- **Font: Manrope** (Google Fonts, SIL Open Font License — cleared for
  commercial/logo use). Same font family as the Apex Lifter app itself,
  keeping studio and first-product visually related without being
  identical.

### Icon: 8-bit pixel-art floppy disk

Final direction after several rejected approaches (see History below) —
a flat, hard-edged pixel-art floppy disk, explicitly chosen over a
realistic/detailed diskette illustration for a stronger "Gaming-Flair".
Built on an 80×80 local-unit grid using plain `<path>`/`<rect>` elements
(no curves), rendered with `shape-rendering="crispEdges"` so edges stay
hard rather than getting anti-aliased soft. Exact colors (don't
approximate from memory — copy from the SVG files):

| Element | Color | Notes |
|---|---|---|
| Body | `#3a3a40` | Stepped top-right corner cut, drawn as an explicit path (not a rect + erase-hack), so its own outline traces the step correctly. |
| Outline | `#0d0d0f`, stroke-width 3 | Only on the body path and the shutter rect — not on every element. |
| Shutter (metal slider) | `#d8d4c8` | |
| Shutter's inner dark slot | `#2a2a2e` | No stroke. |
| Label | `#ece6d8` | Full, unbroken rectangle — see the corner-notch note below. |
| Label's top accent stripe | `#E2C766` (brand gold) | Deliberate substitution — generic floppy-icon art usually has a red stripe here; gold ties it to the brand instead. Inset 2 units in from the label's own top/left/right edges (`x=10,y=34,w=60,h=6` against a label of `x=8,y=32,w=64,h=44` with a 3-unit border stroke) — **this inset is load-bearing**: without it, the gold fill paints over the label's own black border stroke at the top corners, since SVG strokes are centered on the path. Keep at least this margin if the stripe or label size ever changes. |
| Label "text line" dashes | `#a39d8c` | Decorative, suggest handwritten label text. |
| Corner rivet notches | `#2a2a2e` | Sit on the disk **body's** own bottom edge (`x=2` / `x=74` in the 80-unit grid), **outside** the label's horizontal range (`x=8` to `x=72`). This was a real bug: they originally overlapped the label's bottom corners, making the label look cut into. Any future detail added near the bottom corners must stay clear of the label's x-range for the same reason. |

- No gradients, no glow, no 3D shading in the shipped version — flat
  color blocks only. This is a deliberate end state, not a placeholder:
  earlier in the same session, soft-3D bevel shading, then a full
  isometric-extrusion "rendered" look, then a monochrome technical-
  drawing/blueprint treatment (hatching, dimension lines, centerlines)
  were all tried and explicitly moved away from — see History. Don't
  reintroduce shading/gradients/3D on this icon without checking first;
  flat pixel-art is the current direction, chosen on purpose.
- **Default presentation**: studio dark background `#1C1C1E` (same value
  as Apex Lifter's app background), lockups optionally shown on a
  slightly lighter card (`#141416` fill, `#2a2a2e` 1px border, 12px
  radius) — this card is a presentation convenience for the preview page,
  not part of the logo itself.

### History (why it looks like this, not something else)

Useful if asked to change the logo again — several directions were tried
and rejected for specific reasons, not arbitrarily:

1. Started from a Gemini-generated "diskette with a label" SVG mockup
   where the user wanted the "SAVE STATE STUDIO" text properly centered
   on the label (it originally overflowed the label's edges).
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
   floppy-disk illustration the user shared for reference). **Rejected**:
   lines too thick, 3D effect far too strong ("sollte vielleicht ein
   Viertel so stark sein").
5. Tried a monochrome "technical drawing / blueprint" treatment instead
   of shaded 3D: pure line art, 45°-hatch pattern fills on cut/exposed
   surfaces instead of gradients, plus an ISO-style dimension line and
   centerline. This was a legitimate, well-received direction on its own
   terms, but the user then pivoted away from a detailed/realistic
   diskette illustration entirely in favor of approach 6.
6. **Final pivot**: drop the detailed diskette illustration altogether,
   go with a two-line wordmark + a simple 8-bit pixel-art floppy icon
   instead, explicitly for more "Gaming-Flair". This is the shipped
   version.
7. User supplied two Vecteezy stock "floppy disk" images (free-license
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
   future studio project, take general style/composition inspiration
   only — never trace or directly derive artwork from the copyrighted
   file itself.**
8. Two bugs found via direct visual feedback on the final pixel design
   and fixed (both documented in the icon table above): the corner rivet
   notches overlapping the label's edge, and the gold stripe bleeding
   over the label's border stroke.

## Licensing / legal status

- Logo artwork is original — not traced or derived from any stock asset.
- Manrope is SIL Open Font License — fine for commercial/logo use, no
  attribution required.
- **No trademark search or registration has been done** for the "Save
  State Studio" name or logo. Flagged to the user as an optional future
  step (e.g. the Swiss IGE trademark register, or a lawyer if the studio
  grows beyond casual indie release) — not something either of us has
  done, don't imply otherwise if asked later.

## Other studio ideas mentioned in passing

Noted here only as background context, not a spec or commitment: the
user mentioned a second possible future app idea under this studio — a
game backlog/wishlist tracker (motivated by Steam wishlists becoming
unmanageable), integrating with HowLongToBeat data to estimate
completion percentage and suggest what to finish first. Nothing has been
designed or built for this yet.
