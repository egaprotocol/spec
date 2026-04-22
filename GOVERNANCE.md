# EGAProtocol Governance

**Version:** 1.0

**Status:** Active

**Last Updated:** 2026-04-21

---

## 1. Purpose

This document defines how the EGAProtocol specification is governed — who makes decisions, how changes are proposed and ratified, how maintainers are added and removed, and how the project is structured to evolve as an open standard.

EGAProtocol was originally developed at MIRASTACK LABS Private Limited and released to the community under Apache License 2.0. This governance model is designed to grow the project from its initial single-organization stewardship into a multi-stakeholder open standard suitable for eventual donation to a neutral foundation such as the Cloud Native Computing Foundation (CNCF) or the Linux Foundation AI & Data.

---

## 2. Guiding Principles

EGAProtocol governance is guided by the following principles:

1. **Openness.** All specification work happens in public. Private forks of the specification are discouraged.
2. **Technical merit.** Decisions are made on technical grounds, not commercial ones.
3. **Vendor neutrality.** No single organization, including MIRASTACK LABS, may unilaterally dictate the direction of the specification.
4. **Sovereign compatibility.** Changes to the specification MUST preserve the protocol's ability to function in air-gapped, on-premises, and regulated environments.
5. **Backward compatibility within major versions.** Breaking changes are reserved for major version increments.
6. **Lazy consensus.** Most decisions move forward unless actively objected to, reducing coordination overhead.
7. **Written record.** All significant decisions produce a durable written artifact.

---

## 3. Roles

EGAProtocol defines four roles. Individuals may hold multiple roles simultaneously.

### 3.1 Contributor

Anyone who submits a Pull Request, files an Issue, or participates in discussion on the project's repositories, mailing list, or community forum.

No formal appointment is required. Contributors retain copyright in their contributions and license them to the project under the terms of the DCO (Developer Certificate of Origin) sign-off on each commit.

### 3.2 Committer

A Contributor who has been granted commit access to one or more EGAProtocol repositories. Committers may:

- Merge Pull Requests after review (subject to Section 5)
- Triage Issues
- Label and close non-controversial Issues
- Represent the project in community forums

Committers are nominated by Maintainers and confirmed by the Technical Steering Committee (Section 4.3). The current list of Committers is maintained in `MAINTAINERS.md`.

### 3.3 Maintainer

A Committer who has demonstrated sustained, high-quality contribution and has been promoted to Maintainer status. Maintainers have all Committer privileges plus:

- Voting rights on EGAProtocol Improvement Proposals (EIPs)
- Nomination rights for new Committers
- Authority to approve breaking changes within the scope of their area of ownership
- Representation on the Technical Steering Committee if elected

Maintainers are confirmed by a two-thirds majority of the current Maintainer set. The current list of Maintainers and their areas of ownership is maintained in `MAINTAINERS.md`.

### 3.4 Technical Steering Committee (TSC)

The TSC is the final decision-making body for EGAProtocol. It consists of five to seven members elected from the Maintainer set. The TSC is responsible for:

- Ratifying major version releases
- Resolving disputes that cannot be resolved by lazy consensus or Maintainer vote
- Managing relationships with foundation bodies, sponsor organizations, and external standards groups
- Enforcing the Code of Conduct at the project level
- Approving changes to this governance document

The TSC is described in detail in Section 4.

---

## 4. Technical Steering Committee

### 4.1 Composition

The TSC consists of an odd number of seats between five and seven. At the time of project inception (v0.1), the TSC is constituted as follows:

- **Seats 1–3:** Appointed by MIRASTACK LABS Private Limited as the originating organization, for an initial term ending 24 months after the public launch of EGAProtocol v0.1.
- **Seats 4–5:** Reserved for elected Maintainers from the broader contributor community, filled as soon as eligible Maintainers emerge.

At the end of the initial 24-month term, all seats transition to community election as described in Section 4.4.

### 4.2 Caps and Balance

