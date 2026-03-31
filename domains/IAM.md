# IAM — Identity & Access Management

> Management of user identities, access rights, and credentials across systems and data.

**6 controls** · T1: 5 · T2: 1

---

## Controls

### IAM-01 — Multi-factor authentication for privileged accounts `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** Art. 5(1)(a)

All accounts with administrative privileges (system, IT, cloud administrators) must use multi-factor authentication (MFA/2FA). The second factor can be a TOTP app (Google Authenticator, Microsoft Authenticator) or a FIDO2 hardware token.

> **Rationale:** Compromised privileged accounts without MFA is the primary attack vector in SMB breaches. MFA blocks over 99% of automated credential stuffing attacks.

---

### IAM-02 — Strong password policy `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** —

All user accounts must use passwords with a minimum of 12 characters, avoiding passwords from known breach lists. Using an organizational password manager (Bitwarden Teams, 1Password Business) is recommended over forced periodic rotation.

> **Rationale:** Weak or reused passwords are the #1 attack vector in SMB breaches. A password manager eliminates reuse and simplifies policy enforcement.

---

### IAM-03 — Least privilege principle `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** Art. 5(1)(b)

Users must have only the permissions necessary for their job duties. Administrative accounts should be separate from day-to-day accounts. Quarterly access reviews and immediate revocation upon role change or departure.

> **Rationale:** Excessive access amplifies the impact of a compromised account. Least privilege is one of the most effective measures for limiting lateral movement.

---

### IAM-04 — Disable inactive accounts `T1`

**NIS2:** — | **GEO 155:** —

User accounts inactive for more than 30 days must be automatically disabled. Former employee accounts must be revoked on their last day. The process must be integrated with the HR offboarding procedure.

> **Rationale:** Abandoned accounts are a frequent entry point for attackers. Automated deactivation eliminates dependency on error-prone manual processes.

---

### IAM-05 — Periodic access rights review `T2`

**NIS2:** Art. 21(2)(i) | **GEO 155:** Art. 5(2)

Formal quarterly review of all privileged access and semi-annual review of standard access. The process must be documented and approved by line managers, not IT.

> **Rationale:** Privilege creep over time is a major risk in organizations with staff turnover. Periodic reviews keep the least privilege principle operational.

---

### IAM-06 — Secrets and credentials management with a vault `T1`

**NIS2:** — | **GEO 155:** —

Credentials, API keys, database connection strings, and other secrets must not be hard-coded in source code or stored in plaintext environment variables. A vault service must be used (Azure Key Vault, AWS Secrets Manager, HashiCorp Vault).

> **Rationale:** Secrets in source code or environment variables are frequently exposed through public repositories or unauthorized access. A centralized vault provides rotation, auditing, and granular access control.
