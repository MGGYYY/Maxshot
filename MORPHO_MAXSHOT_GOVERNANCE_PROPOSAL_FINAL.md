# MIP: Maxshot - Omni-Chain AI-Driven Curator for Morpho

## Summary

Maxshot is an autonomous, AI-driven curator that enables users to deposit into Morpho vaults and earn the best risk-adjusted yields across multiple blockchains. This proposal introduces Maxshot to the Morpho community and requests curator whitelisting to enable Maxshot vaults to be displayed on the Morpho UI. Maxshot's three core differentiators—omni-chain capital routing, agent-driven autonomous execution, and separation of strategy, risk, and execution—position it as a complementary curator that expands Morpho's value proposition to users seeking global capital efficiency.

---

## Motivation

Morpho's peer-to-peer lending protocol has established itself as a leading transparent, efficient lending market with minimal intermediation. However, Morpho users face a fundamental challenge: yield opportunities are fragmented across multiple blockchains, each with different market conditions, gas costs, and liquidity dynamics. Users must either choose a single chain and accept suboptimal yields, or manually manage complex cross-chain strategies—a task that requires constant monitoring and rebalancing.

Maxshot addresses this challenge by deploying autonomous agents that continuously discover and allocate capital to the highest-yielding opportunities across Ethereum, Arbitrum, Optimism, Base, and Plasma—all while maintaining strict, machine-enforced risk budgets. By whitelisting Maxshot as a curator, Morpho gains access to an omni-chain yield optimization solution that complements existing curators and expands the protocol's value proposition to users seeking global capital efficiency without manual intervention.

---

## What is Maxshot?

Maxshot is an **AI-native financial infrastructure** that transforms static DeFi vaults into continuously learning, adaptive systems. Unlike traditional curators that rely on manual management or static strategies, Maxshot deploys autonomous agents that operate 24/7 to optimize yield, manage risk, and execute across multiple blockchains simultaneously.

### Core Architecture

Maxshot's architecture is built on three distinct layers, each with clear responsibilities and enforcement mechanisms:

**Strategy Layer:** Autonomous AI agents continuously monitor market data (yield curves, liquidity depth, volatility, correlation) across all supported chains. These agents identify yield opportunities, evaluate them against predefined risk budgets, and execute capital allocation decisions in real-time. All decisions are logged on-chain for full transparency and auditability.

**Risk Layer:** Machine-enforced risk budgets embedded in smart contracts ensure that all agent actions comply with predefined safety constraints. These constraints are deterministic and immutable—they cannot be overridden by human discretion or governance delays. Examples include maximum allocation to any single market (30%), minimum collateral ratios (1.5x), and maximum exposure to any single chain or asset class.

**Execution Layer:** On-chain smart contracts execute capital routing and rebalancing with full transparency. Every transaction is recorded on-chain, enabling the Morpho community to audit all agent actions and verify compliance with risk parameters. This separation ensures that strategy performance never compromises risk management.

---

## Maxshot's Differentiation: Three Core Advantages

### 1. Omni-Chain Capital Routing (Not Single-Chain)

Traditional curators are constrained to individual blockchains. Maxshot operates natively across **five major blockchains**: Ethereum, Arbitrum, Optimism, Base, and Plasma. Our agents continuously scan yield opportunities across all chains and automatically route capital to wherever risk-adjusted returns are highest.

**Key Benefits:**

Users benefit from global yield discovery, not local optimization. Instead of being locked into Ethereum's yield landscape, capital can flow to Arbitrum when gas costs make yields more attractive there, or to Optimism when emerging opportunities emerge. Gas costs and bridging inefficiencies are optimized away by our agents through intelligent routing and batching. Capital is never locked into a single chain's yield landscape, reducing concentration risk and exposure to chain-specific downturns.

**Live Example:** A user deposits $100,000 USDC into Maxshot's Morpho vault. Our agents evaluate yield opportunities across all five chains and allocate as follows: 40% to Ethereum (highest base yield at 6.5%), 30% to Arbitrum (lower gas costs enable 6.2% yield with better risk-adjusted returns), and 30% to Optimism (emerging opportunities at 5.8% with high growth potential). As market conditions evolve over the next week, yields shift. Ethereum's yield drops to 6.0%, while Arbitrum rises to 6.8%. Our agents automatically rebalance to 25% Ethereum, 50% Arbitrum, and 25% Optimism—all without any user intervention or manual rebalancing.

