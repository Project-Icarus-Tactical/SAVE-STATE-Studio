# Late Byte — Brandbook

The authoritative reference for how Late Byte looks and sounds. For the
logo's exact construction (shape coordinates, color table, why it looks
the way it does), see `CLAUDE.md` — this file is the higher-level brand
summary: colors, type, voice, and usage rules for anything beyond the
logo itself (the website, social posts, future assets).

## Name & story

**Renamed from "Save State Studio" to "Late Byte" (2026-09-23)** — same
founder, same studio, same first product (Apex Lifter), new name. "Save
State" (the gaming save-point term) was retired in favor of "Late Byte":
shorter, cleaner as a wordmark, and the domain (`latebyte.ch`) was free
where the old one required buying `savestate.ch` fresh anyway. The
underlying story is unchanged and is actually what "Late Byte" now names
directly: a full-time-employed father of two who codes late in the
evening, once the kids are asleep — "Byte" for the code, "Late" for when
it actually gets written. If "Save State" or the floppy-disk icon shows
up anywhere old (social kit repos, cached pages), that's the pre-rename
identity — see `CLAUDE.md`'s History section for the full logo lineage
across both names.

**Naming due diligence before landing on this name**: several other
candidates were checked via web search and domain lookups (RDAP against
`nic.ch`/Verisign, not a full legal trademark search) before picking
this one — "Lullaby Logic" and "Lullaby Byte"/"LullaByte" were both
rejected after finding an active, trading LLC and a live Google Play app
respectively using those almost-exact names. "Late Byte" cleared that
same check with only a loose, different-category collision (a tech blog
called "The Latebyte"). Given the founder's own stated plan (no scaling
beyond maybe future merch, in the founder's words), that residual risk
was judged acceptable. Still not a substitute for an actual trademark
register check (e.g. Swissreg) if this ever gets registered as a real
business entity or scales beyond a hobby project.

## Colors

**Gold + red only — no violet in the studio's own chrome.** Explicit,
deliberate call: violet + gold is Apex Lifter's own brand. Late Byte
needs a clean, immediately recognizable difference from the app it
ships, not a shared palette — so violet never appears in the studio's
own nav, buttons, section labels, or accent bar. An earlier draft of
this file used gold + violet + red for the studio itself; that was a
misread of the instruction and has been corrected. This rule survived
the name change unchanged.

**One narrow, deliberate exception**: where the site shows a *specific
other product's own logo/icon* (currently: the Apex Lifter mark on the
"Projekte" card), that mark keeps the depicted product's own real
colors — Apex Lifter's icon stays gold+violet there, because it's
showing that product's actual identity, not the studio's. This is not
a loophole for violet in general: any studio-level element (nav,
buttons, badges, section labels, dividers) stays gold+red, always. If
violet shows up anywhere on this site *other than* a specific product's
own logo mark, that's a bug.

| Token | Hex | Role |
|---|---|---|
| `--bg` | `#1C1C1E` | Primary background. Same value as the Apex Lifter app's own background — deliberate, ties studio and first product together. |
| `--gold` | `#E2C766` | Primary accent. Same gold as Apex Lifter (the one color deliberately shared). Used for primary buttons, the "BYTE"/"STUDIO" wordmark, most of the chip icon's frame/pins/bits, "Live" status badges. |
| `--red` | `#E2554C` | Secondary accent, **studio-only**. Apex Lifter's own brand explicitly avoids red everywhere (see that repo's CLAUDE.md); Late Byte deliberately uses it as its own second color instead of reusing Apex Lifter's violet. Also the "LATE" half of the wordmark (`#E2554C` — "late" reads as the more urgent/accented word) and the one red bit inside the chip icon. |
| `--text` | `#ECECEC` | Primary text on dark backgrounds. **No longer used anywhere in the logo/wordmark itself** — the wordmark used to have a white "LATE", but that was dropped once the founder pointed out nothing else in the mark was white (see Colors note below and `CLAUDE.md`'s chip/byte icon section). Still fine for ordinary body copy. |
| `--text-muted` | `#9a949e` | Secondary/muted text. Also used for neutral, non-branded states (e.g. an "in progress" badge) that shouldn't claim either accent color. |
| `--cream` | `#ece6d8` | Historical only — was the retired night-scene logo's bed/blanket color. Not used by the current chip/byte mark or the intermediate crescent-moon mark; kept defined in `index.html` only until confirmed nothing else references it. |

**The accent bar** (`.accent-bar` in `index.html`) is the studio's
signature motif: a single bar, hard-split 50/50 into gold and red (not
a smooth gradient — same "hard split, not blended" convention Apex
Lifter uses for its own gold→violet lockup, just with the studio's own
two colors). Reuse this exact pattern for any future divider/underline
that needs to read as "Late Byte".

**Red stays an accent, never a surface.** Use it for a small mark, an
icon fill, one half of the accent bar, or the "BYTE" half of the
wordmark — never a background, never body text, never more than one or
two elements per screen. It's meant to read as "this studio is a little
different/edgier than the polished product brand", not as an alarm/
error color.

**The current chip/byte icon is gold + one red bit** — a rounded chip
outline with pin legs, solder pads and a pin-1 dot all in faint gold,
containing 8 small squares (a literal byte: 8 bits) mostly gold with
**exactly one red bit**, always at the same grid position. That single
red square is the icon's only color break — the same "small, deliberate
accent, never a surface" rule as everywhere else in this brandbook.
**The wordmark's own color split changed alongside this icon**: "LATE"
is red, "BYTE" and "STUDIO" are gold — tying "late" to the accent color
and "byte" to the primary one. White was dropped from the wordmark
entirely once the founder pointed out the inconsistency of a white word
next to an icon with no white in it; if either the icon or the wordmark
ever reintroduces white, do it in both places at once, not just one. A
version with the chip's frame/pins/solder-pads *also* in white (keeping
the bits gold+red) was designed and shown but explicitly not picked —
see `CLAUDE.md`'s "Icon: chip/byte mark" section for that comparison and
the exact construction/coordinates.

