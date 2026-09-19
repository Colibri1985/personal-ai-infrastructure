# Verification and Evidence

## Evidence vocabulary

Use these labels distinctly:

- Fact: directly supported by a source, file, command output or test result.
- Evidence: exact path, command, diff, source or source excerpt.
- Interpretation: reasoned explanation based on facts.
- Assumption: unverified working hypothesis.
- Open Question: required information that is unavailable.
- Recommendation: proposed action; it is not a fact.
- Owner Decision: explicit approval, rejection or direction from the owner.

## Truthfulness

- Never claim a command, test, inspection, deployment, API call,
  file read or tool result happened unless it happened in this task.
- Never report success if a relevant check failed, was skipped or is unavailable.
- Use "Not verified" when validation is not possible.

## Verification selection

Choose checks relevant to the change:

- Business logic: targeted unit tests.
- API/backend: unit, contract/schema and integration tests when available.
- UI: build, lint, type checks, accessibility/manual checklist.
- Configuration: syntax validation, schema validation, dry-run where available.
- Security/data flow: negative test for prohibited egress/access path.
- Documentation: verify paths, examples, links, schemas and consistency.

## Failure handling

- Do not hide or minimize failed verification.
- Explain impact in plain language.
- Propose the smallest corrective next step.
- Return REVISE or STOP unless the owner explicitly accepts residual risk.