To preserve vendor neutrality, **no single organization may hold more than one-third of TSC seats** once the TSC reaches full size of five or more elected members. This cap takes effect at the end of the initial 24-month term. If the cap is violated due to organizational changes (e.g., a Maintainer's employer changes), the affected member MUST either resign from the TSC or the organization MUST reduce its representation within 90 days.

### 4.3 Responsibilities

The TSC:

- Ratifies EGAProtocol Improvement Proposals (EIPs) that affect the protocol specification, subject to Section 5.
- Approves new Committers and Maintainers.
- Adjudicates Code of Conduct escalations.
- Approves changes to this governance document by a two-thirds supermajority.
- Maintains the project roadmap.
- Represents EGAProtocol in discussions with CNCF, Linux Foundation, W3C, IETF, and other external standards bodies.
- Appoints a TSC Chair on an annual basis.

### 4.4 Elections

After the initial 24-month term, TSC seats are filled by annual election from the Maintainer pool. Election procedures:

- Nominations open 30 days before election day. Any Maintainer may self-nominate or be nominated.
- Voting is open to all Maintainers. Each Maintainer has one vote per open seat.
- Winners are determined by plurality, subject to the one-third organizational cap.
- Terms are one year, renewable without limit.
- Staggered terms are used once the TSC is fully elected: half the seats elected in even years, half in odd years.

### 4.5 Removal

A TSC member may be removed for cause (e.g., Code of Conduct violation, extended inactivity, loss of Maintainer status) by a two-thirds vote of the remaining TSC members.

---

## 5. Decision-Making Process

EGAProtocol uses a tiered decision-making model based on the significance of the change.

### 5.1 Decision Classes

| Class | Examples | Process |
|---|---|---|
| **Trivial** | Typo fixes, minor clarifications, example updates | Single Committer approval |
| **Standard** | New examples, non-normative appendix additions, clarifying rewrites | Two Maintainer approvals, 72-hour review window |
| **Significant** | New Error Codes, new non-breaking message fields, new optional features | EIP process (Section 6), simple majority of Maintainers |
| **Breaking** | Changes altering existing message semantics, removed fields, protocol version bumps | EIP process, two-thirds majority of Maintainers, TSC ratification |
| **Major Release** | Release of vX.0 from vX-1.y | TSC unanimous approval |
| **Governance Change** | Changes to this document | TSC two-thirds supermajority |

### 5.2 Lazy Consensus

For Standard and below classes, decisions move forward by lazy consensus: if no Maintainer objects within the review window, the change is considered accepted. An objection MUST cite specific technical or governance concerns and propose a path to resolution.

### 5.3 Voting

For Significant, Breaking, Major Release, and Governance Change classes, formal voting is used:

- Votes are recorded in the relevant EIP or Pull Request thread.
- Votes are `+1` (approve), `0` (abstain), or `-1` (object).
- A `-1` vote MUST include written justification. Unjustified `-1` votes are not counted.
- Votes are open for at least 7 calendar days to accommodate distributed Maintainers.

### 5.4 Tie-Breaking

Ties are broken by the TSC Chair. If the TSC Chair is absent or conflicted, ties are broken by a random selection from uninvolved TSC members.

---

## 6. EGAProtocol Improvement Proposals (EIPs)

Substantive changes to the specification proceed through the EIP process, modeled on Python PEPs, Ethereum EIPs, and IETF RFCs.

### 6.1 When an EIP is Required

An EIP is required for:

- Any change to the normative specification
- Any new Core Message Type
- Any new Error Code
- Any change to Governance Metadata schema
- Any change to Approval Flow semantics
- Any change to Audit Event schema
- Any change to Conformance Criteria
- Changes to binding definitions (JSON-RPC, gRPC)
- Any change classified as Significant, Breaking, or Major Release under Section 5.1

### 6.2 EIP Lifecycle

Every EIP progresses through the following states:

```
DRAFT → REVIEW → LAST_CALL → ACCEPTED → FINAL
                                      ↘
                                        WITHDRAWN / REJECTED
```

- **DRAFT** — Author is actively developing the proposal. Other Maintainers may comment but no vote yet.
- **REVIEW** — Author has requested feedback. Minimum 14-day review period.
- **LAST_CALL** — Proposal is considered stable. Minimum 7-day last-call period during which formal objections may be raised.
- **ACCEPTED** — Proposal has passed vote. Awaiting merge into the main specification.
- **FINAL** — Proposal is merged and active.
- **WITHDRAWN** — Author has withdrawn the proposal.
- **REJECTED** — Proposal failed vote or received sustained `-1` votes.

### 6.3 EIP Format

EIPs are Markdown files committed to `proposals/` in the spec repository. Each EIP MUST include:

- EIP number (assigned on first merge)
- Title
- Author(s) and their GitHub handles
- Status (as above)
- Type: `Standards Track`, `Informational`, or `Meta`
- Created date
- Last updated date
- Abstract (max 200 words)
- Motivation
- Specification (the actual proposed change)
- Rationale (why this approach vs alternatives)
- Backwards compatibility analysis
- Reference implementation (required for `Standards Track`)
- Security considerations
- Copyright waiver (CC0 by default)

### 6.4 EIP Numbering

EIPs are numbered sequentially starting from EIP-001. EIP-001 is reserved as the bootstrap EIP documenting the v0.1 specification itself.

---

## 7. Maintainer Lifecycle

### 7.1 Becoming a Committer

Any Contributor may be proposed as a Committer once they have:

- Contributed at least three non-trivial Pull Requests merged into main branches
- Demonstrated understanding of the governance model and technical direction
- Been active in the project for at least 90 days

Proposal: any Maintainer submits a Pull Request to `MAINTAINERS.md` adding the candidate. Simple majority of existing Maintainers approves within 14 days.

### 7.2 Becoming a Maintainer

A Committer may be proposed as a Maintainer after:

- Sustained contribution over at least 6 months as a Committer
- Evidence of independent technical judgment in area of ownership
- Demonstrated ability to mentor new Contributors

Proposal: any existing Maintainer nominates via PR to `MAINTAINERS.md`. Two-thirds of existing Maintainers approve within 14 days.

### 7.3 Emeritus Status

Maintainers who have become inactive (no contribution for 12 consecutive months) transition automatically to Emeritus status. Emeritus Maintainers retain historical recognition but lose voting rights. They may return to active Maintainer status upon resumption of activity and confirmation by the current Maintainer set.

### 7.4 Removal

A Committer or Maintainer may be removed for cause by two-thirds vote of the remaining Maintainers. Cause includes:

- Sustained Code of Conduct violations
- Malicious code contribution
- Breach of trust (e.g., private disclosure of unpublished security issues, use of Committer access to circumvent review)

Removal is a serious action. Due process requires written notice of the alleged cause, opportunity to respond, and a recorded vote.

---

## 8. Conflict of Interest

Maintainers and TSC members MUST disclose:

- Employer or primary funding source
- Any commercial product that implements EGAProtocol
- Any competing protocol specification they participate in
- Any patents or patent applications that may read on EGAProtocol

Disclosures are recorded in `MAINTAINERS.md` and updated within 30 days of material change.

Conflicted members MUST recuse themselves from votes where their conflict is material. Recusal is recorded in the vote record.

---

## 9. Intellectual Property

### 9.1 License

The EGAProtocol specification, reference implementations, and all project artifacts are licensed under Apache License 2.0 unless explicitly marked otherwise.

### 9.2 Contributor Sign-Off

All contributions MUST be accompanied by a Developer Certificate of Origin (DCO) sign-off (`Signed-off-by:` trailer on each commit) as defined at https://developercertificate.org/.

EGAProtocol does NOT use a Contributor License Agreement (CLA). DCO sign-off is sufficient.

### 9.3 Naming and Brand

EGAProtocol and EGAP are names of an open specification, not trademarked product names. The names may be used freely to describe:

- Conformant implementations of the specification
- Tutorials, documentation, academic publications, and research work referencing the specification
- Products that interoperate with EGAProtocol-compliant systems
- Community events, talks, and educational materials

Guidance on how to describe EGAProtocol for different audiences is provided in [EXPANSIONS.md](./EXPANSIONS.md). Contributors introducing new canonical expansions must follow the process described there and in [CONTRIBUTING.md](./CONTRIBUTING.md).

Misleading use of the EGAProtocol name to suggest sponsorship or endorsement by MIRASTACK LABS Private Limited where none exists is not permitted.



### 9.4 Patent Grant

All contributions are subject to the patent grant in Apache License 2.0 Section 3. Contributors explicitly grant a royalty-free patent license for any patents they hold that would necessarily be infringed by their contribution.

### 9.5 Future Assignment

In the event that the EGAProtocol project is donated to a neutral foundation (CNCF, Linux Foundation, OASIS, or similar), the TSC is authorized to transfer the specification copyright and project stewardship to the foundation on terms that preserve Apache 2.0 licensing of the specification and continued open governance. Such a transfer requires:

- Two-thirds supermajority of the TSC
- Simple majority of active Maintainers
- 30-day public comment period before the transfer is executed

---

## 10. Meetings and Communications

### 10.1 Regular Meetings

The TSC meets at least monthly via video conference. Meeting notes are published publicly within 7 days.

Maintainers are expected to attend meetings relevant to their area of ownership but attendance at every meeting is not required.

### 10.2 Asynchronous Communication

Primary asynchronous channels:

- **GitHub Issues and Pull Requests** — for all code and specification work.
- **Mailing list** (forthcoming) — for long-form discussion and announcements.
- **Community chat** (forthcoming) — for informal discussion. Not a substitute for the written record.

### 10.3 Public Record

All governance decisions MUST be captured in durable written form in a public location. Decisions made verbally MUST be ratified in writing before taking effect.

---

## 11. Code of Conduct

All participants in the EGAProtocol project are bound by the project's Code of Conduct, published as `CODE_OF_CONDUCT.md` in the spec repository and based on the Contributor Covenant v2.1.

Code of Conduct enforcement is the responsibility of the TSC. Serious violations may result in temporary or permanent removal from project participation, up to and including removal from Maintainer or TSC positions.

Reports of Code of Conduct violations SHOULD be sent to `conduct@egaprotocol.org`. A dedicated subgroup of the TSC handles reports with discretion and due process.

---

## 12. Amendment of This Document

Changes to this governance document require:

- An EIP in the `Meta` category
- Two-thirds supermajority of the TSC
- 30-day public comment period before ratification

Amendments take effect upon merge of the ratifying EIP into the main branch of the spec repository.

---

## 13. Bootstrap Provisions

Until the TSC is fully constituted and at least 12 months have elapsed from project launch:

- MIRASTACK LABS Private Limited holds the TSC majority as described in Section 4.1.
- The initial Maintainer set is drawn from MIRASTACK LABS engineers who authored the v0.1 specification.
- New Maintainer additions during the bootstrap period follow the standard Section 7 process.
- This bootstrap provision is automatically retired 24 months after the public launch of EGAProtocol v0.1 or upon ratification of a governance EIP retiring it early.

---

## 14. Contact

- **Project Chair:** To be elected. Initial contact: `governance@egaprotocol.org`
- **Security reports:** `security@egaprotocol.org`
- **Code of Conduct reports:** `conduct@egaprotocol.org`
- **General inquiries:** `hello@egaprotocol.org`
- **Project home:** https://egaprotocol.org
- **Specification repository:** https://github.com/egaprotocol/spec

---

*This governance document was approved as v1.0 upon public release of EGAProtocol v0.1. It is licensed under Creative Commons Attribution 4.0 (CC-BY-4.0).*
