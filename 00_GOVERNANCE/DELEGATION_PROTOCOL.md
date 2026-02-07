# Delegation Protocol

## Purpose

This protocol defines how decisions are made when the Protocol Owner (Andwar) is unavailable.

## Availability Tiers

| Tier | Condition | Decision Scope |
|------|-----------|----------------|
| T0 | Andwar online | Full authority |
| T1 | Andwar offline < 24h | AI can proceed with documented decisions |
| T2 | Andwar offline 1-7 days | AI can proceed with minor changes, major changes queued |
| T3 | Andwar offline > 7 days | Fallback human required |

## Decision Classification

### Minor Decisions (AI can proceed at T1-T2)
- Documentation updates
- Log entries
- Changelog updates
- Non-breaking configuration

### Major Decisions (Require T0 or fallback human)
- Protocol changes
- Governance rule changes
- REGISTRY.json modifications
- Any changes to 00_GOVERNANCE/

## Fallback Human

If Andwar is unavailable for > 7 days:
1. Check if a fallback human is designated in REGISTRY.json
2. If no fallback, Fail-Closed on all major decisions
3. AI continues minor maintenance only

## Fail-Closed Requirements

When in doubt:
1. Do not proceed
2. Document the blocked decision in `04_CHANGELOG/DECISIONS/`
3. Wait for human confirmation

## Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-02-07 | WeiDe-7 | Initial version |
