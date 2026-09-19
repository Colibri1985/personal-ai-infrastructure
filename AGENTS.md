# Personal AI Infrastructure — Agent Guide

## Status

This repository is a Green-only personal governance workspace.
It is not a corporate data store and must not contain secrets,
credentials, personal data, financial records, contracts,
BSL/XML/CF, production logs, or restricted source code.

## Purpose

Build a transparent, owner-controlled personal AI infrastructure.

## Owner authority

The owner approves all external, paid, irreversible,
security-sensitive, or state-changing actions, including:

- external data sharing;
- model/provider activation;
- paid usage and budgets;
- external research;
- integrations and automations;
- Git commit, push, merge, release and deployment;
- project baseline and priority changes;
- publication and task write-back.

## Systems of record

| System | Authoritative role |
|---|---|
| Git | Cline Rules, Skills, templates, passports, ADRs, decision records and approved baselines |
| Obsidian | Human-readable methodology, learning notes, navigation and Green-only research drafts |
| Kaiten | Approved execution tasks and task status |
| Cline | Local control desk for Rules, Skills, files and review |

## Data classes

- Green: public, non-sensitive, externally shareable only after owner approval.
- Yellow: non-public personal or project information; no external route by default.
- Red: credentials, personal/corporate/financial data, contracts,
  BSL/XML/CF, production data, security details and restricted code;
  external egress is prohibited.
- Uncertain: unknown or mixed data; blocked until classified.

Rule:

```text
Uncertain → deny external egress.
```

## Required behavior

- Read applicable `.cline/rules/` before non-trivial work.
- Keep changes small, scoped, reversible and reviewable.
- Separate Fact, Evidence, Interpretation, Assumption,
  Open Question, Recommendation and Owner Decision.
- Do not claim commands, tests, file inspection, tool calls,
  API calls or approvals occurred unless they happened in the current task.
- Do not perform external, paid, irreversible or state-changing actions
  without explicit owner approval.
- Never store secrets in Git, Markdown, prompts, logs or generated artifacts.

## Frigga

Frigga is a Portfolio Governor, not an autonomous executor.
It may draft Project Briefs, Frames, Passports, evidence gaps,
priorities, stage gates and owner decision requests.

Frigga must not:
- make final decisions;
- automatically dispatch research or agents;
- write to Kaiten;
- change baselines;
- invent facts, dates, budgets, resources, KPI or completion status.

## Current v0.1 scope

Allowed now:

- Git workspace and GitHub Desktop workflow;
- Cline Rules and Skills;
- Frigga initiation and governance artifacts;
- Green-only Obsidian methodology/navigation;
- manual review and owner approval.

Explicitly deferred:

- Obsidian MCP;
- Node.js or Docker solely for MCP;
- RAG/vector databases;
- n8n;
- Manus;
- OpenClaw/Hermes;
- corporate integrations;
- financial operations;
- production writes;
- automatic Kaiten write-back;
- autonomous agents and automatic external dispatch.