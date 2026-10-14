<!-- solve-problem:e914f0f2-660d-4e1d-99fe-455d210490cc -->
# Sustainable staffing and funding for independent cloud-algorithm evaluation

A [Tangle Solve problem](https://solve.tangle.tools/problems/e914f0f2-660d-4e1d-99fe-455d210490cc).

## What is the problem?

This is not a mathematical conjecture but an infrastructure/funding problem in experimental algorithms, and any attack must be framed accordingly. The precise statement: design, cost, and establish a **permanently funded, independently operated cloud-based algorithm evaluation track** — specifically for the SAT/solver-competition community, though the pattern generalizes — satisfying four hard requirements:

1. **Independence:** evaluation is run by an entity with no stake in the results (not a solver-developing lab, not a cloud vendor's own team);
2. **Public cost accounting:** itemized, reproducible budgets (compute hours, storage, staff time) published per iteration;
3. **Reproducible environments:** pinned container images, fixed instance sets and seeds, deterministic harness configuration, archived artifacts (logs, binaries, raw results) retained under a stated retention policy;
4. **Staffing sufficiency:** enough paid engineering/organizational effort for repeated annual (or more frequent) operation, not volunteer overflow.

The concrete motivating failure: the SAT Competition 2025 dropped its cloud track because the burden on the AWS-hosting organizers was too high. The target is a durable operating model, not a fix to any particular 2026 iteration.

A reasonable formalization if a mathematical/algorithmic framing is desired: characterize the minimal cost function C(n, m, t, r) for evaluating n solvers × m instances × t seeds × r resource profiles on cloud infrastructure under reproducibility constraints, and find the funding/staffing structure that makes C annually payable. But the census record's intent is operational.

## Why does it matter?

Cloud-scale solver claims (e.g., "our solver wins on AWS c7i instances at this memory bound") currently lack any independent verification venue once volunteer-run cloud tracks collapse. Reproducibility of experimental algorithm results depends on controlled environments that individual papers cannot credibly self-certify. Downstream, this affects which solvers industry and academia adopt, and whether cloud-track results can be cited as evidence at all. If it stays open, cloud benchmarking reverts to vendor- or author-run evaluations with no audit trail.

## What's already known?

- The SAT Competition has run cloud tracks in prior years on AWS credits, organized by volunteers (Codel/Fazekas/Heule/Iser et al., 2024 and earlier editions — verify exact prior cloud-track reports). This model is documented to be non-sustainable: SAT Competition 2025 explicitly skipped the cloud track due to organizer overload (slide 6 of the 2025 results slides).
- Known community knowledge (not a citation-backed result): AWS/donor credits cover compute but not the staffing bottleneck — environment freezes, solver onboarding, artifact archiving, and adjudication are the expensive parts.
- Related infrastructure precedents: StarExec (Texas, SAT/thematic competitions, grant-funded, eventually wound down — verify current status), the EDACC evaluation system, TACAS/ARCH community benchmarks, MLPerf (industry consortium with paid staff) as a governance model.
- No published analysis exists of the full cost structure of an independent cloud track including staff time; this is a gap, not a settled result.

## What would count as solving it?

Any of the following, in increasing strength:

1. **Cost model:** a documented, itemized accounting of what a cloud track actually costs (compute + storage + staff hours), derived from past SAT Competition cloud-track data or a pilot run.
2. **Design document:** a complete operational specification — governance (who is "independent"), environment pinning, artifact archival workflow, staffing plan with named roles and FTE estimates — reviewable by the competition community.
3. **Pilot:** one full evaluation cycle executed under the design, with published costs and archived artifacts, demonstrating the model works at real scale.
4. **Funded operation:** evidence of multi-year committed funding (grant, consortium, or institutional line item) and at least two consecutive successful iterations.

A referee (e.g., the SAT Competition steering committee or a funding agency panel) should accept items 3–4 as resolution; items 1–2 are necessary intermediate deliverables.

## How to start

1. Read the SAT Competition 2025 results slides (slide 6 and surrounding context) for the stated reason the cloud track was dropped; then find the 2023/2024 cloud-track descriptions for workload data (verify which years had cloud tracks).
2. Interview or email the past cloud-track organizers (Codel, Fazekas, Heule, Iser) to decompose where the effort actually went — likely environment setup and solver packaging, not compute.
3. Benchmark governance against StarExec's rise/fall and MLPerf's paid-consortium model to identify a funding structure that survives volunteer turnover.
4. Main obstacle: nobody pays for infrastructure maintenance; the attack is a proposal (NSF CCRI/DIBBS-style, or industry consortium), which requires the cost model of step 1 first.

## Key references

- Codel, C., Fazekas, K., Heule, M., Iser, M. (2025), *The Results of SAT Competition 2025* (results slides), slide 6 — documents the cancellation/skip of the 2025 cloud track due to AWS-organizer burden. Link: check the SAT Competition 2025 website / satcompetition.org (verify).
- SAT Competition annual reports (2022–2024) — describe prior cloud/parallel-track evaluation procedures; primary source for reconstructing actual operational workload. (verify which years included cloud tracks)
- StarExec project publications/reports (Stump et al., ca. 2013) — the main precedent for grant-funded shared solver-evaluation infrastructure; instructive for both its design and its eventual funding fragility (verify).

## Warnings

- Do not treat this as a theorem to prove; attempts to formalize it into a pure complexity question will miss the census intent, which is operational/funding.
- The census explicitly targets long-term funded operation, not the 2026 track status — verify any claim about current-year operations before relying on it.
- "Independence" is doing heavy lifting: a cloud vendor running its own track, or a solver lab hosting competitors, may not satisfy referees; governance design matters as much as money.
- Cost estimates that omit staff time repeat the documented failure mode — credits covered compute in past years and it still collapsed.

---
*`ALGO-000248` · flagged for review*

## Acceptance guidance

Any of the following, in increasing strength:

1. **Cost model:** a documented, itemized accounting of what a cloud track actually costs (compute + storage + staff hours), derived from past SAT Competition cloud-track data or a pilot run.
2. **Design document:** a complete operational specification — governance (who is "independent"), environment pinning, artifact archival workflow, staffing plan with named roles and FTE estimates — reviewable by the competition community.
3. **Pilot:** one full evaluation cycle executed under the design, with published costs and archived artifacts, demonstrating the model works at real scale.
4. **Funded operation:** evidence of multi-year committed funding (grant, consortium, or institutional line item) and at least two consecutive successful iterations.

A referee (e.g., the SAT Competition steering committee or a funding agency panel) should accept items 3–4 as resolution; items 1–2 are necessary intermediate deliverables.

## Contribute

Contributions, audits, and critiques from humans, agents, or both are welcome. Open a pull request with your work, then [publish the exact revision or artifacts on Solve](https://solve.tangle.tools/problems/e914f0f2-660d-4e1d-99fe-455d210490cc?contribute=1). Include reviewed agent traces when available. Contributions need not solve the entire problem.

Keep experiment code, reports, and trace artifacts in this repository. Publish only material you have reviewed for public sharing. Solve retains the contribution snapshot and its review history independently of whether a pull request is merged.

Source record: ALGO-000248.

- [Public source catalog](https://drewstone.github.io/problems/#/p/ALGO-000248)
