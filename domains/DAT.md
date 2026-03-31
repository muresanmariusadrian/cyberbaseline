# DAT — Data Protection

> Protection, classification, backup, and governance of organizational data.

**5 controls** · T1: 5

---

## Controls

### DAT-01 — Data classification `T1`

**NIS2:** — | **GEO 155:** —

All data managed by the organization must be classified into categories (Public, Internal, Confidential, Secret) with clear handling policies for each category. Classification must be documented and communicated to employees.

> **Rationale:** Without classification, the organization doesn't know which data needs the strictest protection. Classification is the foundation on which all other data protection controls are built.

---

### DAT-02 — 3-2-1 backup for critical data `T1`

**NIS2:** Art. 21(2)(c) | **GEO 155:** Art. 5(1)(f)

Critical data must follow the 3-2-1 rule: at least 3 copies, on 2 different media, with 1 copy off-site or in the cloud. Backups must be tested via full restoration at least quarterly and protected against ransomware through immutable copies.

> **Rationale:** Backup is the last line of defense against ransomware. Immutable off-site copies make recovery possible even if all local systems are encrypted.

---

### DAT-03 — Data in transit encryption (TLS) `T1`

**NIS2:** Art. 21(2)(h) | **GEO 155:** —

All network traffic containing sensitive data must be encrypted with TLS 1.2 or 1.3. SSL certificates must be managed and renewed automatically (Let's Encrypt, Azure Certificate Manager). Plain HTTP must be redirected to HTTPS.

> **Rationale:** Data transmitted unencrypted can be intercepted at any point in the network. TLS is the minimum standard and is mandatory for any web service or API.

---

### DAT-04 — Record of processing activities (GDPR Art. 30) `T1`

**NIS2:** — | **GEO 155:** —

The organization must maintain an up-to-date record of personal data processing activities, in accordance with GDPR Art. 30. The record must include the purpose, data categories, retention period, and international transfers.

> **Rationale:** The GDPR Art. 30 record is a legal requirement for organizations with over 250 employees and recommended for all. It is the foundation of GDPR compliance and the basis for DPIA risk assessments.

---

### DAT-05 — Backup policy for cloud resources `T1`

**NIS2:** Art. 21(2)(c) | **GEO 155:** —

All critical cloud resources (databases, VMs, storage) must be included in automated backup policies with defined retention. Backups must be stored in different geographic regions and tested semi-annually.

> **Rationale:** Cloud resources are not immune to data loss — accidental deletion, ransomware, or configuration errors can cause irreversible losses without backup.
