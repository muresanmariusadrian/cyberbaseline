# CyberBaseline

**Standardul de securitate cibernetică pentru IMM-uri din România**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![NIS2](https://img.shields.io/badge/NIS2-aliniat-blue)](https://eur-lex.europa.eu/legal-content/RO/TXT/?uri=CELEX:32022L2555)
[![GEO 155/2024](https://img.shields.io/badge/GEO%20155%2F2024-aliniat-blue)](https://legislatie.just.ro)

Un framework open-source de securitate cibernetică conceput pentru organizații fără echipe dedicate de securitate. **31 de controale practice**, organizate în **6 domenii** și **3 niveluri de maturitate**, aliniate la NIS2 și GEO 155/2024.

**Website:** [cyberbaseline.ro](https://cyberbaseline.ro) *(în curând)*

---

## De ce CyberBaseline?

80% din riscul de breșă provine din 20% din controale. Pentru IMM-urile din România, amenințările principale sunt:

1. **Phishing și BEC** — prin email
2. **Ransomware** — prin endpoint sau RDP expus
3. **Compromiterea credențialelor** — parole slabe, fără MFA
4. **Servicii expuse** — RDP, SMB, porturi de management deschise pe internet

CyberBaseline este construit în jurul acestor amenințări reale, nu al unei taxonomii academice exhaustive.

---

## Structura framework-ului

### Domenii de control

| Abbr | Domeniu | Controale |
|------|---------|-----------|
| [IAM](domains/IAM.md) | Identity & Access Management | 6 |
| [EML](domains/EML.md) | Email Security | 4 |
| [NET](domains/NET.md) | Rețea & Infrastructură | 7 |
| [EPT](domains/EPT.md) | Endpoint Protection | 4 |
| [DAT](domains/DAT.md) | Data Protection | 5 |
| [INC](domains/INC.md) | Incident Management | 5 |

**Total: 31 controale**

### Niveluri de maturitate

| Nivel | Label | Controale | Descriere |
|-------|-------|-----------|-----------|
| T1 | **Esențial** | 26 | Controale de bază, obligatorii pentru conformitate NIS2 minimă. Implementabile rapid, cu impact imediat. |
| T2 | **Avansat** | 3 | Controale recomandate pentru organizații cu risc moderat sau date sensibile. |
| T3 | **Rezistent** | 2 | Controale pentru organizații din sectoare esențiale sau critice conform NIS2. |

---

## Conformitate NIS2 și GEO 155/2024

Toate controalele sunt mapate la articolele relevante din:
- **Directiva NIS2** (UE 2022/2555)
- **GEO 155/2024** — transpunerea NIS2 în legislația română

Organizațiile din sectoare esențiale (energie, transport, sănătate, financiar, apă, infrastructură digitală) și importante (servicii poștale, gestionarea deșeurilor, producție, servicii digitale) au obligații legale de conformitate.

---

## Cum să folosești framework-ul

### 1. Evaluează nivelul actual
Parcurge controalele T1 și bifează ce ai implementat deja. Majoritatea IMM-urilor implementează 40-60% din T1 fără să știe.

### 2. Prioritizează pe baza riscului
Începe cu:
- **IAM-01** (MFA pentru admini) — impact maxim, efort minim
- **EPT-02** (patch management) — elimină 60%+ din vectorii de atac
- **DAT-02** (backup 3-2-1) — protecție împotriva ransomware
- **EML-01** (SPF/DKIM/DMARC) — oprește spoofing-ul de domeniu

### 3. Documentează implementarea
Fiecare control are criterii clare. Documentează ce ai implementat, când și cum — util pentru audituri și notificări NIS2.

### 4. Extinde la T2 și T3
Odată cu implementarea completă T1, evaluează controalele T2 în funcție de profilul de risc al organizației.

---

## Fișiere

| Fișier | Conținut |
|--------|----------|
| [`controls.json`](controls.json) | Toate controalele în format JSON (sursă de adevăr) |
| [`domains/IAM.md`](domains/IAM.md) | Identity & Access Management |
| [`domains/EML.md`](domains/EML.md) | Email Security |
| [`domains/NET.md`](domains/NET.md) | Rețea & Infrastructură |
| [`domains/EPT.md`](domains/EPT.md) | Endpoint Protection |
| [`domains/DAT.md`](domains/DAT.md) | Data Protection |
| [`domains/INC.md`](domains/INC.md) | Incident Management |

---

## Contribuții

Contribuțiile sunt binevenite — în special:
- Corecturi sau clarificări ale descrierilor de controale
- Mapări suplimentare NIS2 / GEO 155
- Traduceri în engleză
- Exemple practice de implementare

Deschide un **Issue** pentru discuții sau un **Pull Request** pentru modificări directe.

---

## Licență

CyberBaseline este licențiat sub [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

Poți folosi, adapta și redistribui liber, cu condiția să menționezi sursa.
