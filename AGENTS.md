# Material Calculators — Project Instructions

## Scope

Standalone, dependency-free HTML/JS engineering calculators. Each file is a
single self-contained page — no build step, no shared code between them.

- `StressTensorCalculator.html` — stress tensor calculations.
- `XRD_Calculator.html` — X-ray diffraction calculations.

## Working Rules

- Keep each calculator a single self-contained HTML file unless a task
  explicitly asks to split it up or add a build step.
- Preserve existing formulas and numeric behavior exactly; these are
  engineering tools where a silent calculation change is worse than a
  visible bug.
- No external dependencies — do not introduce a framework or package.json
  for what is currently plain HTML/CSS/JS.

## Validation

- Open the file directly in a browser and check the calculation against a
  known reference case after any formula change.

## Definition of Done (extends the global default)

- Gates: none automated; each formula change is checked against a known
  reference case, with inputs and expected outputs written in the report.
- Visual/device proof: the calculator opened in a browser; screenshot only when
  layout changed.
- Merge: PR against `main`, `gh pr merge --squash --delete-branch`.
- Deploy: none.
- Live check: n/a.
- User-only steps (report, do not attempt): choosing new reference cases or
  changing an engineering formula's definition.

## Agent loop

- The reviewer recomputes the reference case independently (by hand or a
  throwaway script) rather than reading the worker's number.
- Single-file HTML, no dependencies: blocking if violated.
