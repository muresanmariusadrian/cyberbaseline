# IAM — Identity & Access Management

> Gestionarea identităților, accesului și secretelor utilizatorilor la sisteme și date.

**6 controale** · T1: 5 · T2: 1

---

## Controale

### IAM-01 — Autentificare multifactor pentru conturi privilegiate `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** Art. 5(1)(a)

Toate conturile cu privilegii administrative (administratori de sistem, IT, cloud) trebuie să utilizeze autentificare multifactor (MFA/2FA). Factorul suplimentar poate fi o aplicație TOTP (Google Authenticator, Microsoft Authenticator) sau un token hardware FIDO2.

> **Rationale:** Compromiterea conturilor privilegiate fără MFA este vectorul principal de atac în breșele care afectează IMM-urile. MFA blochează peste 99% din atacurile automate de credential stuffing.

---

### IAM-02 — Politică de parole complexe `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** —

Toate conturile de utilizator trebuie să folosească parole cu minimum 12 caractere, evitând parolele din liste de breșe cunoscute. Se recomandă implementarea unui manager de parole organizațional (Bitwarden Teams, 1Password Business) în locul rotației forțate periodice.

> **Rationale:** Parolele slabe sau reutilizate reprezintă vectorul de atac #1 în breșele care afectează IMM-urile. Un manager de parole elimină reutilizarea și simplifică respectarea politicii.

---

### IAM-03 — Principiul privilegiului minim `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** Art. 5(1)(b)

Utilizatorii trebuie să aibă doar permisiunile necesare pentru sarcinile de serviciu. Conturile administrative separate de cele de zi cu zi, revizuire trimestrială a accesurilor, revocare imediată la schimbarea rolului sau plecarea din organizație.

> **Rationale:** Accesul excesiv amplifică impactul unui cont compromis. Principiul least privilege este una din cele mai eficiente măsuri de limitare a propagării laterale.

---

### IAM-04 — Dezactivarea conturilor inactive `T1`

**NIS2:** — | **GEO 155:** —

Conturile de utilizator inactive mai mult de 30 de zile trebuie dezactivate automat. Conturile foștilor angajați trebuie revocate în ziua plecării. Procesul trebuie integrat cu procedura de offboarding HR.

> **Rationale:** Conturile abandonate sunt o poartă de intrare frecventă pentru atacatori. Automatizarea dezactivării elimină dependența de procese manuale eronate.

---

### IAM-05 — Revizuirea periodică a drepturilor de acces `T2`

**NIS2:** Art. 21(2)(i) | **GEO 155:** Art. 5(2)

Revizuire formală trimestrială a tuturor accesurilor privilegiate și semestrială pentru accesurile standard. Procesul trebuie documentat și aprobat de manageri de linie, nu de IT.

> **Rationale:** Acumularea de privilegii în timp (privilege creep) este un risc major în organizații cu fluctuație de personal. Revizuirile periodice mențin principiul least privilege operațional.

---

### IAM-06 — Gestionarea secretelor și credențialelor cu vault `T1`

**NIS2:** — | **GEO 155:** —

Credențialele, cheile API, șirurile de conexiune la baze de date și alte secrete nu trebuie hard-codate în cod sau stocate în variabile de mediu text clar. Trebuie utilizat un serviciu de vault (Azure Key Vault, AWS Secrets Manager, HashiCorp Vault).

> **Rationale:** Secretele în cod sursă sau variabile de mediu sunt expuse frecvent prin repository-uri publice sau acces neautorizat. Un vault centralizat oferă rotație, audit și acces granular.
