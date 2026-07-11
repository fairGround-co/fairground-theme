# Refinement notes — fairground-theme 0.1.x draft values (issue #2)

*The 0.1.0 seed was extracted from gainGround's design spec and token file and
mapped onto core token contract v0. Everything below needs a decision pass —
per Kyle, worked in this repo with an agent that has the gainGround app
context, one value at a time, against `docs/lookbook.html`.*

## Flagged decisions

1. **`--commit` is proposed.** gainGround has no commit-emphasis hue; the seed
   deepens the pine family. Confirm, or pick a distinct definitive-act color.
2. **Scope colors are proposed.** No capability-color pattern exists in the app
   yet. Seed maps: view = the info blue, guest = amber (fits its
   "provisional/pending" semantics), edit = the commit pine.
3. **Interpolated values:** `--surface-2/3`, `--text-faint`,
   `--border-strong`, several dark-mode steps, and the dark status lifts.
4. **Categorical slots deliberately stay neutral.** gainGround uses fixed score
   ramps, not discrete series — the pine sequential and pine↔clay diverging
   ramps derive automatically from `--accent` + the div anchors. Confirm that
   leaving `--cat-*` on the reference palette is the right call (they'd only
   surface if a fairGround app starts using categorical identities).
5. **Dark surface direction.** gainGround's own dark mode lifts cards LIGHTER
   than the ground — opposite of the base system's pop-to-black field pattern.
   The seed keeps gainGround's shipped direction; confirm.
6. **"Sunlight mode"** exists in the design spec (whiter ground, thicker
   hairlines, larger text) but not in code — decide whether it becomes this
   theme's dark-mode-analog for field work or an app-level concern.
7. **No voice doc.** `nwae-theme/docs/voice.md` is the model.
8. **Type is authentically the system stack** — no webfonts to arrange; the
   `--font-editorial` serif is a placeholder (unused by the app).
