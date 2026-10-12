# Minecraft World Storage Audit

Inventory and trend world-storage usage so operators can plan disk capacity and investigate unexpected growth. Avoid deleting region files as a cleanup shortcut: they contain world data and may cause irreversible loss.

## Audit workflow
1. Record filesystem capacity, free space, and mount health.
2. Measure world directory and region-file counts by dimension on a consistent snapshot or stopped server.
3. Compare with prior measurements and correlate growth with player activity, exploration, or scheduled generation.
4. Alert on remaining disk headroom and forecast time to exhaustion using observed growth rates.
5. Before any cleanup or migration, make and verify a separate backup and test on a copy.

Keep world paths and host identifiers private where they reveal infrastructure details.

## Files
- `storage-audit.csv`: measurement worksheet.
- `runbook/disk-pressure.md`: safe first response to disk pressure.