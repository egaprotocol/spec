# Contributing to EGAP

Thank you for your interest in contributing to EGAP — the Engine Governed Agents Protocol. This document explains how to participate in the project — whether you're fixing a typo, proposing a new message type, or implementing EGAP in a new language.

EGAP is an open specification released under Apache License 2.0. Contributions are welcome from anyone, regardless of affiliation. All contributors are bound by the project's [Code of Conduct](CODE_OF_CONDUCT.md) and governed under [GOVERNANCE.md](GOVERNANCE.md).

For background on how EGAP is positioned across different audiences — engineering, enterprise, regulatory, open-source, ethics, and operations — see [EXPANSIONS.md](EXPANSIONS.md).

---

## Table of Contents

1. Ways to Contribute
2. Before You Start
3. Reporting Issues
4. Proposing Changes
5. Pull Request Process
6. Developer Certificate of Origin (DCO)
7. Commit and PR Conventions
8. Review Process
9. EGAP Improvement Proposals (EIPs)
10. Implementing EGAP
11. Security Issues
12. Trademark Use
13. Communication
14. Getting Help
15. Recognition

---

## 1. Ways to Contribute

There is no single "right" way to contribute. Useful contributions include:

- **Reporting issues** — bugs in the specification, ambiguous language, missing edge cases.
- **Improving documentation** — clarifying spec language, adding examples, improving diagrams.
- **Reviewing Pull Requests** — engaging with others' proposals with technical feedback.
- **Writing reference implementations** — in Go, Python, Rust, Java, TypeScript, or any other language.
- **Building conformance tests** — adding coverage to the conformance test suite.
- **Writing EIPs** — proposing substantive changes via the EGAP Improvement Proposal process.
- **Implementing EGAP in your product** — and telling us about it so we can list you in `ADOPTERS.md`.
- **Publishing case studies, talks, or tutorials** — expanding the community's collective understanding.

Small contributions are valuable. A one-character typo fix is as welcome as a 500-line conformance test.

---

## 2. Before You Start

### 2.1 Read the Specification

Before proposing changes, please read the current [SPEC.md](SPEC.md). Many common questions are answered there. Reviewing recent merged Pull Requests and open Issues also helps avoid duplication.

### 2.2 Understand the Scope

EGAP governs Engine-to-Agent communication with a specific focus on governance: authentication, authorization, audit, approvals, alerts. Contributions that align with this scope are more likely to be accepted. Contributions that attempt to expand the protocol into unrelated domains (tool invocation, peer messaging, model serving) will typically be redirected to complementary protocols such as MCP, A2A, or OpenTelemetry.

EGAP is deliberately positioned as an audience-flexible standard — relevant to engineers, enterprises, regulators, operations leaders, the open-source community, and ethics researchers simultaneously. See [EXPANSIONS.md](EXPANSIONS.md) for the full positioning guidance. Contributions that clarify EGAP for a specific audience without forking the technical spec are welcome.

### 2.3 Check Existing Work

Before filing an Issue or opening a Pull Request:

