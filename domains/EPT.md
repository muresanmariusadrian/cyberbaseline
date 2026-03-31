# EPT — Endpoint Protection

> Protection of devices, patch management, and asset inventory.

**4 controls** · T1: 4

---

## Controls

### EPT-01 — EDR solution on all devices `T1`

**NIS2:** Art. 21(2)(b) | **GEO 155:** Art. 5(1)(c)

All managed devices (laptops, desktops, servers) must run an Endpoint Detection & Response (EDR) solution. Coverage must be monitored and maintained at 100%. Critical alerts must be investigated within 24 hours.

> **Rationale:** EDR provides visibility and response capability against advanced threats that exceed traditional antivirus capabilities. It is the foundational component of modern endpoint protection.

---

### EPT-02 — Automated patch management `T1`

**NIS2:** Art. 21(2)(e) | **GEO 155:** Art. 5(1)(e)

Critical security updates must be applied within 72 hours of availability across all systems. Important patches must be applied within 7 days. Unpatched systems must be isolated or urgently remediated.

> **Rationale:** Exploitation of unpatched vulnerabilities causes over 60% of security breaches. Automated patch management reduces the exposure window to a minimum.

---

### EPT-03 — Full disk encryption on laptops `T1`

**NIS2:** — | **GEO 155:** —

All laptops and portable devices must have full disk encryption enabled (BitLocker on Windows, FileVault on macOS). Recovery keys must be stored centrally in Azure AD or a secure vault.

> **Rationale:** Loss or theft of an unencrypted laptop constitutes a reportable data breach. Disk encryption protects organizational data without affecting usability.

---

### EPT-04 — Hardware and software asset inventory `T1`

**NIS2:** — | **GEO 155:** —

Maintain an up-to-date inventory of all hardware devices and software applications in the organization. Automatic discovery through network scanning. Monthly review to identify unauthorized assets.

> **Rationale:** You can't protect what you don't know exists. A complete inventory is the prerequisite for any effective security program and the foundation for patch management and monitoring.
