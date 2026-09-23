# Save State Studio — Brandbook

The authoritative reference for how Save State Studio looks and sounds.
For the logo's exact construction (icon grid, color table, why it looks
the way it does), see `CLAUDE.md` — this file is the higher-level
brand summary: colors, type, voice, and usage rules for anything beyond
the logo itself (the website, social posts, future assets).

## Name & story

"Save State" is the gaming term for a save-point/snapshot — a
deliberate reference to the founder's own identity as, in his words,
"im Grunde ein absoluter Nerd, der für das Gaming liebt, lebt und
stirbt", alongside being a full-time-employed father of two who codes
in the evenings and on weekends. The name is a nod to that gaming
identity, not a generic "save"/productivity pun — keep that framing
whenever the name itself needs explaining in copy.

## Colors

**Gold + red only — no violet in the studio's own chrome.** Explicit,
deliberate call: violet + gold is Apex Lifter's own brand. Save State
Studio needs a clean, immediately recognizable difference from the app
it ships, not a shared palette — so violet never appears in the
studio's own nav, buttons, section labels, or accent bar. An earlier
draft of this file used gold + violet + red for the studio itself;
that was a misread of the instruction and has been corrected.

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
| `--gold` | `#E2C766` | Primary accent. Same gold as Apex Lifter (the one color deliberately shared — see the logo's History note on why the label stripe is gold, not the generic red). Used for primary buttons, the "STUDIO" wordmark, the logo's label stripe, "Live" status badges. |
| `--red` | `#E2554C` | Secondary accent, **studio-only**. Apex Lifter's own brand explicitly avoids red everywhere (see that repo's CLAUDE.md); Save State Studio deliberately uses it as its own second color instead of reusing Apex Lifter's violet. Provisional exact hex — revisit if it fights gold in practice. |
| `--text` | `#ECECEC` | Primary text on dark backgrounds. |
| `--text-muted` | `#9a949e` | Secondary/muted text. Also used for neutral, non-branded states (e.g. an "in progress" badge) that shouldn't claim either accent color. |
| `--cream` | `#ece6d8` | The floppy disk icon's label color — not a general-purpose UI color, only used in/near the logo itself. |

**The accent bar** (`.accent-bar` in `index.html`) is the studio's
signature motif: a single bar, hard-split 50/50 into gold and red (not
a smooth gradient — same "hard split, not blended" convention Apex
Lifter uses for its own gold→violet lockup, just with the studio's own
two colors). Reuse this exact pattern for any future divider/underline
that needs to read as "Save State Studio".

**Red stays an accent, never a surface.** Use it for a small mark, an
icon fill, one half of the accent bar, or a tiny logo detail — never a
background, never body text, never more than one or two elements per
screen. It's meant to read as "this studio is a little different/edgier
than the polished product brand", not as an alarm/error color.

**Red now appears in the logo itself, in one spot only**: the pixel
floppy disk's two corner rivet notches (previously dark gray) are red.
The gold label stripe is untouched — that substitution (gold instead of
the generic red stripe real floppy icons have) stays as-is; the rivets
were a separate, smaller opportunity to carry the studio's red into the
mark itself without undoing that original choice. Don't extend red to
any other part of the icon without checking first — see `CLAUDE.md`'s
logo History section for the full reasoning.

## Typography

**Manrope** (Google Fonts, SIL Open Font License) — same family as the
Apex Lifter app, keeping studio and first product visually related
without being identical. This is explicitly **provisional**: the
founder flagged that the typeface choice may still change once the
studio identity is fleshed out further. If it changes, update this
file, `index.html`'s font import, and the logo SVGs together — don't
let them drift out of sync.

- Headings: weight 800, tight-ish letter-spacing.
- The "STUDIO" half of any lockup is always weight 700 with wide
  letter-spacing (~4-6), gold — this specific treatment is part of the
  logo itself, not just a heading style (see `CLAUDE.md`).
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
  compromises for outside investors).
- **Dogfooding over marketing claims.** Prefer "ich nutze sie selbst
  jeden Tag" over feature-list bullet points wherever both are
  possible — proof of use is the studio's actual credibility, not
  polish.
- A little dry humor is fine (e.g. the Friends/Buzz-feature "insider"
  post asking Apex Lifter users to add the founder as a friend and buzz
  him to the gym) — never at the expense of clarity about price, ads,
  or data.

## Logo usage

Full construction rules live in `CLAUDE.md` (icon grid, exact colors,
why each design direction before the current one was rejected). Quick
rules for anyone just placing the logo, not redrawing it:

- Always on the studio's dark background (`#1C1C1E`) or the slightly
  lighter card color (`#141416`) — never on a light background without
  redesigning the wordmark's off-white color first.
- Use `assets/logo/logo-full.svg` for hero/standalone placements,
  `assets/logo/logo-footer.svg` for compact inline placements (nav
  bars, footers), `assets/logo/icon-only.svg` for favicons/app icons
  where no wordmark fits.
- Don't recolor the label stripe (stays gold — a deliberate brand
  substitution for the generic red stripe real floppy-disk icons
  usually have, see `CLAUDE.md` History item 7). The corner rivet
  notches are the one part of the icon that does carry the studio's
  red accent; don't extend red beyond that single detail without
  checking first.

## Where this is used

- `index.html` — the studio's own landing page (this repo).
- The [apexlifter-social](https://github.com/Project-Icarus-Tactical/apexlifter-social)
  kit is Apex Lifter's own (gold + violet), unaffected by any of this.
- The [SAVE-STATE-social](https://github.com/Project-Icarus-Tactical/SAVE-STATE-social)
  kit was built before the red accent color existed and currently uses
  only gold + gray — no violet, so it was never wrong, just incomplete
  next to this brandbook. Add the red accent there too if it's ever
  revisited, but nothing needs undoing.
