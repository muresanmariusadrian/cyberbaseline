# EPT — Endpoint Protection

> Protecția dispozitivelor, patch management și inventarul activelor.

**4 controale** · T1: 4

---

## Controale

### EPT-01 — Soluție EDR pe toate dispozitivele `T1`

**NIS2:** Art. 21(2)(b) | **GEO 155:** Art. 5(1)(c)

Toate dispozitivele gestionate (laptopuri, desktop-uri, servere) trebuie să ruleze o soluție de tip Endpoint Detection & Response (EDR). Acoperirea trebuie monitorizată și menținută la 100%. Alertele critice trebuie investigate în 24 de ore.

> **Rationale:** EDR oferă vizibilitate și capacitate de răspuns la amenințări avansate care depășesc capabilitățile antivirus tradițional. Este componenta de bază a protecției endpoint moderne.

---

### EPT-02 — Patch management automatizat `T1`

**NIS2:** Art. 21(2)(e) | **GEO 155:** Art. 5(1)(e)

Actualizările de securitate critice trebuie aplicate în maximum 72 de ore de la disponibilitate pe toate sistemele. Patch-urile importante trebuie aplicate în 7 zile. Sistemele neactualizate trebuie izolate sau remediate urgent.

> **Rationale:** Exploatarea vulnerabilităților nepatchuite este cauza a peste 60% din breșele de securitate. Patch management-ul automatizat reduce fereastra de expunere la minimum.

---

### EPT-03 — Criptarea completă a discurilor pe laptopuri `T1`

**NIS2:** — | **GEO 155:** —

Toate laptopurile și dispozitivele portabile trebuie să aibă criptarea completă a discului activată (BitLocker pe Windows, FileVault pe macOS). Cheile de recuperare trebuie stocate centralizat în Azure AD sau un vault securizat.

> **Rationale:** Pierderea sau furtul unui laptop necriptat constituie breșă de date raportabilă ANSPDCP. Criptarea discului protejează datele organizației fără a afecta utilizabilitatea.

---

### EPT-04 — Inventarul hardware și software `T1`

**NIS2:** — | **GEO 155:** —

Menținerea unui inventar actualizat al tuturor dispozitivelor hardware și aplicațiilor software din organizație. Descoperire automată prin scanare de rețea. Revizuire lunară pentru identificarea activelor neautorizate.

> **Rationale:** Nu poți proteja ceea ce nu știi că există. Inventarul complet este prerequisitul oricărui program de securitate eficient și baza pentru patch management și monitorizare.
