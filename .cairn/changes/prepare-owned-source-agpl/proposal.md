## Why

The operator explicitly selected AGPL-3.0-or-later for all owned code. UCAN's current MPL grant for ucan-core must not describe new owned contributions. Prior grants cannot be revoked. This is local source preparation, not publication.

## What Changes

- Apply AGPL-3.0-or-later prospectively to all UCAN-owned source including ucan-core, the root shell, optional adapters, contracts, schemas, owned fixtures, templates, documentation and policy.
- Align manifests, complete package-local texts, license-policy.tsv, source license checks and current licensing/contribution documentation.
- Preserve immutable imports, historical receipts and grants, existing third-party attribution and exact source identities. Keep vendor/verified-logic and its recorded Trellis revision byte-for-byte unchanged under MPL-2.0.
- Preserve every exported Rust API, executable algorithm and proof semantic boundary.

## Impact

No dependency or consumer lock update, vendor refresh, proof promotion, lifecycle migration, public distribution, remote operation, or registry publication. Byte-identical earlier material remains usable under its earlier effective grant. New owned contributions are not offered under MPL.
