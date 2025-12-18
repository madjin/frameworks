# Documentation FAQ Audit Report

Generated: 2025-12-18

## Summary

| Metric | Count | Percentage |
|--------|-------|------------|
| **Total MDX pages** | 328 | 100% |
| **Pages with FAQ sections** | 2 | 0.6% |
| **Pages with Troubleshooting sections** | 1 | 0.3% |
| **Overview pages (overview.mdx)** | 46 | 14% |
| **Index pages (index.mdx)** | 59 | 18% |
| **Overview pages missing FAQs** | 44 | 95.6% of overviews |

---

## Priority Pages Needing FAQs

### High Priority (Main Framework Entry Points)

These overview pages are primary entry points and would most benefit from FAQs:

| Page | Topic | Current Status | Suggested FAQ Count |
|------|-------|----------------|---------------------|
| `wallet-security/overview.mdx` | Wallet fundamentals | No FAQ | 8 |
| `incident-management/overview.mdx` | Incident response | No FAQ | 6 |
| `multisig-for-protocols/overview.mdx` | Multisig security | No FAQ | 7 |
| `infrastructure/overview.mdx` | Cloud/DNS/DDoS | No FAQ | 6 |
| `dprk-it-workers/overview.mdx` | Insider threats | No FAQ | 8 |
| `external-security-reviews/overview.mdx` | Audits | No FAQ | 6 |
| `awareness/overview.mdx` | Security culture | No FAQ | 5 |
| `security-testing/overview.mdx` | Testing methods | No FAQ | 6 |

### Medium Priority (Sub-framework Entry Points)

| Page | Topic |
|------|-------|
| `opsec/overview.mdx` | Operational security |
| `ens/overview.mdx` | Ethereum Name Service |
| `community-management/overview.mdx` | Discord/Telegram/Twitter |
| `privacy/overview.mdx` | Privacy practices |
| `threat-modeling/overview.mdx` | Threat assessment |
| `governance/overview.mdx` | DAO governance |
| `supply-chain/overview.mdx` | Dependency security |

---

## Suggested FAQ Questions

### wallet-security/overview.mdx

```html
## FAQ

<details>
<summary>What is the difference between a hot wallet and a cold wallet?</summary>

A hot wallet is connected to the internet and allows for quick transactions, but has higher exposure to online attacks. A cold wallet is stored offline (hardware device or paper) and provides stronger security for long-term storage, but requires physical access to sign transactions.

</details>

<details>
<summary>Should I use a custodial or non-custodial wallet?</summary>

Non-custodial wallets give you full control over your private keys ("not your keys, not your coins"), but you are responsible for security and backup. Custodial wallets (exchanges) manage keys for you, offering convenience but introducing counterparty risk. For significant funds, non-custodial is recommended.

</details>

<details>
<summary>When should I use a multisig wallet instead of a single-key wallet?</summary>

Use a multisig wallet when managing funds that require shared control (DAOs, treasuries, business accounts), when you want protection against single-key compromise, or when holding high-value assets. Multisig requires multiple signatures (e.g., 2-of-3) to authorize transactions.

</details>

<details>
<summary>How do I safely store my seed phrase?</summary>

Store your seed phrase offline on durable materials (metal backup, paper in fireproof safe). Never store it digitally (photos, cloud, password managers). Consider geographic distribution for redundancy. See the Seed Phrase Management guide for detailed recommendations.

</details>

<details>
<summary>What is account abstraction and when should I consider it?</summary>

Account abstraction (ERC-4337) enables smart contract wallets with features like social recovery, spending limits, and gasless transactions. Consider account abstraction wallets when you need programmable security rules or want recovery options beyond seed phrases.

</details>
```

---

### incident-management/overview.mdx

```html
## FAQ

<details>
<summary>What is the first thing I should do when I discover a security incident?</summary>

Immediately contain the threat by revoking compromised credentials, pausing affected contracts if possible, and isolating compromised systems. Then notify your incident response team and begin documentation. Speed matters—every minute of delay can increase losses.

</details>

<details>
<summary>How do I contact SEAL 911 during an active incident?</summary>

SEAL 911 provides emergency response support for Web3 security incidents. Contact them through seal.org or the designated emergency channels. Have your wallet addresses, transaction hashes, and timeline ready when you reach out.

</details>

<details>
<summary>Should I publicly disclose an incident immediately?</summary>

Not immediately. First contain the threat and assess the scope. Premature disclosure can tip off attackers or cause panic. Follow your communication strategy: notify affected users promptly but only after you have accurate information about what happened and what actions users should take.

</details>

<details>
<summary>What should be included in a post-incident report?</summary>

Include: timeline of events, root cause analysis, systems and funds affected, response actions taken, remediation steps, and lessons learned. Be factual and transparent. Post-mortems help the community learn and build trust through accountability.

</details>

<details>
<summary>How often should we run incident response drills?</summary>

Run tabletop exercises quarterly and full simulations annually. Update playbooks after each drill based on lessons learned. Regular practice ensures your team can respond effectively under pressure when real incidents occur.

</details>
```

