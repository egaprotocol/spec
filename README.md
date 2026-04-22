# EGAProtocol

**The open protocol that brings discipline to AI agents.**

EGAP is an open specification for governed communication between orchestration engines and AI agents — the identity, authorization, audit, approvals, and alerts required wherever autonomous systems are trusted with real-world action.

[![Spec Status](https://img.shields.io/badge/spec-v0.1%20draft-orange)](./SPEC.md)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](./LICENSE)
[![DCO](https://img.shields.io/badge/DCO-required-green)](./CONTRIBUTING.md#6-developer-certificate-of-origin-dco)

---

## What EGAP Stands For

**EGAP** is the permanent name. The expansion flexes by audience:

- To engineers — **Engine Governed Agents Protocol**
- To enterprises — **Enterprise Governance for Agents Protocol**
- To regulators — **Evidence-based Governance for AI Protocols**
- To the open-source community — **Every Governed Agent Protocol**
- To ethics and research audiences — **Ethical Governance for Agentic Platforms**
- To operations leaders — **Elevated Governance of Autonomous Processes**

All expansions describe the same protocol. See [EXPANSIONS.md](./EXPANSIONS.md) for the full philosophy and usage guidance.

---

## The Governance Gap

The agent protocol landscape today solves for connectivity, not accountability.

| Protocol | Purpose | Governance |
|---|---|---|
| **MCP** (Anthropic) | Tools and context for LLMs | None specified |
| **A2A** (Google) | Agent-to-agent interoperability | None specified |
| **EGAP** | Engine-to-agent dispatch with governance | Required |

MCP lets an LLM call a tool. A2A lets an agent call another agent. Neither specifies how the calling party is authenticated, how the action is authorized, how it is audited, how humans approve destructive operations, or how anomalies are alerted.

For regulated industries — banking, healthcare, defense, government, critical infrastructure — connectivity without governance is unshippable.

**EGAP defines the governance layer.** Every message carries identity, permission scope, audit correlation, time context, and budget state. Every destructive action triggers a mandatory human approval checkpoint. Every decision is recorded immutably.

---

## Status

This is a **draft specification (v0.1)**. The protocol is being developed publicly. Breaking changes should be expected until v1.0.

- **Current version:** v0.1
- **Specification:** [SPEC.md](./SPEC.md)
- **Expansions and positioning:** [EXPANSIONS.md](./EXPANSIONS.md)
- **Governance:** [GOVERNANCE.md](./GOVERNANCE.md)
- **Contributing:** [CONTRIBUTING.md](./CONTRIBUTING.md)
- **Security:** [SECURITY.md](./SECURITY.md)

---

## Core Principles

1. **Governance is mandatory, not optional.** Every message carries governance metadata. There is no "unauthenticated mode."
2. **The agent proposes, the engine disposes.** Agents request actions. Engines validate, authorize, and dispatch.
3. **Human-in-the-loop is a protocol primitive.** Approval gates are first-class message types, not application-level conventions.
4. **Every decision is auditable.** Audit events follow OpenTelemetry semantic conventions and are immutable.
5. **Sovereignty by default.** No outbound calls required. Runs in air-gapped environments.
6. **Open standard, multiple implementations.** The specification is free. Conformance is certified.

---

## Relationship to MCP and A2A

EGAP is **complementary**, not competitive.

- An engine can speak **MCP** to fetch tools for an agent.
- An agent can speak **A2A** to coordinate with peer agents.
- The engine-to-agent dispatch, approval flow, and audit trail use **EGAP**.

A production governed agent system typically speaks all three.

---

## Who Should Implement EGAP

- **Platform teams** operating AI agents in regulated environments (BFSI, healthcare, defense, public sector, critical infrastructure).
- **Vendors** building orchestration engines, agent SDKs, or agent marketplaces who need a governance contract with their customers' compliance teams.
- **Enterprise architects** defining their organisation's AI governance posture and needing an open standard to anchor it.
- **Regulators and standards bodies** seeking evidence-based, technically verifiable AI governance primitives.
- **Researchers and practitioners** working on accountable, explainable, human-governed AI systems.

---

## Why This Matters Now

AI agents are being deployed into production faster than the governance models around them are maturing. The pattern is familiar: the first wave of any powerful technology arrives without its safety infrastructure, and the infrastructure is built retroactively, at higher cost, under regulatory pressure, after something has gone wrong.

EGAP is an attempt to build the governance layer alongside the capability layer — not after it. The protocol exists so that an enterprise deploying AI agents into a payment system, a hospital, a grid control centre, or a government service can answer, with cryptographic certainty: who acted, on whose behalf, with whose permission, under what constraints, with what outcome, and with what evidence.

Without that layer, autonomous agents in critical infrastructure are a risk no regulator will accept. With it, they become infrastructure itself.

---

## Getting Involved

- **Read the spec:** [SPEC.md](./SPEC.md)
- **Understand the positioning:** [EXPANSIONS.md](./EXPANSIONS.md)
- **Propose a change:** See [GOVERNANCE.md](./GOVERNANCE.md) for the EGAP Improvement Proposal (EIP) process.
- **Report an issue:** Use the GitHub issue tracker.
- **Report a security issue:** See [SECURITY.md](./SECURITY.md).
- **Join the discussion:** GitHub Discussions on this repository.
- **Implement EGAP:** See [CONTRIBUTING.md](./CONTRIBUTING.md) Section 10 and submit a PR to `ADOPTERS.md`.

---

## Attribution

EGAProtocol is an open specification originally developed at **Mirastack Labs Private Limited** and released under the Apache License 2.0. Mirastack Labs maintains EGAProtocol in collaboration with the community under the governance model described in [GOVERNANCE.md](./GOVERNANCE.md).

EGAProtocol and EGAP are names of an open specification. They may be used freely to describe conformant implementations, tutorials, academic work, research publications, and compatible products — subject to the guidance in [EXPANSIONS.md](./EXPANSIONS.md).

---

## License

This specification and all associated artifacts are licensed under the [Apache License 2.0](./LICENSE).

Documentation files including EXPANSIONS.md, CONTRIBUTING.md, and GOVERNANCE.md are additionally licensed under Creative Commons Attribution 4.0 (CC-BY-4.0) for unrestricted quotability.

Copyright © 2026 Mirastack Labs Private Limited.

---

**Project home:** https://egaprotocol.org
**Specification repository:** https://github.com/egaprotocol/spec
**Contact:** hello@egaprotocol.org