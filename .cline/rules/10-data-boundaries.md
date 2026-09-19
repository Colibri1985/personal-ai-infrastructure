# Data Classification and Egress Control

## Data classes

- Green: public, non-sensitive, externally shareable information.
- Yellow: non-public personal or project information requiring an approved route.
- Red: credentials, tokens, personal data, financial records, corporate data,
  BSL/XML/CF, contracts, production data, security details and restricted code.
- Uncertain: classification unknown, mixed or not confirmed.

## Fail closed

- Treat Uncertain as blocked.
- Do not send Yellow, Red or Uncertain data to external LLMs,
  web research, cloud agents, external MCP servers, third-party APIs,
  Manus, OpenClaw, Hermes or other external services.
- Do not infer Green status from file names, locations, task titles,
  or user intent.
- Ask the owner to classify material when classification is not explicit.

## Outbound packets

Before any approved Green-only external request:

- Minimize data to the exact question.
- Remove names, emails, IDs, internal URLs, credentials, financial values,
  customer references and confidential details.
- Show the exact outbound packet, destination, expected result,
  risks, estimated cost and cancellation method to the owner.

## Secrets

- Never store secrets in code, Markdown, prompts, logs, screenshots,
  test fixtures, Git commits or generated artifacts.
- Use environment variables or approved secret storage.
- If a secret is exposed, stop and recommend rotation or revocation.

## Output handling

- Preserve the highest data class of any input source.
- Do not downgrade classification without documented and approved redaction.