## Typography

**Manrope** (Google Fonts, SIL Open Font License) — same family as the
Apex Lifter app, keeping studio and first product visually related
without being identical. This is explicitly **provisional**: the
founder flagged that the typeface choice may still change once the
studio identity is fleshed out further. If it changes, update this
file, `index.html`'s font import, and the logo SVGs together — don't
let them drift out of sync.

- Headings: weight 800, tight-ish letter-spacing.
- The "STUDIO" half of any lockup is always the lighter of the two
  wordmark weights (currently 600, vs. 700 for "LATE BYTE" above it)
  with wide letter-spacing (~4), gold — this specific treatment is part
  of the logo itself, not just a heading style (see `CLAUDE.md`).
  Weights were reduced across the board from an earlier 800/700 pass per
  direct feedback that it read too bold.
- Body copy: weight 500-600, 15-16px, generous line-height (1.6-1.75)
  — this is a personal, story-driven site, not a dense product page.

## Voice & tone

- **First person, always.** This is one person's studio, not an
  anonymous company — "ich", not "wir" or "das Team".
  it's important this reads honest, not corporate.
- **No-bullshit directness.** Say the actual thing: "fairer Preis" not
  "wertorientierte Preisgestaltung", "keine Ads" not "werbefrei nach
  einem nutzerzentrierten Modell". If a sentence would fit in a VC
  pitch deck, rewrite it.
- **The Feierabend/family framing is a feature, not an apology.** Lead
  with "Vollzeit-Job tagsüber, Code nach Feierabend" rather than
  burying it — it's the actual reason this studio's products are
  built the way they are (fair price, no growth pressure, no
  compromises for outside investors), and it's now literally what the
  studio's name refers to.
- **Dogfooding over marketing claims.** Prefer "ich nutze sie selbst
  jeden Tag" over feature-list bullet points wherever both are
  possible — proof of use is the studio's actual credibility, not
  polish.
- A little dry humor is fine (e.g. the Friends/Buzz-feature "insider"
  post asking Apex Lifter users to add the founder as a friend and buzz
  him to the gym) — never at the expense of clarity about price, ads,
  or data.

## Logo usage

Full construction rules live in `CLAUDE.md` (shape coordinates, exact
colors, the full history of the retired floppy-disk mark, the retired
night-scene mark, the retired minimalist crescent moon, and the current
chip/byte mark). Quick rules for anyone just placing the logo, not
redrawing it:

- Always on the studio's dark background (`#1C1C1E`) or the slightly
  lighter card color (`#141416`) — never on a light background without
  redesigning the icon's faint-gold linework (currently tuned for a dark
  background) first.
- Use `assets/logo/logo-full.svg` for hero/standalone placements (icon
  on top, wordmark below), `assets/logo/logo-footer.svg` for compact
  inline placements (nav bars, footers — icon left, wordmark right),
  `assets/logo/icon-only.svg` for favicons/app icons where no wordmark
  fits.
- The icon is a chip/processor outline containing 8 small bits (one
  red) — a literal "byte". No moon, no bed, no parent, no laptop, no
  fused second symbol. See `CLAUDE.md` if asked to bring an earlier mark
  back or to understand why it changed three times.

## Where this is used

- `index.html` — the studio's own landing page (this repo).
- The [apexlifter-social](https://github.com/Project-Icarus-Tactical/apexlifter-social)
  kit is Apex Lifter's own (gold + violet), unaffected by any of this.
- The [SAVE-STATE-social](https://github.com/Project-Icarus-Tactical/SAVE-STATE-social)
  kit still carries the **old** name and floppy-disk logo as of this
  writing — it was not renamed alongside this repo (not asked for, and
  would need its images regenerated from scratch). Flag this to the
  founder before publishing anything from that kit; either rename it to
  match or treat it as retired/superseded.
- `apexlifter-web`'s own footer ("Made by Late Byte") pulls the compact
  icon inline — see that repo's own `i18n-strings.php`/CLAUDE.md for the
  `footer.madeBy` string in all four languages.
- The `APEX-LIFTER` Android app now carries a subtle "Made by Late Byte"
  credit too — a small non-nav row at the bottom of the drawer (past the
  crash-logs item), tapping through to latebyte.ch. Uses its own
  hand-converted `ic_late_byte_logo.xml` VectorDrawable of the current
  chip/byte icon (flat colors, no gradient/glow — VectorDrawable doesn't
  need it at this size) — see that repo's own `TrainingsTrackerApp.kt`
  and CLAUDE.md for the construction. Keep this in sync manually if the
  studio icon changes again, same as every other place it's duplicated.
