# Contributing to SIC-T-NEXUS

## Contribution Rules

### For All Contributors

1. **Branch First**: Never commit directly to `main`
2. **PR Required**: All changes must go through Pull Request
3. **Scope Awareness**: Stay within your authorized scope

### For AI Contributors

AI contributors (WeiDe, Manus, etc.) have the following permissions:

| Action | Allowed |
|--------|---------|
| Create branch | ✅ Yes |
| Submit PR | ✅ Yes |
| Review PR | ✅ Yes |
| Merge to main | ❌ No |
| Direct push to main | ❌ No |

### Commit Message Format

```
[TYPE:CONTRIBUTOR] scope: description

Examples:
[AI:WeiDe] governance: add delegation protocol
[HUMAN:Andwar] protocol: update S★ threshold
```

### Fail-Closed Principle

If you encounter:
- Unclear scope
- Missing governance rules
- Licensed/Collaborative boundary ambiguity

**STOP** and report using sic-js format. Do not proceed with assumptions.

## Code Review Process

1. AI can review and comment
2. Only @Endwar116 (or delegated human) can approve and merge
3. See `00_GOVERNANCE/DELEGATION_PROTOCOL.md` for fallback rules

## Questions?

Open an issue or contact @Endwar116.
