# DAT — Data Protection

> Protecția, clasificarea, backup-ul și guvernanța datelor organizației.

**5 controale** · T1: 5

---

## Controale

### DAT-01 — Clasificarea datelor organizației `T1`

**NIS2:** — | **GEO 155:** —

Toate datele gestionate de organizație trebuie clasificate în categorii (Public, Intern, Confidențial, Secret) cu politici clare de gestionare pentru fiecare categorie. Clasificarea trebuie documentată și comunicată angajaților.

> **Rationale:** Fără clasificare, organizația nu știe ce date trebuie protejate cel mai strict. Clasificarea este fundația pe care se construiesc toate celelalte controale de protecție a datelor.

---

### DAT-02 — Backup 3-2-1 pentru date critice `T1`

**NIS2:** Art. 21(2)(c) | **GEO 155:** Art. 5(1)(f)

Datele critice trebuie să urmeze regula 3-2-1: minim 3 copii, pe 2 medii diferite, cu 1 copie off-site sau în cloud. Backup-urile trebuie testate prin restaurare completă cel puțin trimestrial și protejate împotriva ransomware prin copii imutabile.

> **Rationale:** Backup-ul este ultima linie de apărare împotriva ransomware. Copiile imutabile off-site fac recuperarea posibilă chiar dacă toate sistemele locale sunt criptate.

---

### DAT-03 — Criptarea datelor în tranzit (TLS) `T1`

**NIS2:** Art. 21(2)(h) | **GEO 155:** —

Tot traficul de rețea care conține date sensibile trebuie criptat cu TLS 1.2 sau 1.3. Certificatele SSL trebuie gestionate și reînnoite automat (Let's Encrypt, Azure Certificate Manager). HTTP plain trebuie redirecționat la HTTPS.

> **Rationale:** Datele transmise necriptat pot fi interceptate în orice punct al rețelei. TLS este standardul minim și este obligatoriu pentru orice serviciu web sau API.

---

### DAT-04 — Registrul activităților de prelucrare (GDPR Art. 30) `T1`

**NIS2:** — | **GEO 155:** —

Organizația trebuie să mențină un registru actualizat al activităților de prelucrare a datelor cu caracter personal, conform GDPR Art. 30. Registrul trebuie să includă scopul, categoriile de date, termenul de retenție și transferurile internaționale.

> **Rationale:** Registrul GDPR Art. 30 este obligatoriu legal pentru organizațiile cu peste 250 angajați și recomandat pentru toate. Este fundamentul conformității GDPR și baza pentru evaluările de risc DPIA.

---

### DAT-05 — Politică de backup pentru resursele cloud `T1`

**NIS2:** Art. 21(2)(c) | **GEO 155:** —

Toate resursele cloud critice (baze de date, VM-uri, storage) trebuie incluse în politici de backup automat cu retention definit. Backup-urile trebuie stocate în regiuni geografice diferite și testate semestrial.

> **Rationale:** Resursele cloud nu sunt ferite de pierderea de date — ștergere accidentală, ransomware sau erori de configurare pot cauza pierderi ireversibile fără backup.
