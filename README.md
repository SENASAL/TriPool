<p align="center"><img src="logo.png" alt="TRIPOOL logo" width="140"></p>

# TriPool (TBL)

**Token-based program on MultiversX with monthly prize rounds, refunds, liquidity locking and staking.**

> ⚠️ **Status: design phase, undergoing a viability assessment.** The TBL token has been created. The program smart contracts and services described here are not deployed, audited or operational. The program will not launch in any jurisdiction until a written legal review is completed.

---

## Token

| | |
|---|---|
| Name | TriPool (TBL) |
| Identifier | `TBL-3468ae` |
| Chain | MultiversX |
| Decimals | 18 |
| Supply | 1,000,000,000 TBL |
| Owner | `erd1g568suxmlmw9znwddffnzvcrpw8t26sf9fpn8mu88vur4n06n5pqglt86m` |
| Market | SENASAL has not authorized any TBL sale or created liquidity pools. |

Always verify the token by its identifier. A token with the same name but a different ID is not ours.

---

## Proposed program design

The following are design requirements, not implemented or verified features.

- **Monthly rounds.** Participants join a round during its open period. Once the round closes, no one can buy or change entries.
- **Minimums.** A round only takes place if it reaches a minimum number of entries and a minimum number of distinct wallets. Otherwise it is cancelled.
- **Refunds.** Cancelled rounds are refunded automatically in batches, with a self-claim fallback if the service wallet fails.
- **Verifiable randomness.** A two-phase draw whose seed the caller cannot choose and that nobody can run twice.
- **Separated contracts.** Prize reserve, draw, vesting, exchange allocation, liquidity locking and staking are separate contracts. Permitted fund flows and protected-reserve restrictions must be explicitly documented and verified before implementation.
- **No owner withdrawal** from the contracts that hold the prize reserve and the locks.

The full technical specification is under legal and technical review and is not published yet.

---

## Roadmap

| Phase | What | Status |
|---|---|---|
| 1 | Reference model (executable specification) | ⏳ Completion not verified; source and validation evidence required |
| 2 | Scenario tests for every rule | ⏳ Pending |
| 3 | Property-based tests against global invariants | ⏳ Pending |
| 4 | Devnet: pair creation, real gas measurement | ⏳ Pending |
| 5 | Testnet: full-program simulation | ⏳ Pending |
| 6 | Independent security audit | ⏳ Pending |
| 7 | Mainnet deployment | ⏳ Only after audit and written approval |

---

## Security

- Contracts holding funds are planned to be **non-upgradeable**.
- Administrative actions (pause, pilot parameters) are planned behind a **multisig** account. A pause can stop new entries and new rounds, but never blocks refunds, prizes or withdrawals.
- The intended launch policy is to disable token properties that allow freezing, wiping or further minting, where technically possible. Current on-chain properties and the feasibility of permanently disabling them must be verified before launch.
- Found a vulnerability? Please read [SECURITY.md](./SECURITY.md) and report it privately.

---

## Legal notice

This project is under development. Nothing here is financial advice, an offer of securities, or an invitation to participate in a game of chance. Participation may be restricted or prohibited in your country. Crypto assets are volatile and you can lose all of your money.

---

## Contact

- 🌐 [senasal.com](https://senasal.com)
- Part of the [SENASAL](https://github.com/SENASAL) ecosystem
