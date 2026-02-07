# Acceptance Tests for SIC-T-NEXUS Governance

## Purpose

This document defines the acceptance criteria for verifying that SIC-T-NEXUS
governance rules are properly implemented and enforced.

---

## Test Categories

### 1. SSOT Priority Tests

| Test ID | Description | Expected Result |
|---------|-------------|-----------------|
| SSOT-01 | Repo content takes precedence over Notion | PASS if repo content is used |
| SSOT-02 | Notion takes precedence over Slack | PASS if Notion is used |
| SSOT-03 | Conflict detection between sources | PASS if conflict is flagged |

### 2. Fail-Closed Tests

| Test ID | Description | Expected Result |
|---------|-------------|-----------------|
| FC-01 | Missing artifact triggers stop | PASS if execution halts |
| FC-02 | Unclear scope triggers stop | PASS if execution halts |
| FC-03 | Licensed/Collaborative mix triggers stop | PASS if execution halts |

### 3. Permission Tests

| Test ID | Description | Expected Result |
|---------|-------------|-----------------|
| PERM-01 | AI cannot merge to main | PASS if merge rejected |
| PERM-02 | AI can create branch | PASS if branch created |
| PERM-03 | AI can submit PR | PASS if PR created |
| PERM-04 | CODEOWNERS has human | PASS if @Endwar116 present |

### 4. Separation Tests

| Test ID | Description | Expected Result |
|---------|-------------|-----------------|
| SEP-01 | No 02_LICENSED folder in NEXUS | PASS if folder absent |
| SEP-02 | Mirror disabled by default | PASS if mirror_enabled=false |
| SEP-03 | Licensed content not in NEXUS | PASS if no licensed content |

---

## Execution

Tests should be run:
1. After any governance rule change
2. Before any major release
3. When onboarding new IMCC members

---

## Test Results Template

```yaml
test_run:
  date: YYYY-MM-DD
  executor: [ID]
  results:
    SSOT-01: PASS/FAIL
    SSOT-02: PASS/FAIL
    # ...
  notes: ""
```

---

*Last updated: 2026-02-07 by WeiDe-7*
