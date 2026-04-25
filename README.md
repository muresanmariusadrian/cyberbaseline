# CyberBaseline

**The cybersecurity baseline standard for Romanian SMBs**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![NIS2](https://img.shields.io/badge/NIS2-aligned-blue)](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32022L2555)

An open-source cybersecurity framework designed for organizations without dedicated security teams. **24 practical controls**, organized across **7 domains** and **3 maturity levels**, aligned with NIS2.

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
| [IAM](domains/IAM.md) | Identity & Access Management | 4 |
| [EML](domains/EML.md) | Email Security | 3 |
| [NET](domains/NET.md) | Network & Infrastructure | 5 |
| [EPT](domains/EPT.md) | Endpoint Protection | 3 |
| [DAT](domains/DAT.md) | Data Protection | 3 |
| [INC](domains/INC.md) | Incident Management | 3 |
| [AIS](domains/AIS.md) | AI Security | 3 |

**Total: 24 controls**

### Maturity levels

| Level | Label | Description |
|-------|-------|-------------|
| L1 | **Minim** | All 24 controls implemented at baseline — essential measures documented and functional. |
| L2 | **Bun** | All 24 controls implemented at intermediate depth — consolidated, tested, and partially automated. |
| L3 | **Puternic** | All 24 controls implemented at advanced level — automated and continuously monitored. |

An organization's maturity is determined by the deepest level at which **all** controls are implemented.

---

## NIS2 compliance

All controls are mapped to relevant articles in the **NIS2 Directive** (EU 2022/2555).

Organizations in essential sectors (energy, transport, health, finance, water, digital infrastructure) and important sectors (postal, waste management, manufacturing, digital services) have legal compliance obligations.

---

## How to use this framework

### 1. Assess your current state
Go through the controls and check what you already have in place. Most SMBs implement 40–60% of L1 without realizing it.

### 2. Prioritize by impact
Start with:
- **IAM-01** (MFA for admins) — maximum impact, minimum effort
- **EPT-02** (patch management) — eliminates 60%+ of attack vectors
- **DAT-02** (3-2-1 backup) — ransomware last line of defense
- **EML-01** (SPF/DKIM/DMARC) — stops domain spoofing

### 3. Document your implementation
Each control has clear criteria for L1, L2, and L3. Document what you've implemented, when, and how — useful for audits and NIS2 notifications.

### 4. Progress through levels
Once all controls are at L1, evaluate L2 criteria based on your organization's risk profile.

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
| [`domains/AIS.md`](domains/AIS.md) | AI Security |

---

## Contributing

Contributions are welcome — especially:
- Corrections or clarifications to control descriptions
- Additional NIS2 mappings
- Practical implementation examples

Open an **Issue** for discussion or a **Pull Request** for direct changes.

---

## License

CyberBaseline is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

Free to use, adapt, and redistribute with attribution.
