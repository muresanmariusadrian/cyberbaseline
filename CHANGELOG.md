# Changelog

All notable changes to CyberBaseline are documented here.

## [1.1.0] — 2026-04-01

### Added: AIS — AI Security domain

- **5 new controls** (AIS-01 through AIS-05) across 3 maturity tiers
- New regulatory mapping dimension: **EU AI Act** (EU 2024/1689) — all controls now include `eu_ai_act_mapped` and `eu_ai_act_article` fields
- AIS-01: Acceptable AI use policy (T1) — mapped to EU AI Act Art. 50
- AIS-02: AI tool inventory and Shadow AI prevention (T1) — mapped to EU AI Act Art. 26
- AIS-03: Prevent data exfiltration through AI tools (T1) — mapped to EU AI Act Art. 26
- AIS-04: Human oversight for AI decisions (T2) — mapped to EU AI Act Art. 26
- AIS-05: EU AI Act compliance for high-risk AI systems (T3) — mapped to EU AI Act Art. 26, 27, 29

**Updated totals:** 36 controls · 7 domains · T1: 29 · T2: 4 · T3: 3

**Why this matters:** CyberBaseline is the first SMB cybersecurity framework to integrate AI security controls alongside traditional security domains, aligned with both NIS2 and the EU AI Act — whose high-risk system requirements become enforceable in August 2026.

---

## [1.0.0] — 2025-03-31

### Initial release

- **31 controls** across **6 domains** (IAM, EML, NET, EPT, DAT, INC)
- **3 maturity tiers**: T1 Esențial (26), T2 Avansat (3), T3 Rezistent (2)
- Full NIS2 and GEO 155/2024 article mappings
- CLD (Cloud Security) domain absorbed into IAM, NET, and DAT — cloud controls are no longer treated as optional
- Framework reduced from 61 controls / 7 domains to focus on the 20% of controls that eliminate 80% of SMB breach risk
- Aligned with: ENISA guidelines, CIS Controls IG1, UK Cyber Essentials, CISA CPGs
