# Preliminary tooling inventory and package importance

Computed as of **2026-10-26** from the pinned local map.
[Evaluation methodology](https://github.com/deltadefi-protocol/devx-updates/blob/94e7860559fc2aeb55d921191b039f00cc3b14a5/content/reports/tooling-evidence/methodology.md) · [Scores](scores.csv)

302 inventory entries across 13 categories: **73 ranked** and
**229 unranked score ranges**. **25 review candidates**;
**0 status holds**. Counts are computed from the input identified below.

## Method and interpretation

Score = 100 × (0.6 × usage/100 + 0.1 × sqrt(stars)/sqrt(max stars) + 0.3 × degree/max degree).
Normalizers use the whole input map, each floored at one. Ranks are within category only.
Unknown inputs produce possibility ranges, not zero scores or ranks. Observed zero remains zero.
CSV scores have six decimal places; ranking uses unrounded values and the existing 1e-12 tie tolerance.
Candidates occupy the first ceil(25% × complete category cohort) positions, including ties,
with recorded usage above zero. Archived/abandoned candidates are held, without backfilling.
There are no manual additions, affiliation adjustments or funding recommendations.

All existing inventory entries are preserved. Added application identities have a separate category;
added tool identities retain unknown usage and stars and are not ranked without complete inputs.
Application transaction counts are not scoring inputs. Sourced application relationships now
contribute to graph degree, including qualified optional, test and historical connections.
Scores describe recorded map connectivity, not verified production reliance.

## Input provenance and limits

- Input: `cardano-graph.json`; SHA-256 `e4775d51bdeecee3fd23091816a7726b859e2c917229029c09221c4bd87368ee`.
- Map metadata generated: 2026-07-20; contacts generated: 2026-08-18.
- Survey attribution in map: State of the Developer Ecosystem 2025 (Cardano Foundation), n=109.
- Source dates vary by field; the computation date is not a fresh measurement of usage, stars or maintenance.
- Raw survey responses have not been independently audited in this run.
- Degree measures both ends of all recorded graph relationship types, not verified incoming adoption.
- Connectivity assumptions inherit unverified baseline links. Regenerate after any map-edge changes.
- Missing-input ranges are conditional on observed normalizers, not statistical confidence intervals.
- A candidate is a review prompt; an unranked or non-candidate tool is not a finding of low importance.

## Category summary

| Category | Entries | Ranked | Unranked | Candidates | Held |
| --- | --- | --- | --- | --- | --- |
| APIs & Providers | 15 | 6 | 9 | 2 | 0 |
| Applications | 18 | 0 | 18 | 0 | 0 |
| Dev Tools & Testing | 48 | 2 | 46 | 1 | 0 |
| Governance | 6 | 0 | 6 | 0 | 0 |
| Indexers & Data | 18 | 9 | 9 | 3 | 0 |
| Infrastructure & Integration | 21 | 6 | 15 | 2 | 0 |
| Layer 2 & Scaling | 11 | 2 | 9 | 1 | 0 |
| Nodes & RPC | 18 | 6 | 12 | 2 | 0 |
| Node Operations | 9 | 5 | 4 | 2 | 0 |
| Oracles & Data Feeds | 4 | 2 | 2 | 2 | 0 |
| Smart Contracts | 32 | 9 | 23 | 3 | 0 |
| SDKs & Libraries | 73 | 23 | 50 | 6 | 0 |
| Wallets & Connectivity | 29 | 3 | 26 | 1 | 0 |

## Review candidates

| Category | Rank | Tool | Score |
| --- | --- | --- | --- |
| APIs & Providers | 1 | Blockfrost (`blockfrost`) | 53.969231 |
| APIs & Providers | 2 | Blockfrost Backend (RYO) (`blockfrost-backend-ryo`) | 29.399031 |
| Dev Tools & Testing | 1 | Demeter (`demeter`) | 24.246154 |
| Indexers & Data | 1 | cardano-db-sync (`cardano-db-sync`) | 28.839727 |
| Indexers & Data | 2 | Kupo (`kupo`) | 22.461271 |
| Indexers & Data | 3 | Yaci Store (`yaci-store`) | 16.652821 |
| Infrastructure & Integration | 1 | Cexplorer (`cexplorer`) | 21.000000 |
| Infrastructure & Integration | 2 | Cardanoscan API (`cardanoscan-api`) | 18.000000 |
| Layer 2 & Scaling | 1 | Hydra (`hydra`) | 17.122112 |
| Nodes & RPC | 1 | cardano-cli (`cardano-cli`) | 49.915385 |
| Nodes & RPC | 2 | Ogmios (`ogmios`) | 35.730248 |
| Node Operations | 1 | cardano-signer (`cardano-signer`) | 10.911011 |
| Node Operations | 2 | cncli (`cncli`) | 6.303866 |
| Oracles & Data Feeds | 1 | Charli3 (`charli3`) | 3.000000 |
| Oracles & Data Feeds | 1 | Orcfax (`orcfax`) | 3.000000 |
| Smart Contracts | 1 | Aiken (`aiken`) | 67.564310 |
| Smart Contracts | 2 | OpShin (`opshin`) | 9.568211 |
| Smart Contracts | 3 | Scalus (`scalus`) | 8.749884 |
| SDKs & Libraries | 1 | MeshJS (Mesh SDK) (`meshjs-mesh-sdk`) | 32.027814 |
| SDKs & Libraries | 2 | Lucid Evolution (`lucid-evolution`) | 26.833479 |
| SDKs & Libraries | 3 | Lucid (`lucid`) | 26.472517 |
| SDKs & Libraries | 4 | cardano-js-sdk (`cardano-js-sdk`) | 22.604101 |
| SDKs & Libraries | 5 | cardano-serialization-lib (CSL) (`cardano-serialization-lib-csl`) | 22.225854 |
| SDKs & Libraries | 6 | cardano-multiplatform-lib (CML) (`cardano-multiplatform-lib-cml`) | 17.734499 |
| Wallets & Connectivity | 1 | cardano-hw-cli (`cardano-hw-cli`) | 11.448842 |

## Affiliated tools: numerical rationale for independent review

Delta Lab maintains Mesh, Whisky and Vodka. They receive the same transformations, weights,
category ranking and missing-data treatment as other entries, with no manual adjustment.
The numerical explanations below are reproducible; independent review remains pending.

### MeshJS (Mesh SDK)

Inputs from the dated map: usage 37%; stars 270; degree 9.
Known contributions: usage=22.200000 points, stars=2.904738 points, connectivity=6.923077 points.
Score range: 32.027814–32.027814. Rank 1 within SDKs & Libraries only.
Review state: candidate.

### whisky

Inputs from the dated map: usage unknown%; stars 16; degree 4.
Known contributions: usage=unknown points, stars=0.707107 points, connectivity=3.076923 points.
Score range: 3.784030–63.784030. Unranked because inputs are missing; unknown usage is not low usage.
Review state: unranked.

### Vodka

Inputs from the dated map: usage unknown%; stars 30; degree 1.
Known contributions: usage=unknown points, stars=0.968246 points, connectivity=0.769231 points.
Score range: 1.737477–61.737477. Unranked because inputs are missing; unknown usage is not low usage.
Review state: unranked.

Independent review of affiliated-tool rationale remains pending; these scores are not funding recommendations.
