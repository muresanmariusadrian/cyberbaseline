# Changelog

All notable changes to CyberBaseline are documented here.

## [2.0.0] — 2026-04-20

### Simplified: 36 → 24 controls, full NIS2 coverage maintained

**Design goal:** Reduce complexity without losing regulatory alignment. Every NIS2 article covered in v1.x remains covered in v2.0.

#### Merges by domain

- **IAM** (6 → 4): IAM-04 + IAM-05 merged into "Gestionarea ciclului de viață al accesurilor". IAM-06 (Secrets Vault) removed from core framework — not NIS2-mapped and better addressed as part of IAM-01 operational guidance.
- **EML** (4 → 3): EML-03 (External marking) + EML-04 (Macro disable) merged into "Întărirea configurației de email" — both are email hardening measures sharing NIS2 Art. 21(2)(b).
- **NET** (7 → 5): NET-03 (DNS) + NET-04 (Guest WiFi) merged into "Protecție DNS și segmentare rețea WiFi"; NET-05 (Cloud config) + NET-06 (Cloud storage) merged into "Securizarea infrastructurii cloud". NET-07 renumbered NET-05.
- **EPT** (4 → 3): EPT-03 (Disk encryption) + EPT-04 (Asset inventory) merged into "Inventar și hardening dispozitive".
- **DAT** (5 → 3): DAT-01 (Classification) + DAT-04 (GDPR register) merged into "Clasificarea datelor și registrul GDPR"; DAT-02 + DAT-05 merged into "Strategie completă de backup" (both mapped to NIS2 Art. 21(2)(c)).
- **INC** (5 → 3): INC-01 (IR Plan) + INC-02 (NIS2 notification) merged — the notification procedure is a natural part of the IR plan; INC-04 (Isolation) + INC-05 (Forensics) merged into "Containment și investigare criminalistică".
- **AIS** (5 → 3): AIS-01 (Policy) + AIS-02 (Inventory) merged — policy and inventory are operationally inseparable; AIS-04 (Human oversight) + AIS-05 (EU AI Act) merged into "Guvernanță AI și conformitate EU AI Act".

**Updated totals:** 24 controls · 7 domains · NIS2 coverage: all original articles preserved

---

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
