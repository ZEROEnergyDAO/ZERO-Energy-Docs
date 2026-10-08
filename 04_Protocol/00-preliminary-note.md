# ZERO ENERGY — PROTOCOL TECHNICAL SPECIFICATION

**Version 1.0**

## PRELIMINARY NOTE

This document is the functional specification of the ZERO Energy protocol and the single reference source for three audiences: the community that participates in the ecosystem, the team that develops the protocol, and the auditors who verify it. It describes how the protocol works through rules, flows and equations.

Three reading rules:

* Where the document describes a limit, that limit is a mandatory rule of the protocol, not an intention.
* The **invariants** cannot be modified by any mechanism. The **parameters** may be configured by governance within the indicated ranges. Section 11 gathers them in two tables: invariants (11.1) and parameters (11.2).
* The evolution of the protocol is decided by the DAO through voting, as the ecosystem grows.

**Nomenclature.** The assets are identified as **ZERO DAO (ZDAO)** and **ZERO REC (ZREC)**. After the first mention in each section, the tickers are used. Formulas, tables, diagrams and contract specifications always use ZDAO and ZREC.

**TOKEN ZERO** is the Presale denomination. A TOKEN ZERO is a **future minting right**: it is neither a minted token nor a third on-chain asset. That right is exercised at the Claim, where it is resolved into ZDAO or ZREC at the participant's choice (Section 5).

**Reference version.** This English version is the reference version of the specification, published in the protocol's official repository. The Spanish and Portuguese versions are translations provided for ease of reading; in case of discrepancy, this English version prevails.

**Extensions.** Anything incorporated into the protocol after this version will be added as a separate, dated annex, without modifying the body of the document.

## INDEX

| | | |
| --- | --- | --- |
| **Section** | **Content** | **File (repository)** |
| 1 | General architecture | `01-general-architecture.md` |
| 2 | ZERO DAO (ZDAO) | `02-zero-dao.md` |
| 3 | ZERO REC (ZREC) | `03-zero-rec.md` |
| 4 | Proof of Energy and Energy Oracles | `04-proof-of-energy.md` |
| 5 | Genesis Phase: Presale, TGE and Claim | `05-genesis-phase.md` |
| 6 | Official Staking System | `06-staking.md` |
| 7 | ZERO DEX | `07-zero-dex.md` |
| 8 | Governance and progressive decentralization | `08-governance.md` |
| 9 | Contract architecture | `09-contract-architecture.md` |
| 10 | Security | `10-security.md` |
| 11 | Invariants and parameters | `11-invariants-parameters.md` |
| 12 | General provisions | `12-general-provisions.md` |

> **Note.** This index refers to the files of the official ZERO Energy repository on GitHub, where each section of the document is published separately, in English (reference version), together with the complete document in Spanish, English and Portuguese: https://github.com/ZEROEnergyDAO/ZERO-Energy-Docs/tree/main/04_Protocol
