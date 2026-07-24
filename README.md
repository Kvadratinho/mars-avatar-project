# Mars Avatar Project

### Control Without Presence

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21268416.svg)](https://doi.org/10.5281/zenodo.21268416)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

<!-- After publishing v3.5 on Zenodo, replace the DOI above with the new
     version DOI, or with the concept DOI ("Cite all versions") so the badge
     always resolves to the latest edition. -->

A concept white paper on exploring Mars through a coordinated fleet of robotic
avatars, commanded from Earth at the level of goals rather than movements.

---

## The problem

The one-way signal delay between Earth and Mars is 4–22 minutes and cannot be
engineered away. Continuous teleoperation is therefore impossible, and the
architecture of any remote presence system has to treat latency as a design
condition rather than a defect. The operator transmits goals; onboard autonomy
determines how to achieve them.

## What is claimed

Almost every component of this architecture already exists in isolation:
goal-based commanding on NASA rovers (AutoNav, AEGIS), supervisory telepresence
from orbit (ESA METERON, Analog-1), immersive avatar interfaces (ANA Avatar
XPRIZE). The paper says so explicitly, in Chapter 3, and treats that prior work
as the baseline.

The narrow claim is this: **what has not been built is the layer that
coordinates a heterogeneous fleet under full interplanetary latency.** A single
rover is autonomous today. Five specialized platforms sharing one world model,
reallocating subtasks after a loss, and staying coherent when the local network
fragments, are not. That layer — Mission AI — is the subject of Chapter 6:
a five-layer reference architecture, a goal-package protocol, graduated decision
classes (A/B/C), a degradation hierarchy, and measurable quality metrics.

## What is not claimed

- **That AI solves unforeseen failure.** Onboard systems handle contingencies
  enumerated at design time, and present-day AI does not meaningfully extend
  that set — particularly under the memory and compute budgets of planetary
  robots. Section 5.13 states this and advances only the weaker claim the
  architecture can defend: a fleet does not solve unmodelled failure, it lowers
  the cost of not having solved it. Redundancy does not answer correlated or
  common-mode failure at all.
- **That this replaces crewed missions.** The intended relationship is
  sequential: robots prepare the environment, humans arrive into it.
- **That the cost model is a budget.** Chapter 11 gives order-of-magnitude
  figures with stated assumptions, and Section 11.9 lists four conditions under
  which they fail.
- **That neural interfaces matter here.** They are explicitly off the critical
  path (Section 9.3). Input bandwidth is not the binding constraint when a
  decision takes minutes to reach Mars.

## Concept

```
Human Operator          goals, constraints, Class A approvals
        │
        ▼
   Mission AI           interpretation, fleet planning, shared world model,
        │               execution monitoring, safety gate
        ▼
Robotic Fleet           rover · construction · cargo · drone · lab · maintenance
        │
        ▼
Scientific Results
```

## Open problems

These are the parts that are genuinely unsolved, and they define the critical
path more than the hardware does:

- detecting the unmodelled case — telling "handled poorly" from "outside the
  system's competence" (Section 6.7)
- common-mode failure in a fleet of similar platforms
- verification of learned components; sim-to-real transfer for Martian conditions
- coordination when the local network fragments for extended periods
- long-term drift of the shared world model
- energy for construction-class platforms: an MMRTG supplies ~110 W, while
  manipulator work needs kilowatts (Section 11.6)

## Contents

| File | Description |
|---|---|
| `Mars_Avatar_White_Paper_v3.5.pdf` | Concept white paper, current edition |
| `Mars_Avatar_White_Paper_v3.5.docx` | Same, editable |
| `Mars_Avatar_Presentation_EN.pptx` | Presentation deck |
| `CHANGELOG.md` | Version history |
| `LICENSE` | CC BY 4.0 |

## Roadmap

| Stage | Scope |
|---|---|
| I | Terrestrial prototype under simulated delay, including failure injection |
| II | Lunar demonstration — multi-robot coordination at seconds of latency |
| III | First robotic missions on Mars |
| IV | Robotic infrastructure |
| V | Support for crewed expeditions |

Transitions occur only against the measurable criteria of Sections 10.9 and 6.6.

## Status

Conceptual research. No prototype, no simulation results, no experimental data
— the document is an architecture proposal, not a report of work performed. The
intended next step is the smallest useful experiment: a simulated fleet under
auction-based task allocation, with anomalies injected from outside the
documented fault model, measured against the metrics of Section 6.6.

Critique is more useful here than agreement. Open an issue, or write directly.

## Citation

> Khalanhot, O. (2026). *Mars Avatar Project — Control Without Presence.*
> Concept White Paper, version 3.5. Zenodo.
> https://doi.org/10.5281/zenodo.21268416

## License

[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)
(CC BY 4.0). You may share and adapt this material for any purpose, including
commercially, provided you give appropriate credit. No permission or fee is
required.

## Author

**Oleksandr Khalanhot** — independent researcher, Zürich, Switzerland
[mars-avatar.com](https://mars-avatar.com/)
