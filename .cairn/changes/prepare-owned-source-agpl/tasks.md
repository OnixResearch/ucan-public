## Preparation

- [x] [serial] Pass proposal, design and tasks gates before product metadata changes. r[ucan.owned_agpl.preparation]

## Implementation

- [x] [serial] Align owned-source package metadata, complete grants, licensing map, policy and checker positive/negative expectations; preserve immutable imports, third-party notices, old source identities and prior grants. r[ucan.owned_agpl.consistency]
- [x] [serial] Update current documentation and prepare replacement license-boundary requirements in the change-local spec; leave accepted-spec sync to coordinated final evidence without migrating legacy lifecycle stores or changing Rust APIs/proof semantics. r[ucan.owned_agpl.boundaries]

## Coordinated final evidence

- [ ] [serial] Parent runs and captures the existing license checker, package metadata/archive checks and exact-revision vendor synchronization checker; no implementation-time proof/build/test runs. r[ucan.owned_agpl.validation]
- [ ] [serial] Reconcile actual evidence and accepted specs, then perform lifecycle sync/archive only if all required evidence exists. No verification or archive completion is claimed by source preparation. r[ucan.owned_agpl.validation]
