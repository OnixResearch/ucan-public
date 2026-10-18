# UCAN licensing boundary

| Package or surface | License |
|---|---|
| New owned `crates/ucan-core/**` source | `AGPL-3.0-or-later` |
| `crates/ucan-nostr/**` | `AGPL-3.0-or-later` |
| Root `ucan` std shell | `AGPL-3.0-or-later` |
| `vendor/verified-logic/**` | `MPL-2.0`, synchronized from the committed Trellis revision in `vendor/verified-logic-revision.txt` |
| All other new UCAN-owned source, contracts, schemas, owned fixtures/templates, documentation and policy | `AGPL-3.0-or-later` |
| Other dependencies and generated material containing upstream code | Their stated upstream terms |

The no-std core must not depend on the std shell. The shell may depend on the core and the verified primitive snapshot. The optional `peer-auth` feature uses `blake3`, `hmac`, `sha2`, and `zeroize` under their upstream terms. It copies no Celld code. The snapshot must be refreshed with `scripts/sync-verified-logic.sh`, not manually reformatted or edited.

Complete texts are in `LICENSES/MPL-2.0.txt` and `LICENSES/AGPL-3.0-or-later.txt`. The core and Nostr adapter carry the complete AGPL text; the synchronized snapshot carries its original complete MPL text, so package archives are self-contained. The retained MPL text documents the immutable snapshot and earlier grants, not an MPL offer for new owned contributions.

The current immutable snapshot is Trellis revision `1f03111b92cc36aade07359c96773e086908c95f`. Its source bytes, MPL metadata/notices and recorded revision remain unchanged by this prospective preparation. New Trellis-owned source terms do not retroactively change this snapshot or old Git pins. A future refresh requires a separate committed-source import and license review; do not copy uncommitted Trellis working bytes into it.

New owned contributions are offered only under AGPL-3.0-or-later. Contributors must have the authority to make that grant and preserve existing copyright attribution and third-party notices. Earlier effective grants are not revoked. Byte-identical material remains usable under its earlier effective grant; this change cannot make previously granted copies AGPL-only.

Trellis source/proof alignment does not certify UCAN parsing, cryptography, resolver truth, revocation freshness, replay storage, policy semantics, interoperability, or shell correctness. This source preparation changes no Rust APIs or proof semantics and authorizes no publication. This map does not establish contributor authority or legal compliance.
