# UCAN owned-source AGPL preparation

## ADDED Requirements

### Requirement: Preimplementation approval
r[ucan.owned_agpl.preparation]

Product metadata changes MUST follow passing proposal, design and tasks gates without policy weakening.

#### Scenario: A gate blocks
- GIVEN a required gate fails
- WHEN source preparation proceeds
- THEN product edits MUST wait and the missing prerequisite MUST be reported.

### Requirement: Prospective owned-source consistency
r[ucan.owned_agpl.consistency]

All new UCAN-owned source, including reusable cores, contracts, schemas, owned fixtures/templates/docs/policy, MUST be offered under AGPL-3.0-or-later with complete text and aligned manifests, maps and checkers.

#### Scenario: A package retains MPL metadata
- GIVEN an owned current package declares MPL-2.0
- WHEN the licensing check runs
- THEN it MUST reject that declaration.

### Requirement: Earlier grants and proof boundaries survive
r[ucan.owned_agpl.boundaries]

Earlier effective grants including byte-identical material MUST remain valid; immutable snapshots, historical receipts/source identities and third-party notices MUST remain unchanged. Public Rust APIs and proof semantics MUST remain unchanged; licensing MUST NOT expand proof claims or authorize publication.

#### Scenario: A consumer retains an old snapshot
- GIVEN a consumer retains a recorded MPL Trellis snapshot
- WHEN this prospective owner change is prepared
- THEN the old snapshot and its original notices/grant MUST remain intact.

### Requirement: Evidence precedes closeout
r[ucan.owned_agpl.validation]

The existing focused licensing and packaging checks and repository-required final gates MUST have captured evidence before validation completion, accepted-spec sync or archival is claimed.

#### Scenario: Only source preparation exists
- GIVEN no coordinated final check output exists
- WHEN handing off
- THEN verification tasks MUST remain unchecked and the lifecycle change MUST remain active.
