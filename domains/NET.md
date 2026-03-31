# NET — Network & Infrastructure

> Security of the network perimeter, remote access, and cloud infrastructure.

**7 controls** · T1: 6 · T3: 1

---

## Controls

### NET-01 — Perimeter firewall with default-deny rules `T1`

**NIS2:** Art. 21(2)(h) | **GEO 155:** Art. 5(1)(d)

The perimeter firewall must be configured with a default-deny policy for inbound traffic. Only explicitly required ports and services should be open. Rules must be documented and reviewed semi-annually.

> **Rationale:** A properly configured perimeter firewall blocks automated scans and exploitation of inadvertently exposed services.

---

### NET-02 — VPN for remote access `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** —

Remote access to organizational resources must be done exclusively through a VPN with MFA authentication. RDP, SMB, and other management protocols must not be directly exposed to the internet. Zero Trust Network Access (ZTNA) architectures are recommended as a modern alternative.

> **Rationale:** Internet-exposed RDP is the #1 vector for ransomware attacks. VPN with MFA eliminates this critical attack surface.

---

### NET-03 — Protective DNS filtering `T1`

**NIS2:** — | **GEO 155:** —

Deploy a DNS resolver with malicious domain filtering (Cloudflare Gateway, Cisco Umbrella, CERT-RO DNS). All organizational devices must exclusively use the organization's DNS. User modification of DNS settings must be blocked.

> **Rationale:** Protective DNS blocks malware communication with command-and-control (C2) servers and access to phishing domains, even after an initial infection.

---

### NET-04 — Separate guest WiFi network `T1`

**NIS2:** — | **GEO 155:** —

Guests and employees' personal devices must be connected to a separate WiFi network, completely isolated from the corporate network. The guest network must provide internet access only, with no access to internal resources.

> **Rationale:** Mixed WiFi networks (corporate + guests) enable ARP spoofing attacks and pivoting to internal resources. Separation is a simple measure with high impact.

---

### NET-05 — Secure cloud account configuration `T1`

**NIS2:** Art. 21(2)(e) | **GEO 155:** —

Cloud accounts (Azure, AWS, GCP) must be configured according to CIS Benchmarks for the respective provider. Enable cloud security centers (Microsoft Defender for Cloud, AWS Security Hub) for misconfiguration detection.

> **Rationale:** Cloud misconfigurations are the #1 cause of breaches in cloud environments. CIS Benchmarks provide a concrete, verifiable baseline for securing cloud accounts.

---

### NET-06 — Disable public access to cloud storage `T1`

**NIS2:** — | **GEO 155:** —

Cloud storage containers (Azure Blob, AWS S3, Google Cloud Storage) must not be publicly accessible by default. Public access must be disabled at the account level and continuously monitored for accidental re-enablement.

> **Rationale:** Accidentally public S3 buckets and Blob containers are the source of some of the largest data breaches. Disabling public access by default prevents leaks through misconfiguration.

---

### NET-07 — Periodic penetration testing `T3`

**NIS2:** Art. 21(2)(e) | **GEO 155:** Art. 6(1)

Conduct an annual external penetration test and bi-annual internal test, performed by an authorized third-party provider. Critical vulnerabilities identified must be remediated within 30 days, high-severity within 90 days.

> **Rationale:** Penetration tests identify real vulnerabilities before attackers exploit them. They are mandatory for NIS2 organizations in essential sectors.
