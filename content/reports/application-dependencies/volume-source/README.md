# Frozen 30-day transaction report

Captured **2026-10-22 at 05:50 UTC**. Exact upstream bytes are in
[tx-stats.json](tx-stats.json); provenance is recorded below.

| Item | Value |
| --- | --- |
| Repository | `cardano-foundation/cardano-org` |
| Branch checked | `staging` |
| Source commit | `85eb8c314fab8af16f6318764750da45161ae8b9` |
| Source path | `src/data/tx-stats.json` |
| Last report-file commit | `84392cde9d7cafdbec443541d5686db186accad8` |
| SHA-256 | `12404c8359d78e2f0a9191b676739df2227fe4d561bdc0fb3a1ef0372ec92688` |
| Bytes | 16610 |
| Generated date in report | 2026-10-16 |
| Reporting start, verbatim | `2026-09-16T21:45:52` |
| Reporting end, verbatim | `2026-10-16T21:44:37` |
| Window | Six epochs, approximately 30 days |
| Chain epoch | 662 |
| Network transactions in report | 2,609,711 |
| Application rows | 56 |
| Metadata-label rows | 73 |

All figures above come from the captured report or capture procedure on 2026-10-22.
The reporting timestamps contain no timezone suffix; they are retained without conversion.

## Source and publication check

[Immutable report](https://github.com/cardano-foundation/cardano-org/blob/85eb8c314fab8af16f6318764750da45161ae8b9/src/data/tx-stats.json).
This is the report at the latest `staging` commit returned by GitHub when captured.
The file history endpoint identifies the last report-file commit shown above.
The [live leaderboard](https://cardano.org/apps/leaderboard/), checked 2026-10-22,
shows the same period, epoch, network total and top application count (1,724,962).
Those observations support the published-report match; the website's deployed commit
was not independently established. The report is a published snapshot, not real-time data.

## Use

Use application transaction counts to prioritise stack research. Keep `appStats`
separate from `metadataLabelStats`; registered metadata standards are not automatically
named applications. Preserve the report without reclassification or filtering.
Application totals may overlap; do not sum them as unique network coverage or infer
unattributed volume by subtracting their sum from the network total.
This capture does not rerun the underlying db-sync queries, establish SDK transaction
counts, verify stack dependencies or change the tooling scoring method.

Attribution details: [published methodology](https://cardano.org/docs/get-involved/tx-rankings/)
and [generator](https://github.com/cardano-foundation/tx-leaderboard-script).
