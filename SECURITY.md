# Security Policy

## Supported Versions

EGAProtocol is a specification, not executable software. "Security" in the context of this
repository covers:

- **Specification vulnerabilities** — design flaws in the EGAP protocol that could, if
  implemented as specified, introduce identity spoofing, authorization bypass, audit tampering,
  approval circumvention, or alert suppression.
- **Infrastructure vulnerabilities** — security issues in tooling, CI/CD pipelines, or
  published artifacts in this repository.

| Version | Status               |
|---------|----------------------|
| v0.1    | Active — current draft |

---

## Reporting a Vulnerability

**Do not report security vulnerabilities through public GitHub Issues.**

Send a detailed report to **security@egaprotocol.org**.

### What to include

- Description of the vulnerability and the affected section of the specification (or infrastructure).
- Potential impact: which governance primitive is affected (identity, authorization, audit,
  approvals, alerts), and in what scenarios.
- Steps to reproduce or a proof-of-concept (if applicable to a reference implementation).
- Your name and contact information (for acknowledgment; anonymous reports are also accepted).

### What to expect

| Timeline   | Action |
|------------|--------|
| 48 hours   | Acknowledgment of receipt |
| 14 days    | Initial assessment and severity classification |
| 90 days    | Target resolution (public disclosure after fix, or at 90 days if no fix is available) |

We follow a **90-day coordinated disclosure window**. If the issue requires a longer timeline,
we will communicate this explicitly before day 90.

If you believe the issue is critical and requires immediate public disclosure, please state
that in your report and we will coordinate accordingly.

---

## Scope

**In scope:**

- Protocol design flaws affecting any of the five governance primitives: identity,
  authorization, audit, approvals, alerts.
- Cryptographic weaknesses in the authentication or audit mechanisms described in SPEC.md.
- Authorization bypass patterns that could be exploited by a conformant but malicious implementation.
- Specification ambiguities that a conformant implementation could exploit to bypass governance.

**Out of scope:**

- Vulnerabilities in third-party implementations of EGAP (report those to the respective maintainer).
- General AI safety concerns not specific to the EGAP governance model.
- Issues in reference links, broken URLs, or documentation typos (use GitHub Issues for these).

---

## Responsible Disclosure

We ask that reporters:

- Allow us the 90-day window before public disclosure.
- Avoid accessing, modifying, or deleting data beyond what is necessary to demonstrate the vulnerability.
- Act in good faith.

We commit to:

- Treating all reports with confidentiality until disclosure.
- Crediting reporters in security advisories (unless anonymous disclosure is requested).
- Not pursuing legal action against good-faith security researchers.

---

## Contact

**Primary:** security@egaprotocol.org  
**General enquiries:** hello@egaprotocol.org  
**Project home:** https://egaprotocol.org

EGAProtocol is maintained by MIRASTACK LABS Private Limited.
