## Decision

Use the exact SPDX expression AGPL-3.0-or-later for new UCAN-owned work, including reusable cores and non-code owned inputs. Preserve copyright attribution. The repository map and package-local grant distinguish current contributions from retained upstream material and historical grants.

## Implementation

Change current package declarations, current license text selection, license-policy.tsv, checker positive/negative expectations and current documentation. Keep a complete MPL text only for retained old grants or snapshots, explicitly described as historical rather than a new permissive offer. Existing license checker policy is the authority; do not add a second checking convention. Current accepted license-boundary requirements are superseded only in the narrow licensing domain after validation; archived decisions and legacy stores remain historical evidence.

The exact vendor/verified-logic snapshot, MPL metadata/notices and vendor/verified-logic-revision.txt remain unchanged. Do not run sync-verified-logic.sh or import uncommitted Trellis bytes. The no-std/std architecture remains unchanged.

## Validation and limits

Before product edits, pass Cairn proposal, design and tasks gates without modifying policy. During implementation run no builds, lint, tests, proof runs or broad validation. Final coordinated verification runs the existing license checker and packaging metadata checks, plus the exact-revision Josh snapshot checker. Record actual output before checking verification tasks or syncing/archiving. Licensing is not proof evidence and expands no correctness or release claim.