- Search existing [Issues](https://github.com/egaprotocol/spec/issues) for duplicates.
- Search merged and open [Pull Requests](https://github.com/egaprotocol/spec/pulls).
- Check [proposals/](proposals/) for existing EIPs covering the same topic.

If someone is already working on what you have in mind, consider collaborating rather than duplicating effort.

---

## 3. Reporting Issues

Issues are for bug reports, specification ambiguities, clarification requests, and feature proposals that don't yet rise to the level of an EIP.

### 3.1 Issue Types

When filing an Issue, please use one of the following templates (available in `.github/ISSUE_TEMPLATE/`):

- **Specification bug** — the spec says something incorrect or internally inconsistent.
- **Specification ambiguity** — the spec is unclear or open to multiple interpretations.
- **Clarification request** — you want to understand intent behind a design choice.
- **Feature request** — you want to propose a new capability (may be promoted to an EIP).
- **Documentation issue** — READMEs, examples, or supporting docs need improvement.
- **Positioning / expansion question** — questions about how EGAP is described to a specific audience (routes to EXPANSIONS.md maintainers).

### 3.2 Good Issue Reports Include

- A clear title describing the issue in one sentence.
- The exact version of the specification being discussed (e.g., v0.1).
- The specific section, line, or example at issue.
- Expected behavior versus actual/specified behavior.
- Impact — who is affected and how.
- Suggested resolution, if any.

### 3.3 Triage

Issues are triaged by Committers within 7 calendar days of filing. Triage outcomes include:

- **Accepted** — the Issue is valid and will be addressed.
- **Needs more information** — the Issue needs clarification before action.
- **Duplicate** — closed with a link to the existing Issue.
- **Out of scope** — closed with explanation of scope boundaries.
- **Promote to EIP** — the Issue warrants a formal proposal.

---

## 4. Proposing Changes

EGAP uses a tiered change process defined in [GOVERNANCE.md Section 5](GOVERNANCE.md#5-decision-making-process). Briefly:

| Change Type | Process |
|---|---|
| Typos, trivial clarifications | Direct Pull Request |
| Example updates, non-normative additions | Pull Request with Maintainer review |
| New fields, non-breaking additions | EIP (Standards Track) |
| Breaking changes, new message types | EIP with two-thirds Maintainer approval |
| Governance changes | EIP (Meta) with TSC approval |
| New canonical expansion in EXPANSIONS.md | EIP (Meta) with TSC approval |

If you are unsure which tier applies, open an Issue first and ask. A Maintainer will guide you to the right process.

---

## 5. Pull Request Process

### 5.1 Fork and Branch

- Fork the repository to your own GitHub account.
- Create a feature branch from `main` with a descriptive name: `fix/section-7-typo`, `feat/add-websocket-example`, `docs/improve-glossary`.
- Avoid working directly on your fork's `main` branch.

### 5.2 Keep PRs Focused

- One logical change per PR. Do not bundle unrelated fixes.
- Separate formatting-only changes from substantive changes.
- If your PR grows beyond ~500 lines of diff, consider splitting it.

### 5.3 Write Good Commit Messages

Commit messages follow the Conventional Commits format:

```
<type>(<scope>): <short summary>

<body — optional, explains what and why, not how>

<footer — references to Issues/EIPs, DCO sign-off>
```

**Types** used in this project:

- `spec` — changes to the specification text.
- `docs` — changes to documentation (README, CONTRIBUTING, EXPANSIONS, etc.).
- `examples` — changes to example code or flows.
- `proto` — changes to Protocol Buffer schemas.
- `schema` — changes to JSON schemas.
- `ci` — changes to CI/CD configuration.
- `chore` — maintenance tasks, dependency updates.

**Example:**

```
spec(section-7): clarify Budget wall-clock tracking responsibility

The previous text was ambiguous about whether Engine or Agent
is authoritative for wall-clock enforcement. Clarifies that both
MUST track independently and Engine is authoritative for termination.

Refs #42
Signed-off-by: Ada Lovelace <ada@example.org>
```

### 5.4 Open the Pull Request

- Use the PR template at `.github/PULL_REQUEST_TEMPLATE.md`.
- Reference any related Issues (`Refs #42`, `Closes #42`).
- If the PR implements an EIP, reference the EIP number (`Implements EIP-007`).
- Mark the PR as draft if it is not ready for review.

### 5.5 Respond to Review

- Address reviewer comments promptly (within 7 days where possible).
- If you disagree with a reviewer, explain your reasoning in the thread rather than pushing past the disagreement.
- Force-pushes are permitted on your feature branch during review.
- Do not resolve reviewer comments unilaterally — let the reviewer confirm their concern is addressed.

---

## 6. Developer Certificate of Origin (DCO)

EGAP uses the **Developer Certificate of Origin (DCO)** for contribution licensing. We do not use a Contributor License Agreement (CLA).

### 6.1 What the DCO Means

By signing off on each commit, you affirm that:

- You wrote the contribution yourself, OR
- The contribution is based on work that is appropriately licensed and you have the right to submit it under the project's license, AND
- Your contribution is made under the project's license (Apache 2.0).

The full text of the DCO is at https://developercertificate.org/.

### 6.2 How to Sign Off

Every commit MUST include a `Signed-off-by:` line at the end of the commit message, matching the author name and email on the commit:

```
Signed-off-by: Ada Lovelace <ada@example.org>
```

Add this automatically with:

```bash
git commit -s -m "spec: clarify budget enforcement"
```

The `-s` flag appends the sign-off using your configured Git `user.name` and `user.email`.

### 6.3 Enforcement

All PRs are checked automatically by the DCO bot. PRs with unsigned commits cannot be merged. If you forget to sign off, you can amend with:

```bash
git commit --amend --signoff
git push --force-with-lease
```

Or for multi-commit PRs:

```bash
git rebase --signoff HEAD~N
git push --force-with-lease
```

### 6.4 Pseudonymous Contributions

Pseudonymous contributions are accepted provided the DCO sign-off is consistent (same pseudonym and email across all contributions) and you can be reliably contacted via the email address used.

---

## 7. Commit and PR Conventions

### 7.1 Commit Granularity

- Each commit should represent one logical change.
- Rebase and squash work-in-progress commits before opening a PR.
- Do not squash commits that represent genuinely separate logical changes — reviewers benefit from seeing the progression.

### 7.2 Branch Protection

The `main` branch is protected:

- No direct pushes. All changes go through PRs.
- At least one approving review from a Committer is required.
- DCO sign-off check must pass.
- CI checks must pass.
- Signed commits (optional but encouraged — GPG or SSH signing).

### 7.3 PR Size Guidance

- **< 50 lines:** usually mergeable within 1–2 business days after review.
- **50–500 lines:** expect 3–7 days of review depending on complexity.
- **> 500 lines:** consider splitting, or expect a longer review cycle.

---

## 8. Review Process

### 8.1 Who Reviews

- Any Committer may review any PR.
- Maintainers responsible for the area of change provide final approval.
- For EIP-level changes, at least two Maintainers must approve.

### 8.2 Review Standards

Reviewers evaluate:

- **Correctness** — does the change accurately reflect intended protocol behavior?
- **Clarity** — is the change understandable to readers not involved in authoring it?
- **Consistency** — does it use terminology and style consistent with the rest of the spec?
- **Backward compatibility** — does it preserve existing conformance?
- **Scope** — is it within the project's defined scope per Section 2.2?
- **Audience neutrality** — for specification changes, does the text remain neutral across the audiences described in EXPANSIONS.md?

### 8.3 Merge Authority

- **Trivial** changes: any Committer may merge after self-review plus DCO and CI passing.
- **Standard** changes: require one approving review from a Committer other than the author.
- **Significant** changes: require EIP ratification before merge.
- **Breaking** changes: require EIP ratification plus TSC approval before merge.

### 8.4 Merge Style

- Small PRs: **squash and merge**.
- Multi-commit PRs with logically separate commits: **rebase and merge**.
- **No merge commits** into `main`.

---

## 9. EGAP Improvement Proposals (EIPs)

Substantive changes proceed through the EIP process. Full details in [GOVERNANCE.md Section 6](GOVERNANCE.md#6-egaprotocol-improvement-proposals-eips). Summary:

### 9.1 When to Write an EIP

Any of the following require an EIP:

- New Core Message Types
- New Error Codes
- Changes to Governance Metadata schema
- Changes to Approval Flow semantics
- Changes to Audit Event schema
- Changes to Conformance Criteria
- Breaking changes to binding definitions
- Governance document changes
- Addition of a new canonical expansion in EXPANSIONS.md

### 9.2 How to Start

1. Open an Issue describing the proposed change at a high level.
2. Gauge Maintainer interest and scope alignment.
3. Copy `proposals/EIP-TEMPLATE.md` to `proposals/EIP-XXX-short-name.md` (XXX assigned on first merge).
4. Open a draft PR with your EIP.
5. Iterate in review until the EIP reaches `LAST_CALL` status.
6. Formal vote per GOVERNANCE.md Section 5.3.

### 9.3 EIP Quality Expectations

Good EIPs are:

- **Motivated** — the problem being solved is clearly stated.
- **Specific** — the proposed change is precise, not aspirational.
- **Justified** — the Rationale section addresses alternatives considered.
- **Compatibility-aware** — backward compatibility impact is analyzed honestly.
- **Implemented** — a reference implementation exists for Standards Track EIPs.

---

## 10. Implementing EGAP

### 10.1 Implementation Repositories

Reference and community implementations live in separate repositories:

- `github.com/egaprotocol/core` — Go reference implementation.
- `github.com/egaprotocol/conformance` — conformance test suite.
- Community implementations are listed in [ADOPTERS.md](ADOPTERS.md) (forthcoming).

### 10.2 Conformance

An implementation claims EGAP conformance by passing the published conformance test suite and meeting the criteria in SPEC.md Section 19. A forthcoming **EGAP Certified** program will provide formal conformance attestation.

### 10.3 Listing Your Implementation

If you implement EGAP, submit a PR adding your implementation to `ADOPTERS.md` with:

- Implementation name
- Link (GitHub, website)
- Language(s)
- Binding(s) supported (JSON-RPC, gRPC, or both)
- Status (production, beta, experimental)
- Contact for implementation questions

### 10.4 Non-Conformant Use

Use of the EGAP or EGAProtocol name to describe an implementation that does not pass conformance tests is not permitted under the project's trademark policy. See Section 12.

---

## 11. Security Issues

**Do NOT file security vulnerabilities as public GitHub Issues.**

Report security issues privately to `security@egaprotocol.org`. See [SECURITY.md](SECURITY.md) for the full coordinated disclosure policy.

Security researchers acting in good faith under the published disclosure policy will be credited in the advisory (unless anonymity is requested).

---

## 12. Naming and Brand

EGAProtocol and EGAP are names of an open specification, not trademarked product names. The names may be used freely to describe:

- Conformant implementations of the specification
- Tutorials, documentation, academic publications, and research referencing the specification
- Products that interoperate with EGAProtocol-compliant systems
- Community events, talks, and educational materials

Guidance on which expansion to use for which audience is in [EXPANSIONS.md](./EXPANSIONS.md). New canonical expansions require an EIP in the Meta category per Section 9.

What the project asks of contributors:

- Do not use the name in a way that implies sponsorship or endorsement by MIRASTACK LABS PRIVATE LIMITED where none exists.
- Do not invent new canonical expansions of EGAP outside the process in EXPANSIONS.md.
- When referring to conformance, use the EGAProtocol Certified program (forthcoming) for formal attestation.

Questions about naming or brand use can go to `hello@egaprotocol.org`.

---

## 13. Communication

### 13.1 Primary Channels

- **GitHub Issues and PRs** — technical discussion tied to specific artifacts.
- **Mailing list** — `discuss@egaprotocol.org` (forthcoming) — long-form, asynchronous.
- **Community chat** — forthcoming — casual discussion; not a substitute for written record.

### 13.2 Meeting Cadence

- **TSC meetings** — monthly, public minutes.
- **Maintainer sync** — biweekly.
- **Open community call** — quarterly, open to all contributors.

Meeting schedules and links are published at https://egaprotocol.org/community.

### 13.3 Language

The project's working language is English. We welcome translations of documentation and examples; non-English EIPs or specification text are not accepted at this stage.

---

## 14. Getting Help

- **New to open source?** Read GitHub's [open source guides](https://opensource.guide/how-to-contribute/). Then come back.
- **Stuck on a PR?** Tag `@egaprotocol/maintainers` in a comment for help.
- **Want mentorship on a first contribution?** Look for Issues labeled `good first issue` or `help wanted`.
- **Confused about positioning or which expansion to use?** Read [EXPANSIONS.md](EXPANSIONS.md). If still unclear, email `hello@egaprotocol.org`.
- **General questions?** Email `hello@egaprotocol.org`.

---

## 15. Recognition

Everyone who contributes to EGAP is recognized. Contributors are listed in:

- Git commit history (by DCO sign-off)
- Release notes for the version their contribution shipped in
- `MAINTAINERS.md` once promoted to Committer or Maintainer
- Annual contributor acknowledgments published on egaprotocol.org

We value the time and thought our contributors invest. Thank you.

---

*This document is licensed under Creative Commons Attribution 4.0 (CC-BY-4.0).*
