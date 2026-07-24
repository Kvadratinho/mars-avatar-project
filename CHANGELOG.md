# Changelog

All notable changes to the Mars Avatar Project concept white paper.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [3.5] — 2026-07-22

Revision pass following external technical review. Two things changed in
substance: unforeseen failure is now treated as a first-class limitation of the
concept rather than a passing remark, and the economic model was rebuilt on
stated assumptions. Neural interfaces were removed from the critical path, and
the document is no longer anonymous.

### Added

- **§5.13 "Unforeseen Failures and the Compute Constraint"** — the principal
  addition, and a direct response to the review. States that contemporary AI
  does not remove the boundary of the modelled fault space; that confidence
  estimates degrade precisely on out-of-distribution inputs; and that flight
  computing remains one to two orders of magnitude behind terrestrial hardware.
  Advances the narrower claim the architecture can defend — a fleet does not
  solve unmodelled failure, it lowers the cost of not having solved it — and
  states the limits of that claim: redundancy does not answer correlated or
  common-mode failure.
- **§11.9 "What Would Invalidate These Estimates"** — four stated conditions
  under which the cost model of Chapter 11 fails, with the consequence of each.
- **§11.1 comparability caveat** — explicit statement that a crewed expedition
  and a robotic fleet do not deliver the same product, and that the figures
  compare the cost of establishing surface presence, not equivalent scientific
  output.
- **Surface power segment** in the Stage III cost model ($2–4B, two
  Kilopower-class units with qualification and deployment) — omitted entirely
  in v3.4.
- **§6.5** — new first level in the degradation hierarchy: unmodelled anomaly on
  a platform, including fleet-wide suspension of a procedure suspected to be
  systematic. Subsequent levels renumbered.
- **§6.6** — two metrics: *Unmodelled Anomaly Rate* (target is honest
  measurement, not decline; a reported zero indicates an incomplete taxonomy)
  and *Anomaly Recovery Cost*.
- **§6.7** — two open research problems: detection of the unmodelled case, and
  common-mode failure in homogeneous fleets.
- **§10.9** — Stage I now requires a failure-injection campaign run by a team
  independent of the developers, drawn from outside the documented fault model.
- **§10.8** — technology readiness row for onboard computing for autonomy.
- **§11.8** — comparison row: response to an unmodelled situation.
- **Executive summary** — "The principal open problem" paragraph.
- **Appendix B. Note on Neural Interfaces** — the BCI survey formerly in
  Chapter 9, condensed, with an explicit statement that the architecture does
  not depend on it.
- **References [31] and [32]** — NASA/JPL High Performance Spaceflight
  Computing (in JPL testing since February 2026, reported at ~500× current
  radiation-hardened flight processors; not yet flight-qualified).
- Title page carries author, affiliation, site, and date; the same details were
  written into the document metadata, previously "Un-named".

### Changed

- **Stage III fleet estimate: ≈ $14–23B → ≈ $18–31B.** The v3.4 figure omitted
  surface power and priced platforms with no flown analogue as though they were
  science rovers. Development of five platform types raised from $8–12B to
  $10–16B; launches from $0.5–1.5B to $0.7–2B (6–8 heavy LVs).
- **Cost comparison claim softened** from "5–10 times cheaper than the lower
  estimate of a crewed program" to "roughly three to six times below the lower
  bound of published crewed estimates," with the reason stated in the text.
- **§5.12** — limitations of AI expanded from five items to seven, adding
  inability to act outside the modelled fault space, unreliable self-assessment
  of confidence, and onboard memory and compute budgets. Framed as permanent
  design conditions rather than problems awaiting a solution.
- **§12.2 "Artificial-Intelligence Failure"** — rewritten to distinguish
  unmodelled situations from ordinary AI error, and to state that no part of the
  architectural response removes the boundary itself.
- **§9.3** rewritten as "A Note on Neural Interfaces": BCIs declared off the
  critical path, on the argument that input bandwidth is not the binding
  constraint when a decision takes minutes to reach Mars. Excluded from the
  Chapter 6 critical path and the Chapter 10 transition criteria.
- **§9.2** — "Stage 3 — Brain–Computer Interface (BCI)" renamed to
  "Stage 3 — Additional Input Channels".
- **§9.9** roadmap table — the 10–20 year row no longer promises
  high-performance BCIs.
- **§4.2** — "seven interconnected layers" corrected to six, matching the six
  layers actually enumerated in §4.3–4.8.
- **§5.14** — former §5.13 (chapter conclusions) renumbered.
- Executive summary and §11.8 updated to the revised figures.
- Front matter rebuilt: title page on its own page, table of contents with page
  numbers on page 2, page numbering in the footer.

### Removed

- Non-invasive / invasive BCI subsections from the body of Chapter 9
  (relocated to Appendix B, condensed).

---

## [3.4] — earlier

Baseline for this changelog. Full edition with Chapters 1–13 and Appendix A.