---

### multisig-for-protocols/overview.mdx

```html
## FAQ

<details>
<summary>What threshold (M-of-N) should I use for my multisig?</summary>

Common configurations: 2-of-3 for small teams (balance of security and availability), 3-of-5 or 4-of-7 for larger organizations. Higher thresholds increase security but risk lockout if signers become unavailable. Ensure you have backup signers or recovery procedures.

</details>

<details>
<summary>How do I safely verify a multisig transaction before signing?</summary>

Verify the transaction on your hardware wallet's screen, not just the web interface. Check the recipient address, amount, and contract interaction details match what was requested. Use the verification guides for Safe or Squads depending on your platform.

</details>

<details>
<summary>What should I do if I suspect a signer's keys are compromised?</summary>

Immediately initiate key rotation procedures. Remove the compromised signer and add a replacement. If you suspect active attack, pause operations and assess what transactions may have been queued. Follow the Emergency Procedures guide.

</details>

<details>
<summary>Can I use a software wallet as one of my multisig signers?</summary>

Hardware wallets are strongly recommended for all signers managing significant funds. Software wallets (browser extensions, mobile apps) have higher attack surface. If you must use software wallets, ensure they are on dedicated devices with strong security practices.

</details>

<details>
<summary>How do I onboard a new signer to our multisig?</summary>

Follow the Joining a Multisig guide. The new signer should set up their hardware wallet securely, share only their public address (never private keys), and be added through a properly verified transaction. Provide training on verification procedures before they sign any transactions.

</details>
```

---

### dprk-it-workers/overview.mdx

```html
## FAQ

<details>
<summary>What are the warning signs that a job candidate might be a DPRK IT worker?</summary>

Red flags include: reluctance to appear on video calls, inconsistencies between resume and interview performance, requests for payment to unusual destinations, working hours that suggest different time zones, generic GitHub profiles with recent activity spikes, and resistance to identity verification processes.

</details>

<details>
<summary>What should I do if I suspect I hired a DPRK IT worker?</summary>

Do not alert the individual. Document all evidence, restrict their access immediately but quietly, consult legal counsel about sanctions compliance, and consider reporting to relevant authorities. Preserve all communications and code contributions for investigation.

</details>

<details>
<summary>Is paying a DPRK IT worker illegal even if I did not know their identity?</summary>

Potentially yes. DPRK is under international sanctions, and unknowing violations can still carry legal consequences. The key factors are due diligence efforts and prompt action upon discovery. Consult legal counsel familiar with OFAC sanctions if you suspect exposure.

</details>

<details>
<summary>How can I harden my hiring process against insider threats?</summary>

Implement video interviews with identity verification, verify work history and references, use background check services, require multi-factor authentication for all employees, limit access based on role necessity, and monitor for suspicious behavior patterns. See the Mitigation guide for detailed steps.

</details>

<details>
<summary>What are the organizational risks beyond financial loss?</summary>

Risks include: sanctions violations leading to asset freezes, supply chain compromise through malicious code, extortion attempts, reputational damage, criminal investigations, and loss of access to banking services. The impact extends far beyond the salary paid.

</details>
```

---

### infrastructure/overview.mdx

```html
## FAQ

<details>
<summary>Should I use a single provider for all infrastructure or multiple providers?</summary>

Both approaches have trade-offs. Single provider: simpler management, unified security controls, but single point of failure. Multiple providers: redundancy and reduced vendor lock-in, but increased complexity and more attack surface to secure. Choose based on your risk tolerance and operational capacity.

</details>

<details>
<summary>What are the most critical infrastructure security priorities for a Web3 project?</summary>

Priority order: (1) DNS and domain registrar security—domain hijacking can redirect users to phishing sites, (2) DDoS protection—availability attacks are common, (3) Cloud access controls—misconfigured IAM is a leading breach cause, (4) Zero-trust network architecture.

</details>

<details>
<summary>How do I protect against DNS hijacking attacks?</summary>

Enable registrar lock, use DNSSEC, enable MFA on registrar accounts, use dedicated email for domain accounts, monitor DNS records for unauthorized changes, and consider using multiple DNS providers. See the Domain and DNS Security section for detailed guidance.

</details>

<details>
<summary>What is zero-trust architecture and do I need it?</summary>

Zero-trust assumes no user or system is inherently trusted, requiring verification for every access request regardless of network location. For Web3 projects with remote teams and valuable assets, zero-trust principles significantly reduce the impact of compromised credentials.

</details>
```

---

### external-security-reviews/overview.mdx

