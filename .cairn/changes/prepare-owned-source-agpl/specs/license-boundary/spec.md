# UCAN License Boundary Specification

## Purpose

Describe prospective owned-source AGPL licensing while retaining the exact immutable MPL snapshot and earlier effective grants. This change supersedes the earlier core/shell licensing split without changing their architectural separation.

## MODIFIED Requirements

### Requirement: All new owned packages use AGPL

r[ucan.packaging.license_boundary.package_split] The root `ucan` shell, `ucan-core` and `ucan-nostr` MUST declare `AGPL-3.0-or-later` for new owned contributions. All other new owned source, contracts, schemas, fixtures/templates, documentation and policy MUST use that same prospective grant unless carrying a preserved third-party notice.

#### Scenario: A consumer selects only the no-std core

- GIVEN a consumer selects `ucan-core`
- WHEN current package metadata is inspected
- THEN it MUST report AGPL-3.0-or-later, without changing its no-std architecture.

### Requirement: Vendored Trellis preserves its recorded grant

r[ucan.packaging.license_boundary.trellis_snapshot] The immutable `vendor/verified-logic` snapshot at recorded Trellis revision `1f03111b92cc36aade07359c96773e086908c95f` MUST preserve its exact source bytes, MPL-2.0 metadata, notices and license artifacts. This prospective owner change MUST NOT refresh that snapshot or its revision.

#### Scenario: New Trellis working source changes license

- GIVEN Trellis prepares new owned source under AGPL
- WHEN UCAN source preparation is applied
- THEN the old snapshot MUST remain byte-for-byte aligned to its recorded committed revision under its original grant, not uncommitted Trellis bytes.

### Requirement: Complete artifacts and grant boundaries accompany source

r[ucan.packaging.license_boundary.artifacts] UCAN MUST ship complete AGPL-3.0-or-later terms for owned packages, complete MPL-2.0 terms for the retained snapshot/earlier grants, and an explicit package/vendor map. A retained historical text MUST NOT offer MPL for new owned contributions.

#### Scenario: A recipient reviews source offline

- GIVEN a recipient receives UCAN packages and the snapshot
- WHEN license artifacts are inspected
- THEN complete applicable terms and the package/historical-grant boundaries MUST be available without fetching.

### Requirement: Documentation keeps grants and proof claims bounded

r[ucan.packaging.license_boundary.documentation] Documentation MUST state that earlier effective grants including byte-identical material remain valid, contributor authority and third-party terms remain necessary, and licensing/source alignment does not expand Rust API, proof, interoperability, release or shell-correctness claims.

#### Scenario: Previously granted bytes are unchanged

- GIVEN content was already effectively granted under earlier terms
- WHEN the new prospective policy is prepared
- THEN that content MUST remain usable under its earlier effective grant.

### Requirement: License validation rejects owned-source drift

r[ucan.packaging.license_boundary.validation] The existing license checker MUST accept AGPL owned-package metadata plus the immutable MPL snapshot, and MUST reject stale MPL owned-package declarations or missing applicable complete texts.

#### Scenario: The core still declares MPL

- GIVEN the current owned core manifest declares MPL-2.0
- WHEN focused licensing validation runs
- THEN validation MUST fail while accepting the old snapshot's original MPL declaration.

### Requirement: Focused evidence precedes lifecycle closeout

r[ucan.packaging.license_boundary.final_validation] Coordinated final validation MUST capture current package metadata, complete artifacts, documentation, exact-revision snapshot identity and Cairn conformance before accepted-spec sync or archival is claimed.

#### Scenario: Source preparation exists without final outputs

- GIVEN only source preparation and preimplementation gate results exist
- WHEN handing off to coordinated verification
- THEN validation tasks MUST remain unchecked and the change MUST remain active.
