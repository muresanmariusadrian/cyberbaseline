# INC — Incident Management

> Răspuns la incidente, notificare NIS2, logging și investigare criminalistică.

**5 controale** · T1: 2 · T2: 2 · T3: 1

---

## Controale

### INC-01 — Plan documentat de răspuns la incidente `T1`

**NIS2:** Art. 21(2)(c) | **GEO 155:** Art. 7(1)

Organizația trebuie să aibă un plan documentat de răspuns la incidente de securitate cibernetică, cu roluri și responsabilități definite, proceduri de escaladare, contacte externe (CERT-RO, ANSSI, furnizori IR) și criterii de clasificare a incidentelor.

> **Rationale:** Organizațiile fără plan de răspuns pierd în medie 3x mai mult timp să conțină un incident. Planul documentat transformă haosul inevitabil al unui incident în acțiuni coordonate.

---

### INC-02 — Notificarea incidentelor NIS2 în 24/72 ore `T1`

**NIS2:** Art. 23(4) | **GEO 155:** Art. 9(1)

Organizațiile NIS2 trebuie să notifice DNSC (Directoratul Național de Securitate Cibernetică) în maximum 24 ore de la detectarea unui incident semnificativ (notificare preliminară) și în 72 ore cu detalii complete. Procedura de notificare trebuie documentată.

> **Rationale:** Termenele de notificare NIS2 sunt obligatorii legal. Nerespectarea lor atrage amenzi semnificative. Procedura pre-documentată asigură că notificarea se face în timp, chiar în condiții de criză.

---

### INC-03 — Logging centralizat și SIEM `T2`

**NIS2:** Art. 21(2)(b) | **GEO 155:** —

Logurile din toate sistemele critice (AD, firewall, endpoint, cloud, aplicații) trebuie colectate centralizat într-un SIEM (Microsoft Sentinel, Splunk, Elastic SIEM). Retenție minimum 12 luni, alertare automată pentru evenimentele de securitate.

> **Rationale:** Fără logging centralizat, investigarea incidentelor este lentă și incompletă. SIEM reduce timpul mediu de detecție (MTTD) și oferă baza pentru alertare proactivă.

---

### INC-04 — Capacitate de izolare a sistemelor compromise `T2`

**NIS2:** Art. 21(2)(c) | **GEO 155:** —

Proceduri documentate și testate pentru izolarea rapidă a sistemelor sau segmentelor de rețea compromise. Capabilitate de izolare în maximum 30 minute de la decizie. Acces out-of-band pentru administrare post-izolare.

> **Rationale:** Viteza de izolare este factorul cel mai critic în limitarea propagării ransomware. Fiecare minut de întârziere permite criptarea mai multor sisteme.

---

### INC-05 — Investigare criminalistică digitală (forensics) `T3`

**NIS2:** Art. 21(2)(c) | **GEO 155:** —

Organizația trebuie să aibă acces la capabilități de investigare criminalistică digitală, fie intern (instruire, instrumente) fie prin contract cu un furnizor IR. Procesele de colectare și prezervare a dovezilor digitale trebuie documentate.

> **Rationale:** Investigarea criminalistică este necesară pentru înțelegerea completă a unui incident, identificarea vectorului de atac și prevenirea recidivei. Fără ea, aceleași vulnerabilități rămân exploatabile.
