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

## First-consumer evidence (2026-07-11 — gainGround React rewrite, gainground#3)

The gainGround app was rebuilt on core + this theme (gainground issue #2 /
PR #3), making it the theme's first production consumer. Per-flag evidence
for Kyle's live lookbook pass — these are observations, not value changes:

1. **`--commit` is now in active use.** The rewrite maps every definitive
   data-changing act to Button `variant="commit"`: save annotation, add
   axis/milestone, send invite, request import job, and the sign-in
   activator. The deepened pine renders correctly, but the distance from
   `--accent` is subtle (L 0.52 → 0.42, same hue/chroma family) — judge in
   the lookbook whether commit reads as "more definitive" or just "darker".
2. **Scope colors: still no app evidence.** The app gates by role
   (manager/modeler/super_admin) but has no scope-colored chrome yet (core's
   `AuthStatus` not adopted; the rail uses plain text + buttons). Unblocked
   whenever wanted, but nothing new to judge against.
3. **`--surface-2` is now highly visible**: core's TextInput / SearchInput /
   Select render surface-2 fills, so every form in the app shows it against
   `--surface` panels on the `--bg` paper. The three-step paper ramp is
   worth a deliberate look in the lookbook forms section. `--text-faint` and
   `--border-strong` remain unconsumed by app code.
4. **Categorical slots staying neutral: CONFIRMED.** The rewrite introduced
   zero `--cat-*` usage — score ramps only, as designed.
5. **Dark surface direction: kept and verified.** The rewrite drives dark
   mode through the ported theme store (`data-theme` on the root); rendered
   values match the pre-rewrite app exactly.
6. **Sunlight mode: still app-level.** The field app doesn't exist yet;
   nothing forces the decision.
7. **Voice doc: DRAFTED** — `docs/voice.md` in this PR, distilled from
   gainGround's BRAND-BRIEF/PRODUCT/DESIGN by the app-context agent.
   Kyle reviews wording like any brand value.
8. **System stack confirmed in production** — the rewrite ships zero
   webfonts; `--font-editorial` still unused.

**New, for the next core session (not a theme concern):** core's Button has
no danger variant, so the app composed an app-side `DangerButton` (neutral
variant tinted with `--status-danger` via style) for destructive acts
(remove axis, revoke invite, discard, compact history). If a second app
grows the same pattern, that's a graduation candidate against core's Button.
