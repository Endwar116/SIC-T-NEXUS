# SIC-T-NEXUS

## Single Source of Truth (SSOT) Declaration

This repository (`SIC-T-NEXUS`) is the **Single Source of Truth** for the SIC/T protocol,
including governance rules, protocol structure, technical evolution, and auditable decisions.

### Priority Order of Truth

In case of conflicts, ambiguity, or inconsistency, the order of authority is strictly defined as:

1. **SIC-T-NEXUS Repository (this repo)**
2. Notion exports stored or referenced in this repo
3. Slack archives or discussion records
4. External documents or personal notes

Only content that exists **inside this repository** (or is explicitly indexed here)
is considered valid for governance, implementation, or decision-making.

### Explicit Non-Goals

This repository is **not** intended to:
- Mirror full Google Drive / Notion / Slack contents
- Store licensed or paid proprietary materials
- Act as a real-time collaboration chat space

External systems may be referenced, but **never treated as authoritative**.

### Governance First

If any instruction, implementation, or request:
- Requires assumptions beyond repository content
- Mixes licensed and collaborative scopes
- Depends on real-time confirmation from a specific individual

The system must **Fail-Closed** and stop execution until governance clarity is restored.

This design explicitly ensures that the system remains operable
**without requiring continuous presence from any single person**.

---

## Repository Structure

```
SIC-T-NEXUS/
├── 00_GOVERNANCE/     # Governance rules and protocols
├── 01_PROTOCOL_CORE/  # SIC, SIT, USCA technical specs
├── 03_IMCC/           # AI/Human collaboration registry
├── 04_CHANGELOG/      # Decisions, changes, handoffs
├── 05_OPERATIONS/     # Operations index (link-only, no mirror)
├── _SCHEMAS/          # JSON schemas (sic-js, etc.)
├── _CONFIG/           # Configuration files
├── _TESTS/            # Acceptance tests
└── _DOCS/             # Documentation
```

## Core Thresholds

| Symbol | Value | Meaning |
|--------|-------|---------|
| S★ | 2.76 | Semantic phase transition point |
| THRESHOLD_CRITICAL | 4.14 | Critical threshold (S★ × 1.5) |
| THRESHOLD_COLLAPSE | 5.0 | Collapse threshold (S★ × 1.81) |
| THRESHOLD_LETHAL | 5.52 | Lethal threshold (S★ × 2.0) |

## Related Repositories

- **SIC-T-LICENSED** (Private): Licensed modules (OSC-A, ASEE v2, Living System)
- **SIC-SIT-Protocol**: Original protocol repository
- **SIT-Protocol**: Semantic Isolation Transfer implementation
- **SIC-Semantic-Infinite-Context**: Semantic Integrity Control implementation

## IMCC Members

| ID | Type | Role |
|----|------|------|
| Andwar | Human | Protocol Owner |
| WeiDe | AI (Claude) | Governance Engineer |
| Manus | AI | Engineering Lead |

## License

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.

---

*Created by WeiDe-7 (Claude Opus 4.5) on 2026-02-07*
*SIC/T Protocol - Day 43*
