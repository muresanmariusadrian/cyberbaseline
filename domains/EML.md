# EML — Email Security

> Security of email communications and protection against phishing and BEC attacks.

**4 controls** · T1: 4

---

## Controls

### EML-01 — Configure SPF, DKIM, and DMARC `T1`

**NIS2:** Art. 21(2)(h) | **GEO 155:** —

The organization's email domain must have SPF, DKIM, and DMARC DNS records configured with a minimum policy of `quarantine`. The DMARC policy must be monitored through aggregate reports (RUA) to detect unauthorized use of the domain.

> **Rationale:** SPF/DKIM/DMARC prevent domain spoofing used in BEC (Business Email Compromise) and phishing attacks. Proper configuration is a high-impact, low-cost measure.

---

### EML-02 — Anti-phishing and anti-malware filtering `T1`

**NIS2:** Art. 21(2)(b) | **GEO 155:** Art. 5(1)(c)

Deploy an email gateway with advanced anti-phishing filtering, malicious URL detection, and attachment sandboxing (Microsoft Defender for Office 365, Proofpoint, Mimecast). Filtering must be enabled for all users.

> **Rationale:** Over 90% of security incidents start with a malicious email. A modern email gateway blocks threats before they reach users.

---

### EML-03 — External email tagging `T1`

**NIS2:** — | **GEO 155:** —

All emails originating from outside the organization must be visibly tagged with a banner or subject prefix (e.g., `[EXTERNAL]`) to alert users to impersonation attempts of colleagues or management.

> **Rationale:** BEC attacks exploit the difficulty users have in distinguishing internal from external emails. Visible tagging significantly reduces the effectiveness of these attacks.

---

### EML-04 — Disable Office macros in emails `T1`

**NIS2:** Art. 21(2)(b) | **GEO 155:** —

Macros in Office documents received via email must be disabled by default through Group Policy or Intune. Exceptions require IT approval and must be limited to verified trusted sources.

> **Rationale:** Malicious macros in Office documents are an extremely common malware delivery vector. Disabling them by default eliminates an entire class of attacks.
