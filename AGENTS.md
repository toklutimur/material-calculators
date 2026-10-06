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

## Definition of Done (extends the global default)

- Gates: none automated. Open the file in a browser and check each formula
  change against a known reference case; report inputs and expected outputs.
- Proof: calculator opened in a browser; screenshot only if layout changed.
- Merge: squash, delete branch. No deploy, no live check.
- User-only steps (report, do not attempt): choosing new reference cases or
  changing an engineering formula's definition.

## Agent loop

- The reviewer recomputes the reference case independently (by hand or a
  throwaway script) rather than reading the worker's number.
- Single-file HTML, no dependencies: blocking if violated.

<!-- harness:shared v3 - source ~/.claude/templates/AGENTS-agent-loop.md; edit there -->

## Agent behaviour (shared)

- The main session orchestrates: it reads git, this file, state/plan files and agent
  reports; source, diffs, test output and data are read by subagents.
- Every dispatch names its model: Explore/haiku locate, worker/sonnet mechanical edit,
  worker/opus judgement or risk, reviewer/opus verdicts. Never fable as a subagent.
- Leave no artefacts: scratch output goes to the session scratchpad, not the repo root;
  delete or gitignore anything untracked you created before reporting DONE.
- Visual work (UI repos): the brief lists VISUAL ACCEPTANCE criteria and a
  "must not change" list; the reviewer compares before/after screenshots at
  the viewport or device this file's Definition of Done names, and the live URL
  or device after deploy. Two fixes on one subject = stop, re-scope.

<!-- /harness:shared -->
