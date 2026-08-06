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
