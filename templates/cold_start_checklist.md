# Cold-Start Checklist Template

Use this checklist when restarting a local operator workstation or repository workspace after downtime, reboot, crash, or context loss.

This checklist is for visible, manual, non-live recovery only.

## Context

- Repository:
- Workstation / environment:
- Operator:
- Date / time:
- Reason for cold start:

## Entry Point

- repository root:
- primary start command:
- preflight-only command:
- expected local URLs, if any:

## Preconditions

Confirm required tools are present or explicitly missing:

- git:
- python:
- node / npm, if applicable:
- project dependencies present:
- environment variables reviewed:
- secrets not required for this path:

## Preflight

Run preflight before any full launch.

- command run:
- exit status:
- expected outputs observed:
- unexpected warnings:
- required manual action:

## Launch, If Explicitly Allowed

Only continue if launch is manual, visible, local, and non-live.

- command run:
- visible windows / processes:
- local URLs opened:
- no hidden background process:
- no startup registration:
- no registry mutation:

## Boundary Review

Confirm explicitly:

- no live runtime:
- no provider call:
- no websocket / gateway / external fetch unless explicitly reviewed:
- no secrets used:
- no wallet:
- no trading / order routing / leverage:
- no memory write:
- no ledger write:
- no autonomous decision:
- no permission-to-act:

## Validation

- expected local surfaces visible:
- preflight passed or known limitation recorded:
- launch passed or known limitation recorded:
- logs reviewed:
- no boundary violation observed:

## Decision

Choose exactly one:

- PASS
- REPAIR_REQUIRED
- STOP_RISK

Selected value:

- DECISION:

## Shutdown / Reset

- manual shutdown steps:
- processes closed:
- local surfaces closed:
- residual risk:

## Final Handoff

- final observed state:
- unresolved risks:
- next recommended action:
