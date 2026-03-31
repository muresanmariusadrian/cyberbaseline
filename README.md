# CyberBaseline

**The cybersecurity baseline standard for Romanian SMBs**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![NIS2](https://img.shields.io/badge/NIS2-aligned-blue)](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022L2555)
[![GEO 155/2024](https://img.shields.io/badge/GEO%20155%2F2024-aligned-blue)](https://legislatie.just.ro)

An open-source cybersecurity framework designed for organizations without dedicated security teams. **31 practical controls**, organized across **6 domains** and **3 maturity tiers**, aligned with NIS2 and Romanian GEO 155/2024.

---

## Why CyberBaseline?

80% of breach risk comes from 20% of controls. For Romanian SMBs, the primary threats are:

1. **Phishing and BEC** — via email
2. **Ransomware** — via endpoint or exposed RDP
3. **Credential compromise** — weak passwords, no MFA
4. **Exposed services** — RDP, SMB, management ports open to the internet

CyberBaseline is built around these real threats, not an exhaustive academic taxonomy.

---

## Framework structure

### Security domains

| Abbr | Domain | Controls |
|------|--------|----------|
| [IAM](domains/IAM.md) | Identity & Access Management | 6 |
| [EML](domains/EML.md) | Email Security | 4 |
| [NET](domains/NET.md) | Network & Infrastructure | 7 |
| [EPT](domains/EPT.md) | Endpoint Protection | 4 |
| [DAT](domains/DAT.md) | Data Protection | 5 |
| [INC](domains/INC.md) | Incident Management | 5 |

**Total: 31 controls**

### Maturity tiers

| Tier | Label | Controls | Description |
|------|-------|----------|-------------|
| T1 | **Essential** | 26 | Foundational controls required for minimum NIS2 compliance. Fast to implement, immediate impact. |
| T2 | **Advanced** | 3 | Recommended for organizations with moderate risk profiles or sensitive data. |
| T3 | **Resilient** | 2 | Controls for organizations in essential or important sectors under NIS2. |

---

## NIS2 and GEO 155/2024 compliance

All controls are mapped to relevant articles in:
- **NIS2 Directive** (EU 2022/2555)
- **GEO 155/2024** — NIS2 transposition into Romanian law

Organizations in essential sectors (energy, transport, health, finance, water, digital infrastructure) and important sectors (postal, waste management, manufacturing, digital services) have legal compliance obligations.

---

## How to use this framework

### 1. Assess your current state
Go through T1 controls and check what you already have in place. Most SMBs implement 40–60% of T1 without realizing it.

### 2. Prioritize by impact
Start with:
- **IAM-01** (MFA for admins) — maximum impact, minimum effort
- **EPT-02** (patch management) — eliminates 60%+ of attack vectors
- **DAT-02** (3-2-1 backup) — ransomware last line of defense
- **EML-01** (SPF/DKIM/DMARC) — stops domain spoofing

### 3. Document your implementation
Each control has clear criteria. Document what you've implemented, when, and how — useful for audits and NIS2 notifications.

### 4. Progress to T2 and T3
Once T1 is fully implemented, evaluate T2 controls based on your organization's risk profile.

---

## Files

| File | Contents |
|------|----------|
| [`controls.json`](controls.json) | All controls in JSON format (source of truth) |
| [`domains/IAM.md`](domains/IAM.md) | Identity & Access Management |
| [`domains/EML.md`](domains/EML.md) | Email Security |
| [`domains/NET.md`](domains/NET.md) | Network & Infrastructure |
| [`domains/EPT.md`](domains/EPT.md) | Endpoint Protection |
| [`domains/DAT.md`](domains/DAT.md) | Data Protection |
| [`domains/INC.md`](domains/INC.md) | Incident Management |

---

## Contributing

Contributions are welcome — especially:
- Corrections or clarifications to control descriptions
- Additional NIS2 / GEO 155 mappings
- Practical implementation examples

Open an **Issue** for discussion or a **Pull Request** for direct changes.

---

## License

CyberBaseline is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

Free to use, adapt, and redistribute with attribution.
