---
title: ADR-004 Obsidian Role and MCP Integration Decision
status: draft_for_owner_approval
date: 2026-09-19
decision_date: null
owner: "[OWNER_NAME]"
classification: green
tags:
  - adr
  - architecture
  - obsidian
  - mcp
  - governance
superseded_by: null
related: []
---

# ADR-004: Obsidian Role and MCP Integration Decision

## Status

**Draft for owner approval.** This ADR becomes approved only after the owner explicitly accepts it and records the decision in Git.

## Context

The personal AI infrastructure uses distinct systems for distinct responsibilities:

| System | Authoritative role |
|---|---|
| Git repository `personal-ai-infrastructure` | Executable governance artifacts: Cline Rules, Cline Skills, Cline-owned templates, approved project passports, schemas, ADRs, decision records, version history and approved baselines |
| Obsidian vault `PMO_Knowledge_Base` | Human-readable methodology, Maps of Content, learning/reference notes, Green-only research drafts and navigation |
| Kaiten | Approved execution tasks and task status |
| Cline Desktop | Local control desk for rules, skills, files, reviews and controlled implementation |
| Owner | Final authority for priority, policy, budget, data sharing, external execution, baseline changes and acceptance |

A possible future integration would allow Cline to read selected Obsidian materials through an MCP server. This ADR decides whether that integration belongs in v0.1.

## Decision

**The v0.1 architecture is Git/Cline-first. Obsidian MCP is deferred.**

Obsidian remains a human knowledge layer. Git remains authoritative for executable artifacts and approved baselines. Cline runs from the local Git workspace. No Obsidian MCP server, plugin, API key or automatic synchronization is installed or configured in v0.1.

## Rationale

1. **Executable governance needs version control.** Cline Rules, `SKILL.md`, Cline-owned templates, passports and decision records must have visible diffs, reviewed commits and reversible baselines.

2. **Obsidian serves a different purpose.** It is the readable learning/reference layer, not the runtime location for Cline execution policy.

3. **Least privilege.** A primary personal vault can contain mixed or sensitive notes. Connecting it to a coding/agent environment before technical restrictions are tested would expand the attack surface.

4. **Incremental adoption.** The Git/Cline-first target architecture must first be validated through practical Frigga pilots. MCP may solve a future demonstrated friction, but it is not required for the initial workflow.

5. **No trust based only on prompts.** A Markdown rule in an Obsidian vault is an instruction to a model, not technical access control. A future integration must use an isolated vault and enforce a technical allowlist.

## Consequences

### Positive

- Clear separation between executable governance and human-readable knowledge.
- Git history and diffs for Rules, Skills, templates, passports and decisions.
- Lower risk of accidental access to personal/corporate notes.
- No dependency on an unreviewed MCP server during v0.1.
- Fewer components, secrets and update obligations.

### Trade-offs

- Specific methodology notes may occasionally need to be copied or linked into `docs/methodology/` when a Cline Skill repeatedly needs them.
- There is no automatic synchronization between Obsidian and Cline in v0.1.
- The owner must decide deliberately when a human note becomes an executable governance artifact.

## v0.1 implementation

### We do

- Keep Cline Rules in `.cline/rules/` in the Git workspace.
- Keep `frigga-portfolio-governor/SKILL.md` and Cline-owned templates in `.cline/skills/`.
- Keep approved project passports, ADRs and baselines in Git.
- Keep PMO methodology, MOC/navigation and learning notes in a separate Green-only Obsidian vault.
- Copy or link only selected approved methodology notes into `docs/methodology/` if a Skill needs repeated access.
- Run 2–3 Green-only Frigga pilots before considering MCP.

### We do not do

- Install an Obsidian MCP server, Local REST API plugin, Node package or Docker container for MCP in v0.1.
- Configure Cline to access an Obsidian vault through MCP.
- Store executable Rules/Skills only in Obsidian.
- Connect a primary personal vault or any corporate vault to Cline.
- Treat `.cline-rules.md` inside Obsidian as technical access control.
- Enable automatic synchronization, write-back or task creation from Cline into Obsidian/Kaiten.

## Future MCP adoption gate

MCP testing may start only if **all** conditions below are satisfied and the owner explicitly approves the isolated test:

- [ ] Two or three Frigga pilots have completed successfully using the Git/Cline-first workflow.
- [ ] A separate Green-only test vault exists; it is not the primary personal vault and not a corporate vault.
- [ ] The candidate MCP server has a public repository, identifiable maintainer, open-source license and reproducible installation instructions.
- [ ] The server's dependencies, permissions, data paths and network behavior have been reviewed.
- [ ] There are no known unresolved critical vulnerabilities relevant to the proposed setup.
- [ ] The server can be restricted technically to the designated test vault/path.
- [ ] Initial access is read-only; write tools are absent or disabled.
- [ ] API keys/credentials are stored outside Git, Obsidian and Markdown.
- [ ] A test plan covers allowed reads, denied paths, error handling, logging and shutdown.
- [ ] A kill switch/rollback procedure has been tested.
- [ ] The owner approves the exact server, permissions, vault and test scope.

## Risks and mitigations

| Risk | Mitigation |
|---|---|
| Sensitive notes become visible to Cline | Do not connect primary/corporate vaults; use separate Green-only test vault only |
| MCP server vulnerability or malicious dependency | Review repository, maintainer, license, dependencies, permissions and network behavior; start read-only |
| Source-of-truth ambiguity | Git is authoritative for executable artifacts; Obsidian is authoritative for human-readable methodology/navigation |
| MCP disrupts workflow | Test in isolation; disable MCP and return to Git/Cline-first workflow |
| Credentials leak | Store credentials only in approved secure settings; never Git, Markdown or Obsidian |

## Rollback plan

If a future MCP test causes any issue:

1. Disable/remove the MCP server from Cline configuration.
2. Revoke/rotate the corresponding key if one was used.
3. Confirm the test vault is disconnected.
4. Continue operating through the Git/Cline-first workflow.
5. Record the issue and root cause before any future retry.

## Review trigger

Review this ADR only after:

- two or three completed Frigga pilots;
- a specific, repeated friction in using selected Obsidian notes from Cline;
- a reviewed MCP candidate;
- explicit owner request to evaluate an isolated test.

## Owner decision

- [ ] Approve ADR-004 as written.
- [ ] Revise ADR-004.
- [ ] Defer the decision.

## References

- `.cline/skills/frigga-portfolio-governor/SKILL.md`
- `.cline/rules/60-frigga-project-governance.md`
- `docs/frigga-initiation-sop-v1.1.md`
- `context/context-brief-v1.0.md` once approved
