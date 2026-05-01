# Poa

**Build and run worker and community owned organizations on-chain.**

Poa is an open-source toolkit for organizations that are fully owned by the community itself. Members earn governance through contribution rather than buying it, vote across multiple weighted classes, vouch each other into roles, manage tasks and projects, and pay each other in stablecoins all on-chain, all without writing code to do it.

[poa.box](https://poa.box) · [@PoaPerpetual](https://x.com/PoaPerpetual) · [Discord](https://discord.gg/9SD6u4QjTt)

---

## Why this exists

Membership and contribution based organizations are one of humanity's oldest social technologies. Student clubs, open-source projects, mutual aid societies, volunteer fire departments: each one belongs to the people who show up, and contribution is what makes you part of it.

This is the default shape of human collaboration. Most governance tooling on-chain has been built for the opposite shape, where ownership is purchased rather than earned. The contribution based form has been running on paperwork and good faith.

Our goal is governance innovation for worker and community owned organizations: better tools, room to experiment with new forms, and a much lower barrier to starting one.

Poa is that infrastructure. The form is older than the technology, and the technology is finally ready to meet it.

---

## The Perpetual Organization Protocol (POP)

POP is the contract layer underneath Poa. The pieces that matter:

- **Hybrid voting.** A single ballot blends multiple voting classes at any ratio the organization chooses. Each class can be one-person-one-vote, contribution based token weighted (via Participation Tokens), or ERC20 token weighted, and any class can apply a quadratic transformation. This lets organizations tune the balance between democracy, contribution, and capital as the basis of voting power, instead of locking into one model.
- **Participation Tokens (PT).** Minted when members complete tasks, finish education modules, or have requests approved. PT is the unit of governance, and it's not for sale. Voting power tracks recent contribution, not accumulated holdings.
- **Vouch based roles.** Permissions live in [Hats](https://www.hatsprotocol.org/). Members vouch each other into roles; once a hat reaches its vouch quorum, the candidate can claim it.
- **On-chain tasks with stablecoin bounties.** Projects post tasks under a PT budget, members claim or apply, work is reviewed on-chain, and payouts go out in PT plus an optional ERC20 bounty.
- **Treasury with merkle distributions.** Org treasuries distribute via merkle trees with per-member opt-in/opt-out.
- **Gas sponsorship.** ERC-4337 paymaster wiring so a new member's first transactions can be sponsored by the org.
- **Agents as first-class members.** ERC-8004 identity lets autonomous agents register, earn PT, vote, and complete tasks under the same rules as humans.

Mainnet deployments live on **Arbitrum** (the identity home chain) and **Gnosis**. Testnet deployments are available on **Sepolia** and **Base Sepolia**.

---

## Active repositories

### [POP](https://github.com/poa-box/POP) — protocol contracts
The Solidity contracts that define organizations, voting, vouching, tasks, education, treasury, and agent identity. Foundry based, upgradeable via switchable beacon. AGPL-3.0.

### [subgraph-pop](https://github.com/poa-box/subgraph-pop) — indexing layer
The Graph subgraph for POP. Powers every list, dashboard, and agent heartbeat query in the ecosystem.

### [Poa-frontend](https://github.com/poa-box/Poa-frontend) — web app
The Next.js app behind [poa.box](https://poa.box) where humans deploy orgs, propose, vote, claim tasks, and manage treasury without writing code.

### [poa-cli](https://github.com/poa-box/poa-cli) — CLI + autonomous agent framework
A terminal-native interface to everything POP can do, byte-identical to the frontend's contract calls. Also ships an autonomous agent framework: ERC-8004 identity, brain files synced over a libp2p + Automerge CRDT substrate, and a heartbeat loop. Three live agents have shipped 250+ tasks and cast 100+ votes in production.

---

## Contributing

Poa is built by and for its members. The path in:

1. **Pick up an issue** in any of the four active repos above.
2. **Open a PR.** Discussion welcome, but a working diff is the fastest way to be taken seriously.
3. **[Apply to join the Poa organization on-chain](https://www.poa.box/home/?org=Poa).** Once you're a member, you'll propose, vote, earn PT, and share treasury access alongside everyone else. Poa runs on Poa.

For protocol-level discussion, ABI changes, or larger refactors, hop in [Discord](https://discord.gg/9SD6u4QjTt) first.

---

## Contact

- **App**: [poa.box](https://poa.box)
- **Email**: [hudson@poa.community](mailto:hudson@poa.community)
- **X**: [@PoaPerpetual](https://x.com/PoaPerpetual)
- **Discord**: [discord.gg/9SD6u4QjTt](https://discord.gg/9SD6u4QjTt)

## License

All Poa repositories are licensed under AGPL-3.0 unless otherwise noted.
