# Archive Policy

## Changelog Compression

To prevent changelog explosion:

1. **Monthly Archive**: At month end, compress daily logs into monthly summary
2. **Quarterly Archive**: At quarter end, move monthly archives to `ARCHIVE/`
3. **Keep Active**: Only last 3 months of detailed logs in main CHANGELOG.md

## Decision Records

- Keep all DECISIONS/*.md permanently
- Never delete decision records
- Archive format: `YYYY-MM-DD_decision-title.md`

## Handoff Logs

- Location: `04_CHANGELOG/HANDOFFS/`
- Format: `YYYY-MM-DD_INSTANCE_handoff.sic-js`
- Retention: Permanent (critical for AI continuity)

## Archive Location

Old records move to: SIC-T-ARCHIVE repository (when created)
