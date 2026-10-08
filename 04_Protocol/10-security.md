# 10. SECURITY

## 10.1 Audit

All contracts must undergo an independent audit before going into production, expressly verifying the invariants of Section 11. Any relevant modification requires an additional audit prior to deployment.

## 10.2 Vectors considered

| | | |
| --- | --- | --- |
| **Vector** | **Measure** | **Section** |
| Repeated Claim after transferring ZDAO | The choice resides in the off-chain allocation, with single consumption | 5.3 |
| Duplication of the allocation using several wallets | Terminal state per allocation | 5.3 |
| Issuance of rewards above the reserve | The staking reserve keeps its own cumulative counter, which burning does not reduce | 2.2 |
| Circumvention of the Merits schedule | The lock lives in the position's withdrawal rules | 5.5 and 6.4 |
| Double minting by retrying a batch | Batch identifier in the uniqueness registry | 4.6 |
| Reuse of already processed production | Irreversible FINALIZED state | 4.6 |
| Double use of a certificate | Registered purpose and non-transferability | 3.6 |
| Inflated production declaration | Plausibility checks | 4.5 |
| Non-existent or oversized installation | Triple verification of nominal power | 4.5 |
| Discretionary authorization of minting | Merkle tree published before the Claim | 5.6 |
| Cumulative rounding deviation | Mandatory carry-over of residues | 4.6 |
| Accelerated depletion of the staking reserve | Decreasing maximum curve and 500M reserve as a ceiling | 6.3 |

## 10.3 Treasury and operational security

The DAO Treasury operates under a multisig scheme; no Committee member can dispose of the funds individually; every operation complies with the authorization rules and the timelock; all operations are recorded on-chain.

Operational measures: separation of responsibilities, permission control, permanent record of operations, cryptographic validation of critical actions, protection against replay attacks and duplicate executions, and continuous monitoring.

## 10.4 Continuous improvement

Governance may incorporate new audits, infrastructure improvements, improvements in permission management, new cryptographic mechanisms and incident response procedures.

**The protocol does not require oracles to post a collateral deposit.** A deposit does not prove that an energy datum is true: it only introduces an economic penalty if someone cheats. For ZERO Energy, the technical verification chain —installation, meter, measurement, period, validation, uniqueness— described in Section 4 is more decisive. Governance may in the future incorporate economic guarantee or penalty mechanisms for certain validators, without making them a requirement of the protocol now.
