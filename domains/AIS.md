# AIS — AI Security

> Governance of AI tools, Shadow AI prevention, and EU AI Act compliance.

**5 controls** · T1: 3 · T2: 1 · T3: 1

---

## Controls

### AIS-01 — Acceptable AI use policy `T1`

**NIS2:** Art. 21(2)(a) | **EU AI Act:** Art. 50 | **GEO 155:** —

The organization must have a documented AI usage policy specifying: which AI tools are permitted, which categories of data must NOT be entered into public AI systems (confidential data, personal data, trade secrets, proprietary source code), and human review requirements for AI-generated content used in business decisions.

> **Rationale:** Employees entering sensitive data into ChatGPT or other public LLMs is the most common AI data leakage vector. A clear, communicated policy significantly reduces risk before any technical controls are implemented.

---

### AIS-02 — AI tool inventory and Shadow AI prevention `T1`

**NIS2:** Art. 21(2)(e) | **EU AI Act:** Art. 26 | **GEO 155:** —

Maintain an up-to-date inventory of all AI tools used in the organization (approved and unauthorized). Block unauthorized AI tools at the proxy/firewall level. Monthly review to identify new uncontrolled adoptions. The approval process for new AI tools must include an assessment of how the vendor processes transmitted data.

> **Rationale:** 20% of organizations have suffered a breach due to Shadow AI in the past year. Employees adopt AI tools without security evaluation — visibility is the first control step.

---

### AIS-03 — Prevent data exfiltration through AI tools `T1`

**NIS2:** Art. 21(2)(h) | **EU AI Act:** Art. 26 | **GEO 155:** Art. 5(1)

Implement DLP (Data Loss Prevention) rules to detect and block transmission of confidential or personal data to external AI APIs. Monitor traffic to known AI endpoints (api.openai.com, etc.). API keys for AI services must be managed through a vault (see IAM-06) and never hard-coded.

> **Rationale:** Data leaks through AI tools are difficult to detect after the fact — data transmitted to an LLM may be used for training or accessed by other users. Technical controls are essential alongside the AIS-01 policy.

---

### AIS-04 — Human oversight for AI decisions `T2`

**NIS2:** Art. 21(2)(b) | **EU AI Act:** Art. 26 | **GEO 155:** —

Any significant business decision assisted by AI (CV screening, financial approvals, external communications, production code) must be reviewed and approved by a competent person before implementation. Agentic AI systems (acting autonomously) must have explicit restrictions on autonomy and must log all actions taken.

> **Rationale:** AI systems make factual errors, can be manipulated through prompt injection, and do not understand organizational context. Human oversight prevents erroneous decisions with operational or reputational impact.

---

### AIS-05 — EU AI Act compliance for high-risk AI systems `T3`

**NIS2:** Art. 21(2)(c) | **EU AI Act:** Art. 26, 27, 29 | **GEO 155:** —

Organizations using or deploying high-risk AI systems (per EU AI Act Annex III: biometrics, critical infrastructure, employment, education, essential services) must: designate a person responsible for system oversight, maintain up-to-date technical documentation, log all AI decisions (minimum 6 months), conduct a fundamental rights impact assessment (Art. 27) before deployment, and report significant incidents to ANPC/DNSC.

> **Rationale:** EU AI Act requirements for high-risk systems become enforceable in August 2026. Non-compliance carries fines of up to 3% of global turnover (50% reduction for SMEs). Early implementation of documentation and oversight avoids crisis remediation costs.
