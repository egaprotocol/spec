---
name: Specification Bug
about: >-
  The spec says something incorrect, internally inconsistent, or technically
  infeasible to implement as written.
title: "[spec-bug] "
labels: ["spec-bug", "triage"]
assignees: []
---

<!--
Before filing: search open and closed Issues for duplicates.
This template is for bugs IN THE SPECIFICATION — incorrect protocol behaviour,
internal contradictions, or ambiguities that block implementation.
For feature proposals, use the "Feature Request" template.
For general spec questions, use the "Spec Clarification" template.
-->

## Summary

<!-- One sentence: what is wrong and where is it. -->

## Affected Section

<!-- Link or cite the specific section(s) of SPEC.md. e.g. "Section 8.3 — Budget Enforcement" -->

**SPEC.md section:**
**Line / paragraph reference (if applicable):**

## Governance Primitive Affected

<!-- Which of the five EGAP primitives is impacted? -->

- [ ] Identity
- [ ] Authorization
- [ ] Audit
- [ ] Approvals
- [ ] Alerts
- [ ] None of the above (infrastructure / general spec structure)

## Description

<!-- Describe the bug. What does the spec currently say? What is wrong about it? -->

**Current spec text (quote or paraphrase):**

**Why it is incorrect or inconsistent:**

## Impact

<!-- What breaks if a conformant implementation follows the spec as written? -->

**Severity:** <!-- Critical / High / Medium / Low -->

<!-- Critical = governance bypass possible. High = security or correctness impact. Medium = implementation difficulty or ambiguity. Low = editorial. -->

## Proposed Fix

<!-- Optional: suggest corrected spec language. If you're unsure, leave this blank. -->

## References

<!-- Any related Issues, PRs, specs, RFCs, or prior discussion. -->

---

*By submitting this issue, you confirm you have read [CONTRIBUTING.md](../CONTRIBUTING.md)
and agree to the [Code of Conduct](../CODE_OF_CONDUCT.md).*
