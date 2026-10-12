---
id: straznickas2026hawk
type: source
status: draft
tags: [pqc, digital-signatures, hawk, cryptanalysis, round-3]
cites: []
used_in: []
---

# HAWK-n Key Recovery Reduces to SVP in Dimension n/2 + 1

- **Authors:** Zygimantas Straznickas, Stephen A. Weis (Anthropic)
- **Publisher:** IACR ePrint 2026/1593 (not peer-reviewed), received 2026-08-03
- **URL:** https://eprint.iacr.org/2026/1593

## Notes

- Deterministic, polynomial-time reduction of HAWK-n key recovery to polynomially many exact SVP calls in dimension n/2+1, via a nontrivial automorphism of the key lattice.
- Claimed cost drop: HAWK-512 2^150 to 2^108; HAWK-1024 2^288 to 2^182. HAWK-256 key recovered in a few hours.
- Authors state it does not apply to Falcon.
- HAWK later withdrawn from NIST's process by its team (see [NIST Round 3 page](https://csrc.nist.gov/projects/pqc-dig-sig/round-3-additional-signatures), 2026-10-12).
- Relevance: HAWK is excluded from round 3.