```html
## FAQ

<details>
<summary>When should I get an external security review?</summary>

Before mainnet launch (mandatory for smart contracts), after significant code changes, before major upgrades, and periodically (annually minimum) for ongoing projects. Also consider reviews before integrating new third-party dependencies.

</details>

<details>
<summary>How do I choose between different security auditors?</summary>

Evaluate: relevant experience with your tech stack, reputation and track record, methodology and tooling, timeline availability, communication style, and post-audit support. Get multiple quotes and check references from past clients. See the Vendor Selection guide.

</details>

<details>
<summary>What should I prepare before engaging an auditor?</summary>

Prepare: complete documentation, clean and well-commented code, test suite with good coverage, deployment instructions, architecture diagrams, and a list of known issues or areas of concern. Better preparation leads to more effective audits.

</details>

<details>
<summary>Does passing an audit mean my code is secure?</summary>

No. Audits are time-boxed assessments that reduce risk but cannot guarantee security. They may miss issues, and new vulnerabilities can emerge after the audit. Treat audits as one layer of defense alongside testing, monitoring, and incident response capabilities.

</details>
```

---

### awareness/overview.mdx

```html
## FAQ

<details>
<summary>What is security awareness and why does it matter?</summary>

Security awareness is the ability to recognize threats, question suspicious activity, and respond appropriately. Human error is involved in most security breaches. A security-aware team is your first line of defense against social engineering, phishing, and targeted attacks.

</details>

<details>
<summary>How do I build a security culture in my organization?</summary>

Lead by example, make security training engaging and relevant, reward reporting of suspicious activity, conduct regular phishing simulations, and integrate security into daily workflows rather than treating it as a separate concern.

</details>

<details>
<summary>What are the most common attack vectors targeting Web3 projects?</summary>

Social engineering (fake job offers, compromised Discord/Telegram), phishing (fake dApps, malicious signatures), supply chain attacks (compromised dependencies), and insider threats. See Understanding Threat Vectors for detailed coverage.

</details>

<details>
<summary>How often should security training be conducted?</summary>

Conduct formal training at onboarding and annually thereafter. Supplement with ongoing awareness: security tips in team channels, incident debriefs, and simulated phishing exercises quarterly. Security awareness should be continuous, not a one-time event.

</details>
```

---

### security-testing/overview.mdx

```html
## FAQ

<details>
<summary>What types of testing should every smart contract project implement?</summary>

At minimum: unit tests (always, with high code coverage), integration tests (always, can combine with fork testing), fuzz tests (always, most unit tests can be fuzz tests), and static analysis (always, using tools like Slither and Aderyn). Formal verification is recommended for math-heavy or stateless functions.

</details>

<details>
<summary>What is fuzz testing and why is it important for smart contracts?</summary>

Fuzz testing automatically generates random or unexpected inputs to find edge cases and vulnerabilities that manual testing might miss. For smart contracts, fuzzing can discover integer overflows, unexpected state transitions, and other bugs that only manifest with specific input combinations.

</details>

<details>
<summary>How do I measure the effectiveness of my test suite?</summary>

Use coverage analysis to see how thoroughly tests exercise code paths (aim for high branch coverage). Use mutation testing to verify tests actually catch bugs—it introduces small code changes and checks if tests fail. Both together give a complete picture of test quality.

</details>

<details>
<summary>When should I use formal verification?</summary>

Use formal verification for math-heavy functions, stateless logic, and functionality that must match another system's behavior. Formal verification mathematically proves correctness but requires significant expertise and is typically reserved for critical code paths.

</details>

<details>
<summary>What static analysis tools are recommended for Solidity?</summary>

Slither (by Trail of Bits) and Aderyn (by Cyfrin) are widely used. These tools analyze code without executing it to find common vulnerability patterns, code quality issues, and potential security risks. Run static analysis in CI/CD pipelines for every commit.

</details>
```

---

## Pages Already with FAQs (Reference)

| Page | FAQ Count |
|------|-----------|
| `safe-harbor/overview.mdx` | 11 Q&A pairs |
| `certs/overview.mdx` | 11 Q&A pairs |

## Page with Troubleshooting Section

| Page | Format |
|------|--------|
| `multisig-for-protocols/backup-signing-and-infrastructure.mdx` | `## Troubleshooting` with Common Issues subsection |

---

## Recommendations

1. **Start with high-priority overview pages** — These are entry points that users visit first
2. **Use consistent format** — `<details><summary>` HTML pattern already established
3. **5-8 questions per page** — Enough to be useful, not overwhelming
4. **LLM-optimized answers** — Use explicit nouns, complete context, consistent terminology
5. **Add Troubleshooting sections** to technical implementation guides (setup, configuration pages)

---

## FAQ HTML Template

```html
## FAQ

<details>
<summary>Question text ending with a question mark?</summary>

Answer text here. Supports **markdown** formatting, [links](url), and code blocks.

Multiple paragraphs are allowed.

</details>
```

### Format Rules
- Place FAQ section near the end of the page, before `</TagProvider>` and `<ContributeFooter />`
- Use `## FAQ` as the section heading
- Each Q&A pair uses `<details>` and `<summary>` tags
- Questions go inside `<summary>` tags, end with `?`
- Answers go between closing `</summary>` and closing `</details>`
- Add blank lines around content for proper markdown parsing
- 5-12 Q&A pairs is ideal; more than 15 becomes unwieldy
