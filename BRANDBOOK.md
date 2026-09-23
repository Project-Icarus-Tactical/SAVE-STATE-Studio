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

| Token | Hex | Role |
|---|---|---|
| `--bg` | `#1C1C1E` | Primary background. Same value as the Apex Lifter app's own background — deliberate, ties studio and first product together. |
| `--gold` | `#E2C766` | Primary accent. Same gold as Apex Lifter. Used for primary buttons, the "STUDIO" wordmark, the logo's label stripe, "Live" status badges. |
| `--violet` | `#D6BBF7` | Secondary accent. Same violet as Apex Lifter. Used for secondary icon fills, "In Konzeption"/concept-stage badges, section eyebrows. |
| `--red` | `#E2554C` | Tertiary accent, **studio-only**. Apex Lifter's own brand explicitly avoids red everywhere (see that repo's CLAUDE.md); Save State Studio is a distinct brand and deliberately uses a warm red as its third signature color, always in the tri-color accent bar and sparingly elsewhere. Provisional exact hex — revisit if it fights the gold/violet pairing in practice. |
| `--text` | `#ECECEC` | Primary text on dark backgrounds. |
| `--text-muted` | `#9a949e` | Secondary/muted text. |
| `--cream` | `#ece6d8` | The floppy disk icon's label color — not a general-purpose UI color, only used in/near the logo itself. |

**The tri-color accent bar** (`.accent-bar` in `index.html`) is the
studio's signature motif: a single bar, hard-split into three equal
gold/violet/red segments (not a smooth gradient — same "hard split,
not blended" convention Apex Lifter uses for its own gold→violet
lockup). Reuse this exact pattern for any future divider/underline
that needs to read as "Save State Studio", the same way Apex Lifter
reuses its own two-color split gradient everywhere.

**Red stays an accent, never a surface.** Use it for a small mark, an
icon fill, or one segment of the tri-color bar — never a background,
never body text, never more than one element per screen. It's meant to
read as "this studio is a little different/edgier than the polished
product brand", not as an alarm/error color.

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
- Never recolor the icon itself (the gold label stripe is a deliberate
  brand substitution for the generic red stripe real floppy-disk icons
  usually have — see `CLAUDE.md` History item 7). The studio's red
  accent lives elsewhere on the page, not on the icon.

## Where this is used

- `index.html` — the studio's own landing page (this repo).
- The [apexlifter-social](https://github.com/Project-Icarus-Tactical/apexlifter-social)
  and [SAVE-STATE-social](https://github.com/Project-Icarus-Tactical/SAVE-STATE-social)
  kits reference this same identity, though the SAVE-STATE-social kit
  was built before the violet/red decision above and currently uses
  only gold + gray — revisit that kit's images if the two should be
  brought fully in line with this brandbook.
