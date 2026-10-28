# Application dependencies and tooling evidence

Prepared 27 October 2026; packaged for draft review on 28 October 2026.

This directory contains an evidence snapshot. It does not replace the site’s
`data/cardano-graph.json` or update the map viewer.

This collection extends the D1 map with sourced application relationships and
provides a volume-prioritised project review, qualitative analysis, preliminary
tooling scores and documented evidence gaps.

## Reports

| Report | What it provides |
| --- | --- |
| [Dependency analysis](dependency-analysis.md) | Findings on component stacks and shared integration boundaries |
| [Map change log](changelog.md) | Sourced changes against the pinned D1 baseline |
| [Projects by activity](projects-by-volume.md) | All 56 application rows, with desk research for the first twenty |
| [Application dependencies](application-tool-dependencies.md) | 57 qualified relationships across thirteen applications, with gaps for all twenty |
| [Package importance](package-importance-report.md) | 73 ranked entries, 229 incomplete-input ranges and 25 review candidates |
| [Repository evidence gaps](inconsistency-register.md) | 34 missing repository URLs and one dated 404 |

The extended [map](cardano-graph.json), assembled on 26 October, has 302 entries
and 304 links. It preserves the 269 baseline entries and 248 baseline links,
adds 33 identities and 56 links, and corrects 26 repository fields.

## Evidence and interpretation

The frozen [activity report](volume-source/README.md) was generated on 16 October
for 16 September–16 October 2026. Application counts prioritise the research;
they may overlap and are not assigned to tools. Source-package and documentation
observations checked on 22 October retain their component scope, dates and
prototype, testing, optional or historical qualifications.

The dependency table contains the source citations supporting the map extension.
The [baseline](baseline.md) and [repository observations](repository-observations.json)
identify the comparison input and dated repository checks. Unknown deployment stacks
remain unknown; inherited links are not validated by the newly sourced links.

The [scores](scores.csv) use the
[evaluation methodology](https://github.com/deltadefi-protocol/devx-updates/blob/94e7860559fc2aeb55d921191b039f00cc3b14a5/content/reports/tooling-evidence/methodology.md)
with 60/10/30 usage, stars and connectivity weights. Missing inputs produce ranges,
not zero scores. Review candidates are not funding recommendations.

Delta Lab maintains Mesh, Whisky and Vodka. They receive the same scoring and
missing-data treatment. Numerical explanations are included in the package-importance
report; independent review of the affiliated-tool rationale remains pending.

## Supporting data

- [Extended map](cardano-graph.json): the graph assessed in these reports.
- [Scores CSV](scores.csv): input values, contribution points, ranges and candidate states.
- [Frozen activity data](volume-source/tx-stats.json) and [provenance](volume-source/README.md).
- [Baseline reference](baseline.md): immutable upstream source and exact input hash.
- [Repository observations](repository-observations.json): twelve repository moves and one unavailable URL, checked on 20 October.
