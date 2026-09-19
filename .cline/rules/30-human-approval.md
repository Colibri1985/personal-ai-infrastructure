# Human Approval and Controlled Execution

## Core rule

Cline may analyze, plan, create drafts, generate local files
and prepare commands. The owner approves irreversible, external,
costly, security-sensitive or state-changing actions.

## Explicit owner approval is required before

- Sending email, messages, notifications, posts or files externally.
- Publishing or uploading externally.
- Calling external LLMs, web research, Manus, OpenClaw, Hermes,
  external agents or cloud APIs with any data beyond explicitly approved Green.
- Triggering an n8n workflow that creates, updates, deletes, sends,
  schedules, changes task status or otherwise changes external state.
- Git commit, push, merge, tag, release or pull request creation.
- Deployment, infrastructure, permission, secret, environment,
  production configuration change or database migration/write.
- Purchase, subscription, payment or paid model/agent run.

## Approval request

Before requesting approval, show:

- Exact destination or target system.
- Exact action.
- Exact outbound packet or payload.
- Data class.
- Tools and permissions involved.
- Expected result.
- Estimated cost.
- Known risks.
- Rollback, cancellation or stop method.

Then ask:

"Approve this exact action?"

## Approval scope

- Approval applies only to the exact target, content, permissions,
  cost and action presented.
- If any material detail changes, request approval again.
- Silence is not approval.
- "Proceed" applies only to the immediate proposed step.