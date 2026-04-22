<!--
Thank you for contributing to EGAProtocol. Please complete this checklist before
requesting review. All items are required unless explicitly marked optional.
-->

## Summary

<!-- One paragraph: what does this PR change, and why? -->

## Type of Change

- [ ] Specification bug fix (non-breaking correction to protocol behaviour)
- [ ] Clarification or editorial (wording, examples, cross-references — no behaviour change)
- [ ] New content (new section, message type, or primitive)
- [ ] Breaking change (requires major version bump — flag this explicitly)
- [ ] Positioning / documentation (EXPANSIONS.md, GOVERNANCE.md, CONTRIBUTING.md, README.md)
- [ ] Infrastructure (CI, templates, tooling — no spec change)

## Affected Sections

<!-- List the SPEC.md sections (or other files) modified. -->

## Governance Primitives Affected

- [ ] Identity
- [ ] Authorization
- [ ] Audit
- [ ] Approvals
- [ ] Alerts
- [ ] None (infrastructure / editorial)

## Checklist

### Required for all PRs

- [ ] I have read [CONTRIBUTING.md](CONTRIBUTING.md).
- [ ] My commit(s) carry a `Signed-off-by` line (DCO). See [Section 6 of CONTRIBUTING.md](CONTRIBUTING.md#6-developer-certificate-of-origin-dco).
- [ ] My commit messages follow the [commit conventions](CONTRIBUTING.md#7-commit-and-pr-conventions).
- [ ] I have searched existing Issues and PRs for duplicates.

### Required for specification changes

- [ ] The change preserves backward compatibility within the current major version, **OR** I have clearly marked this as a breaking change requiring a major version bump.
- [ ] The change is compatible with air-gapped, sovereign deployments (no mandatory external connectivity added).
- [ ] If a new mandatory field is introduced, I have updated the conformance criteria in Section 19 of SPEC.md.
- [ ] If a new message type is introduced, I have added it to the message type registry in Appendix A and Appendix B.
- [ ] Example flows in Appendix C are updated or a new example is added.

### Required for breaking changes

- [ ] This PR has been discussed in a GitHub Issue or GitHub Discussion before being opened.
- [ ] A draft EIP (EGAP Improvement Proposal) exists in `proposals/` or is linked below.
- [ ] The TSC has been notified (tag `@egaprotocol/tsc` in the PR or referenced Issue).

## Related Issues / EIPs

<!-- Closes #xxx or References #xxx -->

## Testing / Validation

<!-- For spec changes: describe how the change was validated.
     e.g. "Reviewed against the JSON-RPC binding in Appendix A",
     "No reference implementation exists yet; validation is editorial only." -->

## Additional Notes

<!-- Anything else reviewers should know. -->
