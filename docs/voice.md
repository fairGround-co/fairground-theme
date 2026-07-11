# fairGround — voice & content rules (theme-level)

*Org voice lives in per-org theme docs (design-system DECISIONS #19); generic
content discipline (tabular numerals, icon-with-label rule) lives in core
docs. Distilled from gainGround's BRAND-BRIEF.md / PRODUCT.md / DESIGN.md by
the app-context agent (fairground-theme#2); Kyle reviews.*

Three words: **instrument, candor, ground game.** The voice splits by room —
the back office, the doors, and the public page — and the split matters more
than any single rule.

## Back office / manager voice (desktop tools)

Terse, dense, operationally credible. The reader is a skeptical operator who
has seen tools overpromise, working data late at night. Talks in campaign
vernacular (precincts, walk lists, universes, contact rates) without
jargon-as-drama.

- **Epistemic honesty is the register.** The model infers and predicts — the
  UI never dresses inference as fact. Scores show confidence; provisional
  data *looks* provisional (dashed border + label, never color alone);
  backtests and caveats are one click away.
- **Every number cites its source.** "Source: pipeline · as of 2026-07-03."
  A number with no provenance reads as marketing.
- **Empty states are one sentence of candor plus the next action.** "No
  score run yet. Benchmarks feed it: 5 labeled of 7." Never an illustration,
  never an apology, never "Oops!".
- Buttons are verbs (*Save annotation, Request job, Run score refresh*);
  destructive options say what is destroyed (*Delete stale versions*).
- Contracts are stated plainly at the moment of commitment: "Old labels are
  kept and marked stale — never deleted."

## Field / canvasser voice (mobile app)

Bold, simple, energizing — one-handed, in sunlight, often a first-time
volunteer being the literal face of the campaign. Short imperatives, one
primary action per screen, never a forced guess. **The tenant wears the
brand here**: campaign energy comes from the *tenant's* theme and copy;
gainGround's own voice stays the quiet instrument underneath.

## Marketing / public voice

Confident, direct, no civic-virtue performance. This is a tool for winning,
and the copy is straight about it: *"Gain ground before election day."* /
*"Field intelligence for local campaigns."* Speaks to campaign managers as
peers; never preachy, never pastel-democracy-celebration, never partisan.

## Casing, tone, symbols

- Wordmarks are **camelCase, always**: fairGround, gainGround — including at
  sentence start. The internal capital is the brand.
- Headers/eyebrows UPPERCASE with wide tracking (`--ls-label` /
  `--ls-eyebrow`); body and data sentence case; status chips lowercase
  ("labeled v3", "re-review").
- Digits are tabular everywhere they align. Coded identifiers (cids, eids)
  render in mono as debugging notes, never as the label.
- No emoji as decoration; no illustrations, anywhere. The one glyph budget
  goes to functional status icons paired with labels.
- First person essentially never; the tool addresses the operator in
  imperative or reports state in plain declaratives.

## Color semantics carried by this theme

- **Pine** (`--accent`, deepened for `--commit`) is the *acting* color —
  primary actions, links, focus, definitive data-changing acts. One brand
  hue, held in reserve.
- **Amber** (`--accent-2`, `--status-caution`, `--scope-guest`) flags the
  provisional: pending, needs-confirmation, review queues. Amber is never an
  error.
- **Saturation is spent on data**, not chrome: score ramps, statuses, map
  fills. If everything is colorful, nothing is.
- Score ramps are **fixed across tenants** (pine sequential; pine↔clay
  diverging for support↔oppose) so trained eyes transfer between campaigns.
- **Never partisan-coded**: the default theme reads neither red-team nor
  blue-team; support↔oppose is pine↔clay by design.
- Status hues are colorblind-safe and always paired with an icon or label —
  color alone never carries state.
