---
title: Agent Handoff Format
version: v0
license: CC BY 4.0
---

<!--
SOURCE_PRS: #27 (asso_agent_handoff_contract)
CONSOLIDATION_TYPE: source unique #27
ANONYMIZATION_PASS: 5c.3 (P1 → [operator]/[stakeholder])
P4_MICROFILTER_PASS: 5c.3 (possessif_exposant + ref_meta_interne)
LICENSE: CC BY 4.0
EXTERNAL_ALIGNMENT_PASS: 5c.3.b (1B + 2A + 3A + 4B applied)
SOURCE_FILES: 04_agent_handoff_format__src.md
-->
# Agent Handoff Format v0

## Purpose

This contract defines the minimum handoff structure and status discipline required for agent work under ACE governance. It specifies what every handoff must contain, which decision values are allowed, and how incomplete or under-proven work must be classified.

## Mandatory AGENT HANDOFF Fields

Every final handoff must include all of the following fields:

- BRANCH:
- BASE_COMMIT:
- CURRENT_COMMIT_OR_UNCOMMITTED_STATE:
- INITIAL_STATUS:
- FINAL_STATUS:
- FILES_CREATED:
- FILES_MODIFIED:
- FILES_DELETED:
- COMMANDS_RUN:
- PASS_FAIL_BY_COMMAND:
- RAW_ERROR_IF_FAIL:
- DIFF_STAT:
- BOUNDARY_CHECK:
- RISK_FLAGS:
- DECISION_PROPOSED:
- NEXT_RECOMMENDED_ACTION:

## Allowed DECISION_PROPOSED Values

- REMOTE_COMMIT_READY
- PARTIAL_NEEDS_REPAIR
- STOP_RISK

## Meaning Of REMOTE_COMMIT_READY

REMOTE_COMMIT_READY is a bounded remote review readiness signal.

It never means merge, live, runtime permission, permission-to-act, local proof, CI proof, human approval, or implementation authority.

It only means a bounded remote artifact may be ready for review when explicitly supported by observed evidence.

REMOTE_COMMIT_READY never means:
- merge
- live
- runtime permission

REMOTE_COMMIT_READY is only appropriate when observed evidence supports the claimed readiness state. It is never a permission signal and never bypasses human review.

## Meaning Of PARTIAL_NEEDS_REPAIR

PARTIAL_NEEDS_REPAIR means useful work may exist, but the result is incomplete, under-proven, missing required checks, or still dependent on repair, review, or validation before stronger status claims are appropriate.

## Meaning Of STOP_RISK

STOP_RISK means the task must stop because required inputs, permissions, base state, repo access, or tooling conditions were unavailable or too uncertain to continue responsibly.

## Rules For Remote GitHub Write

A draft PR is accepted as a bounded artifact.

Remote write alone is not proof of correctness.

If local validation is missing, the result must be classified as PARTIAL_NEEDS_REPAIR.

If CI is missing, the result must be classified as PARTIAL_NEEDS_REPAIR.

There is no REMOTE_COMMIT_READY without observed CI or human local validation.

Remote GitHub write without observed local validation or observed CI remains under-proven.

## Rules For REPAIR / ADVANCE / STOP Next Prompts

### REPAIR

Use REPAIR when prior work exists but needs bounded correction, completion, or proof strengthening.

### ADVANCE

Use ADVANCE only for a newly and explicitly assigned future front after the current front is closed by the control tower.

### STOP

Use STOP when required repo state, permissions, tools, or evidence are missing and responsible continuation is not possible.

## Incomplete Handoff Classification

Any AGENT HANDOFF missing one or more mandatory fields is incomplete.

An incomplete handoff must be treated as under-proven.

An incomplete handoff cannot support REMOTE_COMMIT_READY.

## Memory Rule

Memory is continuity only.

Memory is not:
- proof
- canon
- git state
- validation
- permission
