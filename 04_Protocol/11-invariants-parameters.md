# 11. INVARIANTS AND PARAMETERS

This section gathers in a single place what cannot change and what can change, with its range.

## 11.1 Invariants

They cannot be modified by any governance mechanism or by contract upgrades. They are implemented so that their verification does not depend on upgradable code.

| | | |
| --- | --- | --- |
| | **Invariant** | **Section** |
| I-1 | The ZDAO `totalSupply` never exceeds 1,000,000,000 (`MAX_SUPPLY` of the ERC-20) | 2.1 |
| I-2 | Burning reduces `totalSupply` and returns minting capacity under `MAX_SUPPLY`; it does **not** replenish the staking reserve | 2.2 |
| I-3 | 500,000,000 ZDAO are reserved exclusively for the Official Staking System (`stakingMinted` capped at 500M) and only the staking contract can mint them | 2.3 and 6.3 |
| I-4 | The decreasing issuance curve (250/125/62.5/31.25M) is an absolute annual ceiling | 6.3 |
| I-5 | A Genesis allocation is consumed only once; the choice between ZDAO and ZREC resides in the off-chain registry, never in the token | 5.3 |
| I-6 | ZREC is a single fungible asset; restrictions live in the positions, never in the token | 3.2 |
| I-7 | No unit of energy can support more than one issuance or more than one certificate | 4.2 |
| I-8 | A batch in FINALIZED state cannot be reused | 4.6 |
| I-9 | No minting can be authorized on the basis of a non-reproducible criterion | 4.5 |
| I-10 | The DAO is the supreme authority; the Committee only exercises delegated competences | 8.1 |
| I-11 | The staking reward accrues linearly over time with a rate that halves each year (100% year 1, 50% year 2…) | 6.2 |

## 11.2 Configurable parameters

Modifiable by governance within the indicated ranges and subject to the timelock of Section 8.3.

| | | | |
| --- | --- | --- | --- |
| **Parameter** | **Initial value** | **Range** | **Section** |
| Energy Issuance split | 50% producer | 30% – 70% | 3.3 |
| Batch closure — time | 24 hours | configurable | 4.6 |
| Batch closure — energy | 1 MWh | configurable | 4.6 |
| Provisional window | 72 hours | configurable downward | 4.6 |
| Burn Execution Threshold | 10,000 ZDAO | configurable | 2.6 |
| ZERO DEX fee | 0.30% | 0.05% – 1.00% | 7.3 |
| Fee split | 40/30/20/10 | see table 7.3 | 7.3 |
| Committee mandate | 24 months | renewable | 8.1 |
| Staking immediate withdrawal fee | 2% | 0.50% – 5.00% | 6.6 |
| Withdrawal fee split | 40/40/20/0 | see Section 6.6 | 6.6 |
| Waiting period and window of the requested withdrawal | set by governance | with safety limits | 6.6 |
