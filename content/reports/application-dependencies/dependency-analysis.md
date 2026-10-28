# Application dependency analysis

Analysis dated **2026-10-26**. This analysis synthesises public-source desk
observations checked **2026-10-22**; it does not refresh those sources or establish
current deployment configurations. Source identifiers below link to the dated,
qualified records in the [application dependency table](application-tool-dependencies.md).

## Evidence and scope

The desk review examined the first twenty applications in the
[frozen transaction-activity ranking](projects-by-volume.md). It recorded 57
component-to-tool relationships across thirteen applications; seven had no concrete
tool relationship established. All twenty retain gaps. These are observations of
published source packages, documentation and examples, rather than thirteen verified
production stacks. The dependency table includes the dated source citations and individual evidence qualifications.

The activity source covers 16 September–16 October 2026, while the desk checks were
performed on 22 October. A repository snapshot can postdate the activity being
prioritised. Application counts may overlap, and cannot be assigned to a tool merely
because one application component declares that tool. The ranking and its provenance
document the source window and attribution limits.

## Applications combine several distinct dependency layers

**Observation.** The reviewed packages separate validator code, transaction-building
libraries, data access and testing. Minswap's V2 contracts identify Aiken, while its
published SDK declares Lucid, Blockfrost, Maestro and Ogmios packages. WingRiders'
Rapid contracts identify Aiken and its Rapid SDK declares Mesh. SundaeSwap's V3+
contracts identify Aiken while its core SDK declares Blaze.
Sources checked 2026-10-22:
[Minswap S002–S005](application-tool-dependencies.md#source-s002),
[WingRiders S011–S012](application-tool-dependencies.md#source-s011),
[SundaeSwap S015–S017](application-tool-dependencies.md#source-s015).

**Interpretation.** A single application-to-language or application-to-SDK label
hides useful distinctions. Contract compilation, transaction construction and chain
queries expose different dependency boundaries. A tool change could affect one
component without establishing an application-wide migration. The map should be
read with the component and relationship qualifications attached to each edge.

MuesliSwap illustrates this distinction within one project: the inspected
concentrated-pool package declares Plutus Tx, while its orderbook package identifies
OpShin and declares PyCardano and an Ogmios Python client. Splash's inspected
packages include Plutarch and Aiken validators, CML-based builders, a CML fork in a
Rust agent, and Pallas networking in a chain-sync component. These observations
support mixed component stacks; they do not resolve which versions account for
the reported application activity. Sources checked 2026-10-22:
[MuesliSwap S048–S050](application-tool-dependencies.md#source-s048),
[Splash S020–S024](application-tool-dependencies.md#source-s020).

## Shared tools create common integration boundaries

**Observation.** Aiken appears in the inspected Minswap V2, WingRiders Rapid,
SundaeSwap V3+, Splash V3 and Masumi payment V2 manifests. CSWAP separately documents
an Aiken claim with an unverified deployment/source match. The SDK evidence is more
varied: it includes Lucid, Mesh, Blaze, Evolution SDK, Cardano Client Lib and
PyCardano in different components. Sources checked 2026-10-22:
[S002](application-tool-dependencies.md#source-s002),
[S011](application-tool-dependencies.md#source-s011),
[S016–S017](application-tool-dependencies.md#source-s016),
[S021](application-tool-dependencies.md#source-s021),
[S026](application-tool-dependencies.md#source-s026),
[S044–S046](application-tool-dependencies.md#source-s044),
and the manifest relationships in the dependency table.

**Interpretation.** Repeated dependencies identify places where compatibility
changes could require coordination across several source packages. They do not
establish market share, a common deployed version, vulnerability or a single point
of failure. The variation in off-chain libraries also means that shared validator
tooling does not imply a shared transaction-building stack.

Data access is another recurring boundary. Minswap declares multiple provider
clients; Dano's CLMM documentation shows a Kupo/Ogmios example; UVerify's Java
backend declares Cardano Client Lib and Yaci Store alongside Blockfrost, Koios and
Ogmios integration packages. Available integrations establish implementation
options, while active production endpoints remain unknown. Sources checked
2026-10-22: [S004–S005](application-tool-dependencies.md#source-s004),
[S009–S010](application-tool-dependencies.md#source-s009),
[S040–S041](application-tool-dependencies.md#source-s040).

**Interpretation.** Provider interfaces are plausible compatibility and substitution
boundaries. Multiple adapters alone do not demonstrate operational redundancy,
tested failover or the ability to switch providers without application changes.

## Testing and historical evidence need separate treatment

**Observation.** Splash declares Lucid Evolution in a testing package; UVerify's
examples declare Mesh in sandbox bootstrap code; SundaeSwap documents Lucid in
benchmark scaffolding. Liqwid publishes Plutarch testing utilities. These records
show development-tool relationships without establishing production transaction
builders. Sources checked 2026-10-22:
[S025](application-tool-dependencies.md#source-s025),
[S043](application-tool-dependencies.md#source-s043),
[S015](application-tool-dependencies.md#source-s015),
[S036](application-tool-dependencies.md#source-s036).

Historical and prototype sources have narrower reach. Hosky's inspected source
describes a claim prototype invoking cardano-cli. Spectrum's inspected packages
provide historical Plutarch and Haskell SDK evidence. Wayup's Anvil integration
record relies on indexed documentation whose direct URL returned 404. None
establishes a current complete stack. Sources checked 2026-10-22:
[S001](application-tool-dependencies.md#source-s001),
[S030–S031](application-tool-dependencies.md#source-s030),
[S034](application-tool-dependencies.md#source-s034).

**Interpretation.** Combining all these relationships into an unqualified edge
count would overstate production adoption. The extended map retains evidence
qualifications, but graph degree still counts recorded relationships of different
strengths. The [preliminary package-importance report](package-importance-report.md)
therefore describes connectivity in the recorded map, including optional, test and
historical relationships; it does not measure verified production reliance.

## What the evidence leaves unresolved

As of the 2026-10-22 desk checks, no concrete tool relationship was established for
5am.earth, Midnight's Cardano distribution activity, FMS by Trivolve, Indianchain by
Trivolve, VyFinance, Shadowbook or Indigo. The
[application gaps table](application-tool-dependencies.md#gaps-across-the-researched-applications)
records the inspected sources and individual limitations. Missing evidence is not
evidence of no dependencies, and this desk review does not classify teams as
non-responsive.

Even where package relationships are established, deployment versions, production
provider configuration and component-level transaction attribution frequently
remain unknown. Masumi's inspected snapshot, dated 21 October, explicitly postdates
the activity window. Dano's manifest/README version mismatch remains unresolved.
Sources checked 2026-10-22:
[S044–S047](application-tool-dependencies.md#source-s044),
[S009–S010](application-tool-dependencies.md#source-s009).

The extension also preserves baseline links whose claim-level evidence has not
been independently verified. New sourced observations should not be read as
validation of every inherited edge. Source boundaries are recorded in the
[map changelog](changelog.md), assembled 2026-10-26. In our interpretation, the
strongest finding is the existence of shared, component-specific integration
boundaries; the evidence does not yet quantify their production exposure or
ecosystem-wide criticality.
