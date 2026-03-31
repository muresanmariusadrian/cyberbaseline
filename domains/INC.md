# INC — Incident Management

> Incident response, NIS2 notification, logging, and digital forensics.

**5 controls** · T1: 2 · T2: 2 · T3: 1

---

## Controls

### INC-01 — Documented incident response plan `T1`

**NIS2:** Art. 21(2)(c) | **GEO 155:** Art. 7(1)

The organization must have a documented cybersecurity incident response plan with defined roles and responsibilities, escalation procedures, external contacts (CERT-RO, ANSSI, IR providers), and incident classification criteria.

> **Rationale:** Organizations without a response plan take on average 3x longer to contain an incident. A documented plan turns the inevitable chaos of an incident into coordinated actions.

---

### INC-02 — NIS2 incident notification within 24/72 hours `T1`

**NIS2:** Art. 23(4) | **GEO 155:** Art. 9(1)

NIS2 organizations must notify DNSC (National Directorate of Cyber Security) within 24 hours of detecting a significant incident (preliminary notification) and within 72 hours with full details. The notification procedure must be documented.

> **Rationale:** NIS2 notification deadlines are legally mandatory. Non-compliance carries significant fines. A pre-documented procedure ensures notification happens on time, even under crisis conditions.

---

### INC-03 — Centralized logging and SIEM `T2`

**NIS2:** Art. 21(2)(b) | **GEO 155:** —

Logs from all critical systems (AD, firewall, endpoint, cloud, applications) must be centrally collected in a SIEM (Microsoft Sentinel, Splunk, Elastic SIEM). Minimum 12-month retention, automatic alerting for security events.

> **Rationale:** Without centralized logging, incident investigation is slow and incomplete. SIEM reduces mean time to detect (MTTD) and provides the basis for proactive alerting.

---

### INC-04 — Capability to isolate compromised systems `T2`

**NIS2:** Art. 21(2)(c) | **GEO 155:** —

Documented and tested procedures for rapidly isolating compromised systems or network segments. Isolation capability within 30 minutes of the decision. Out-of-band access for post-isolation administration.

> **Rationale:** Isolation speed is the most critical factor in limiting ransomware propagation. Every minute of delay allows more systems to be encrypted.

---

### INC-05 — Digital forensics capability `T3`

**NIS2:** Art. 21(2)(c) | **GEO 155:** —

The organization must have access to digital forensics capabilities, either internally (training, tools) or through a contract with an IR provider. Evidence collection and preservation processes must be documented.

> **Rationale:** Digital forensics is necessary for fully understanding an incident, identifying the attack vector, and preventing recurrence. Without it, the same vulnerabilities remain exploitable.
