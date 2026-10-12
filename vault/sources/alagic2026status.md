---
id: alagic2026status
type: source
status: draft
tags: [nist, pqc, digital-signatures, additional-signatures, round-2]
cites: []
used_in: []
---

# Status Report on the Second Round of the Additional Digital Signature Schemes for the NIST PQC Standardization Process

- **Authors:** Gorjan Alagic, Maxime Bros, Pierre Ciadoux, Quynh Dang, Thinh Hung Dang, John Kelsey, Jacob Lichtinger, Yi-Kai Liu, Carl Miller, Dustin Moody, Rene Peralta, Ray Perlner, Angela Robinson, Hamilton Silberg, Daniel Smith-Tone, Noah Waller
- **Publisher:** NIST Internal Report (NIST IR) 8610, May 2026
- **DOI:** https://doi.org/10.6028/NIST.IR.8610
- **PDF:** https://nvlpubs.nist.gov/nistpubs/ir/2026/NIST.IR.8610.pdf
- **Project page:** https://www.nist.gov/pqcrypto

## Abstract (verbatim)

This report describes the evaluation criteria and selection process of the Second Round of the Additional Digital Signatures for the NIST Post-Quantum Cryptography (PQC) Standardization Process, which will identify public-key digital signature algorithms for potential standardization to protect sensitive information into the foreseeable future, including after the advent of quantum computers. Any signature scheme that is eventually selected will augment FIPS 204, Module-Lattice-Based Digital Signature Standard; FIPS 205, Stateless Hash-Based Digital Signature Standard; FIPS 186-5, Digital Signature Standard (DSS); and SP 800-208, Recommendation for Stateful Hash-Based Signature Schemes. Based on public feedback and internal reviews of the second-round candidates, NIST has selected nine candidate algorithms to move forward to the third round of evaluation: FAEST, HAWK, MAYO, MQOM, QR-UOV, SDitH, SNOVA, SQIsign, and UOV.

## Notes

- Third-round candidates as published: FAEST, HAWK, MAYO, MQOM, QR-UOV, SDitH, SNOVA, SQIsign, UOV.
- HAWK has since been withdrawn (post-dates this report): see [[straznickas2026hawk]].
- Selection priority: 1. security 2. cost/performance 3. then algorithm/implementation characteristics. Entry bar: lattice schemes need a large advantage over Dilithium and Falcon; non-lattice over SPHINCS+.
- 50 submissions, 40 first-round, 14 second-round (2024-10-24 to 2026-05-14), 9 third-round.
- Eliminated in round 2: CROSS, LESS, Mirath, PERK, RYDE.
- Third-round tweaks due 2026-08-14. Next NIST PQC conference planned H1 2027.
- No side-channel result in round 2 was decisive; constant-time, side-channel-resistant implementations expected to be a round-3 focus.
- Multivariate schemes (UOV, MAYO, SNOVA, QR-UOV): NIST expects a longer timeline, unlikely to standardize without a further round.

## NIST per-candidate assessments

- **FAEST:** AES-only assumptions, most confident of the MPCitH candidates. Risk: side-channel/fault attacks on masked implementation.
- **HAWK:** 555 B signatures at cat. 1 (smaller than Falcon and ML-DSA), integer-only arithmetic. Risk: smLIP/omSVP assumptions (see [[straznickas2026hawk]]).
- **MAYO:** small public keys. Wedge attack cost MAYO₂ ~30 bits at cat. 1; parameter selection risk.
- **MQOM:** best MPCitH performance, smallest total pk+sig. Risk: ROM/QROM proofs not yet mature.
- **QR-UOV:** pk 15-50% of UOV's, no parameter set broken, resists wedge attack (odd characteristic). Signing 15-20x faster than round 1. Risk: resampling hard to make constant-time.
- **SDitH:** conservative syndrome-decoding assumption. Risk: higher compute cost, complex design.
- **SNOVA:** very small keys and signatures. Risk: most parameter sets broken by wedge variant; "not a stable form", longer timeline.
- **SQIsign:** smallest pk+sig (148 B signature at cat. 1), signing ~20x and verification ~6x faster than round 1. Risk: slowest signing, hard to make constant-time, partial side-channel leakage.
- **UOV:** 96 B signatures at cat. 1, fast verification, but pk >200 KB expanded. Wedge and small-field attacks broke 3 of 4 parameter sets; NIST suggests odd characteristic.
- Relevance: Full candidate list.