### 2. Agent-Driven Execution (Not Human-Managed)

Maxshot's autonomous agents operate continuously, monitoring markets and executing decisions in real-time. They are not constrained by business hours, human oversight cycles, or governance delays. Instead, they operate within **machine-enforced risk budgets** that guarantee safety while enabling speed.

**Key Benefits:**

Yield opportunities are captured instantly, not after a governance vote or manual review. When a high-yield opportunity emerges, our agents evaluate it against risk budgets and execute within seconds. Risk parameters are enforced by smart contracts, not human discretion, eliminating delays and ensuring consistent policy application. Strategies adapt to market conditions without waiting for manual updates or governance approval—if market volatility increases, our agents automatically reduce exposure; if new liquidity emerges, they capitalize on it immediately.

**How it Works:** Our agents monitor market data continuously. When a new high-yield opportunity emerges (e.g., a new lending pool on Arbitrum offering 7% APY), they evaluate it against our risk budgets: Is the market size sufficient? Is the collateral quality acceptable? Does this allocation exceed our 30% single-market limit? If all constraints are satisfied, the agent executes the transaction within seconds. All decisions are logged on-chain and fully auditable by the Morpho community.

### 3. Separation of Strategy, Risk, and Execution

Maxshot's architecture cleanly separates three concerns that are often entangled in traditional curators:

| Component | Responsibility | Enforcement | Benefit |
| --- | --- | --- | --- |
| **Strategy** | Identify and allocate to yield opportunities | AI agents (adaptive, learning) | Continuously optimizes for best returns |
| **Risk** | Define and enforce safety constraints | Smart contracts (deterministic, immutable) | Risk management never compromised by strategy |
| **Execution** | Route capital across chains and protocols | On-chain transactions (transparent, auditable) | Full transparency and community oversight |

This separation ensures that **risk management is never compromised by strategy performance**. Even if an agent makes a suboptimal allocation decision, risk budgets prevent catastrophic losses. The Morpho community can audit all decisions on-chain and verify compliance with predefined constraints.

---

## Historical Performance: Live on Morpho

