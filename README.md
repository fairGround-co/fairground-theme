# fairground-theme

**→ [Open the lookbook](https://fairground-co.github.io/fairground-theme/)** —
this theme rendered live: every contract token with its resolved fairGround
value, all core primitives, light/dark, a neutral ⇄ fairground switcher, and
density. Source: [docs/lookbook.html](docs/lookbook.html).

> **0.1.x is a draft-quality seed** extracted from gainGround's design spec so
> app work can start; the value refinement pass is issue #2 (flags in
> [docs/refinement-notes.md](docs/refinement-notes.md)).
>
> **First production consumer (2026-07-11):** the gainGround app
> ([fairground-co/gainground](https://github.com/fairground-co/gainground)
> `app/`, React rewrite PR #3) ships on this theme. First-consumer evidence
> per flagged value is recorded in refinement-notes; org voice is drafted in
> [docs/voice.md](docs/voice.md).

Brand **token values only** for this org — all palettes/variants, consumed with
`@fairground-co/core`'s token contract. Invariant: no components, no widget code,
no licensed assets (those live in the private `<org>-brand-assets` repo). Always
safe to publish.

Published as `@fairground-co/fairground-theme` (GitHub Packages). See
`fairground-co/design-system` DECISIONS.md #10.

## Usage

```js
import '@fairground-co/core/styles.css';          // contract + neutral reference
import '@fairground-co/fairground-theme/styles.css'; // brand values (AFTER core)
```

```html
<html data-brand="fairground" data-theme="light">
```

The brand is a "paper instrument": pine primary + amber companion on warm
paper, borders over shadows (card shadow deliberately zeroed), system-stack
type — no webfonts to arrange. Categorical slots intentionally stay on the
neutral reference (gainGround uses fixed score ramps, which derive from
`--accent` and the diverging anchors automatically). Multi-tenant campaign
overrides ride the core tenant whitelist on a `[data-tenant]` scope.

## Regenerating the lookbook

```bash
node <design-system>/packages/core/scripts/build-lookbook.mjs \
  --brand fairground --title "fairGround" \
  --package "@fairground-co/fairground-theme@<version>" \
  --theme-css ./styles.css \
  --out ./docs/lookbook.html \
  --note "0.1.x values are a draft-quality seed; refinement is issue #2."
```
