# Material Calculators

Dependency-free browser tools for common materials-engineering calculations. Each calculator is a standalone HTML file: download it or open it locally in any modern browser—no installation, account, network connection, or data upload required.

## Tools

- **[Stress Tensor Transformation Calculator](StressTensorCalculator.html)** — transforms a 3×3 stress tensor between coordinate systems using user-supplied Euler angles; includes invariants, principal stresses, Mohr-circle data, and CSV export.
- **[XRD Crystal Structure Solver](XRD_Calculator.html)** — estimates the cubic lattice constant from ordered 2θ peaks for FCC, BCC, and simple-cubic structures using Bragg’s law.

## Live demo

When GitHub Pages is enabled, open the repository site and choose a calculator from the landing page.

## Run locally

Clone or download this repository, then open `index.html` or either calculator HTML file directly in a modern browser. The tools have no external dependencies and do not transmit inputs.

## Scope and limitations

These are educational and engineering-support tools. Verify inputs, assumptions, units, crystal structure, and results independently before using results for design, safety, publication, or commercial decisions.

The XRD solver assumes correctly ordered peaks and the selected cubic structure. The stress-tensor calculator relies on the angle convention presented in its interface.

## Development

The project deliberately avoids build tooling and third-party dependencies. Formula and numerical-behaviour changes require an independent reference-case check before merge.

## License

MIT — see [LICENSE](LICENSE).
