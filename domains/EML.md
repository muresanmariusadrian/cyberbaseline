# EML — Email Security

> Securitatea comunicațiilor email și protecția împotriva phishing și BEC.

**4 controale** · T1: 4

---

## Controale

### EML-01 — Configurare SPF, DKIM și DMARC `T1`

**NIS2:** Art. 21(2)(h) | **GEO 155:** —

Domeniul de email al organizației trebuie să aibă configurate înregistrările DNS SPF, DKIM și DMARC cu politică minimă `quarantine`. Politica DMARC trebuie monitorizată prin rapoarte agregate (RUA) pentru a detecta utilizarea neautorizată a domeniului.

> **Rationale:** SPF/DKIM/DMARC previn spoofing-ul de domeniu utilizat în atacuri BEC (Business Email Compromise) și phishing. Configurarea corectă este o măsură cu impact ridicat și cost scăzut.

---

### EML-02 — Filtrare anti-phishing și anti-malware `T1`

**NIS2:** Art. 21(2)(b) | **GEO 155:** Art. 5(1)(c)

Implementarea unui gateway de email cu capacități avansate de filtrare anti-phishing, detecție URL malițioase și sandbox pentru atașamente (Microsoft Defender for Office 365, Proofpoint, Mimecast). Filtrarea trebuie activată pentru toți utilizatorii.

> **Rationale:** Peste 90% din incidentele de securitate încep cu un email malițios. Un gateway de email modern blochează amenințările înainte să ajungă la utilizatori.

---

### EML-03 — Marcarea emailurilor externe `T1`

**NIS2:** — | **GEO 155:** —

Toate emailurile provenite din afara organizației trebuie marcate vizibil cu un banner sau prefix de subiect (ex: `[EXTERN]`) pentru a alerta utilizatorii la tentative de impersonare a colegilor sau conducerii.

> **Rationale:** Atacurile BEC exploatează dificultatea utilizatorilor de a distinge emailurile interne de cele externe. Marcarea vizibilă reduce semnificativ eficiența acestor atacuri.

---

### EML-04 — Dezactivarea macro-urilor Office în emailuri `T1`

**NIS2:** Art. 21(2)(b) | **GEO 155:** —

Macro-urile din documentele Office primite prin email trebuie dezactivate implicit prin Group Policy sau Intune. Excepțiile necesită aprobare IT și trebuie limitate la surse de încredere verificate.

> **Rationale:** Macro-urile malițioase în documente Office sunt un vector de livrare malware extrem de frecvent. Dezactivarea lor implicit elimină o clasă întreagă de atacuri.