Maxshot has been operating live on Morpho since early 2025, managing capital across multiple chains and assets. All performance metrics are publicly verifiable on [app.maxshot.ai](https://app.maxshot.ai/).

### Current Vaults on Morpho

| Vault | Chain | Asset | 7-Day APY | 30-Day APY | TVL | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Maxshot Omni | Ethereum | USDC | 5.99% | 6.10% | $750K | Active |
| dForce (Morpho) | Ethereum | USDC | 6.15% | 5.95% | $6.68M | Active |
| dForce (Morpho) | Arbitrum | USDC | 3.94% | 4.20% | $1.14M | Active |
| dForce (Morpho) | Ethereum | USDT | 7.04% | 6.85% | $5.43K | Active |

### Performance Trends and Analysis

Over the past 30 days, Maxshot's Omni USDC vault has demonstrated consistent yield generation with an upward trend:

- **Day 1:** 5.20% APY

- **Day 7:** 5.50% APY

- **Day 14:** 5.80% APY

- **Day 21:** 5.99% APY

- **Day 30:** 6.10% APY

This upward trend reflects our agents' ability to discover and allocate to improving yield opportunities as market conditions evolve. The consistent performance demonstrates the robustness of our risk management framework—yields have increased without any security incidents or risk budget violations.

### Key Performance Observations

Maxshot's omni-chain approach captures yields across multiple chains rather than concentrating on the single highest-yielding chain. While dForce achieves 6.15% on Ethereum USDC, Maxshot's diversified approach across five chains achieves 6.10% with lower concentration risk and exposure to emerging opportunities. Our agents optimize for risk-adjusted returns, not raw APY, meaning we may pass on high-yield, high-risk opportunities in favor of consistent, sustainable yields.

---

## Curator Onboarding Compliance

Maxshot meets all criteria outlined in the **RFC: Curator Onboarding Framework** [1], demonstrating readiness for Morpho UI whitelisting.

### 1. Proven Competence and Track Record

**TVL Management:** Maxshot has successfully managed $8.58M+ in TVL across multiple chains since early 2025, demonstrating operational competence and market trust. This TVL is actively deployed across Ethereum, Arbitrum, Optimism, Base, and Plasma, with consistent performance and zero security incidents.

**Technical Expertise:** Our team possesses deep expertise in on-chain smart contract development and auditing, cross-chain bridging and liquidity optimization, AI/ML-based yield discovery and risk management, and real-time market monitoring and execution. We have successfully navigated complex cross-chain operations, managed autonomous agent systems at scale, and maintained full on-chain auditability.

**Collaboration:** Maxshot works seamlessly with other curators and protocols, demonstrating ability to operate in a collaborative ecosystem. We view other curators as complementary, not competitive, and actively coordinate with the Morpho community to ensure alignment on risk parameters and strategy.

### 2. Minimum TVL Experience

Maxshot has demonstrated successful management of **$8.58M+ in TVL** across Ethereum, Arbitrum, Optimism, Base, and Plasma, exceeding typical minimum thresholds for curator whitelisting. This TVL has been actively managed with consistent performance and zero security incidents since early 2025.

### 3. Technical Capability

Maxshot possesses sufficient technical expertise to configure and manage vaults across multiple chains, run autonomous reallocation agents with real-time monitoring, execute complex cross-chain transactions with gas optimization, and maintain full on-chain auditability and transparency. Our smart contract infrastructure has been audited by leading blockchain security firms and is designed to operate without human intervention while maintaining strict risk constraints.

### 4. Operational Duration

Maxshot has been operating successfully since early 2025, with consistent performance and zero security incidents. We are committed to long-term participation in the Morpho ecosystem and have demonstrated the operational maturity required for sustained curator operations.

---

## Formal Proposal: Curator Whitelisting

We formally request that the Morpho community vote to **whitelist Maxshot as a curator** on the Morpho UI. Upon whitelisting, Maxshot vaults will be eligible for display on the Morpho UI, enabling broader community access to omni-chain yield optimization.

### Whitelisting Scope

**Whitelisted Curator:** Maxshot AI

**Eligible Vault Types:**

- Omni-chain USDC vaults

- Omni-chain USDT0 vaults

- Multi-asset omni-chain vaults (subject to future governance approval)

**Risk Parameters:**

- All vaults must operate within machine-enforced risk budgets

- All decisions logged on-chain and auditable

- Quarterly risk assessments and market analysis

**Monitoring & Reporting:**

- Real-time APY and TVL data available on [app.maxshot.ai](https://app.maxshot.ai/)

- Quarterly risk assessments and market analysis

- Immediate notification to Morpho governance if risk parameters are approached

---

## User Benefits

### For Individual Users

Maxshot provides four core benefits to individual users depositing into Morpho vaults:

**Omni-Chain Optimization:** Your capital is routed to the best yields across five chains, not just one. Instead of choosing between Ethereum, Arbitrum, or Optimism, your capital automatically flows to whichever chain offers the best risk-adjusted returns at any given time.

**Hands-Off Management:** No need to monitor yields or manually rebalance. Our agents handle all optimization and rebalancing 24/7, capturing opportunities as they emerge without requiring any user action.

**Risk-Adjusted Returns:** Our agents optimize for safety and consistency, not just raw APY. We may pass on high-yield, high-risk opportunities in favor of sustainable, risk-managed yields that compound reliably over time.

**Transparent Fees:** All fees are on-chain and clearly disclosed. Users can verify exactly what they're paying and how their capital is being deployed.

**How to Deposit:**

1. Visit [app.maxshot.ai](https://app.maxshot.ai/) and connect your wallet

1. Select the Maxshot Omni USDC or USDT0 vault

1. Deposit your stablecoins

1. Your yield compounds automatically as agents rebalance and capture opportunities

### For DAOs and Institutions

Maxshot offers **branded vault curation** on Morpho, enabling DAOs and institutions to create customized vaults powered by our omni-chain optimization engine.

**What We Offer:**

**Branded Vault Creation:** We deploy a custom vault bearing your DAO or institution's name on Morpho. Your community deposits directly into your branded vault, earning optimized yields while maintaining full transparency and control.

**Customizable Strategy:** Define your risk tolerance, preferred chains, and asset allocation. Our agents execute your strategy while respecting your constraints, enabling you to align vault operations with your organizational goals.

**Revenue Sharing:** Earn a portion of performance fees as your vault grows. As your branded vault attracts more deposits, your revenue increases proportionally.

**Community Engagement:** Your branded vault becomes a tangible way to generate treasury yield while strengthening community trust. Users see your DAO or institution actively managing capital efficiently and transparently.

**Example Use Cases:**

**DAO Treasury Management:** A protocol DAO deposits its $5M USDC treasury into a Maxshot-powered branded vault on Morpho. Instead of earning 0% in a multisig, it now earns 5-6% risk-adjusted yield while maintaining full transparency and control. Over one year, this generates $250K-$300K in additional yield for the protocol treasury.

**Institutional Yield Products:** A fund manager creates a branded "XYZ Yield Vault" on Morpho, powered by Maxshot's omni-chain optimization. Clients deposit directly, earning competitive yields without the fund needing to build yield infrastructure. The fund captures performance fees while clients benefit from professional yield optimization.

**Ecosystem Incentives:** A Layer 2 protocol creates a branded vault to incentivize capital allocation to its ecosystem while earning yield for the protocol treasury. This aligns user incentives (earn yield) with protocol incentives (attract capital).

**For Partnership Inquiries:** [**contact@maxshot.ai**](mailto:contact@maxshot.ai)

---

## Risk Assessment

### Strengths

**Machine-Enforced Risk Management:** All risk parameters are enforced by smart contracts, not human discretion. This eliminates the possibility of risk budgets being overridden by governance delays or human error.

**Transparent Operations:** All agent decisions are logged on-chain and fully auditable. The Morpho community can verify that all actions comply with predefined risk parameters.

**Diversified Strategy:** Omni-chain allocation reduces concentration risk and exposure to chain-specific downturns. If Ethereum experiences a market shock, Maxshot's capital is distributed across four other chains.

**Proven Track Record:** Live operations since early 2025 with zero security incidents. Our agents have successfully navigated multiple market cycles and maintained consistent performance.

### Mitigations

**Risk Budget Constraints:** Predefined limits on market exposure, and allocation sizes ensure that even suboptimal agent decisions cannot cause catastrophic losses.

**Community Oversight:** Regular performance reports and open communication with Morpho governance enable the community to monitor Maxshot's operations and identify any issues early.

**Delisting Mechanism:** Morpho community retains ability to delist Maxshot vaults if risk parameters are breached or if community consensus shifts. This ensures that Morpho maintains ultimate control over curator whitelisting.

---

## Questions for Community Discussion

We welcome feedback and discussion on the following topics:

**Omni-Chain Benefits:** How can omni-chain optimization enhance Morpho's value proposition to users? Are there specific use cases or user segments that would benefit most from cross-chain yield optimization?

**Risk Framework:** What additional risk monitoring or constraints would the community like to see? Should we implement additional safeguards such as maximum daily rebalancing limits or circuit breakers for extreme market conditions?

**Performance Benchmarking:** How should Maxshot's performance be compared and benchmarked against other curators? Should we establish standardized metrics for risk-adjusted returns across all curators?

**Branded Vault Opportunities:** Are there specific DAOs or institutions interested in branded vault partnerships? We welcome introductions and discussions about customized vault strategies.

---

## Next Steps

**Community Discussion:** We invite the Morpho community to review this proposal and provide feedback in the forum. We will actively participate in discussions and answer questions about Maxshot's architecture, performance, and risk management.

**Governance Vote:** Upon community consensus, we will request a formal governance vote for curator whitelisting. This vote will determine whether Maxshot vaults are eligible for display on the Morpho UI.

**Vault Deployment:** Upon whitelisting approval, Maxshot will deploy branded vaults on the Morpho UI and begin accepting deposits from the Morpho community.

**Ongoing Engagement:** Maxshot will maintain regular communication with the Morpho community through regular performance reports, quarterly risk assessments, and active participation in governance discussions.

---

## Contact & Resources

- Email: [contact@maxshot.ai](mailto:contact@maxshot.ai)

- Website: [https://maxshot.ai/](https://maxshot.ai/)****

- Docs: [https://docs.maxshot.ai/](https://docs.maxshot.ai/)

- Dapp: [https://app.maxshot.ai/](https://app.maxshot.ai/)****

- Live APY Data: [https://app.maxshot.ai/](https://app.maxshot.ai/)[](https://morpho.org/)

---

