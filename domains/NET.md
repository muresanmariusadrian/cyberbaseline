# NET — Rețea & Infrastructură

> Securitatea rețelei, perimetrului, accesului remote și infrastructurii cloud.

**7 controale** · T1: 6 · T3: 1

---

## Controale

### NET-01 — Firewall perimetral cu reguli implicite de blocare `T1`

**NIS2:** Art. 21(2)(h) | **GEO 155:** Art. 5(1)(d)

Firewall-ul perimetral trebuie configurat cu politică default-deny pentru traficul inbound. Doar porturile și serviciile explicit necesare trebuie deschise. Regulile trebuie documentate și revizuite semestrial.

> **Rationale:** Un firewall perimetral corect configurat blochează scanările automate și exploatarea serviciilor expuse inadvertent pe internet.

---

### NET-02 — VPN pentru acces remote `T1`

**NIS2:** Art. 21(2)(i) | **GEO 155:** —

Accesul remote la resursele organizației trebuie realizat exclusiv prin VPN cu autentificare MFA. RDP, SMB și alte protocoale de management nu trebuie expuse direct pe internet. Se recomandă arhitecturi Zero Trust Network Access (ZTNA) ca alternativă modernă.

> **Rationale:** RDP expus pe internet este vectorul #1 pentru atacuri ransomware. VPN-ul cu MFA elimină această suprafață de atac critică.

---

### NET-03 — Filtrare DNS protectivă `T1`

**NIS2:** — | **GEO 155:** —

Implementarea unui resolver DNS cu filtrare a domeniilor malițioase (Cloudflare Gateway, Cisco Umbrella, CERT-RO DNS). Toate dispozitivele organizației trebuie să folosească exclusiv DNS-ul organizației. Modificarea DNS de către utilizatori trebuie blocată.

> **Rationale:** DNS protectiv blochează comunicațiile malware cu serverele de comandă și control (C2) și accesul la domenii phishing, chiar după infecția inițială.

---

### NET-04 — Rețea WiFi separată pentru oaspeți `T1`

**NIS2:** — | **GEO 155:** —

Oaspeții și dispozitivele personale ale angajaților trebuie conectați la o rețea WiFi separată, izolată complet de rețeaua corporativă. Rețeaua de oaspeți trebuie să ofere acces doar la internet, fără acces la resurse interne.

> **Rationale:** Rețelele WiFi mixte (corporative + oaspeți) permit atacuri de tip ARP spoofing și pivot spre resursele interne. Separarea este o măsură simplă cu impact mare.

---

### NET-05 — Configurare securizată a conturilor cloud `T1`

**NIS2:** Art. 21(2)(e) | **GEO 155:** —

Conturile cloud (Azure, AWS, GCP) trebuie configurate conform CIS Benchmarks pentru furnizorul respectiv. Activarea centrului de securitate cloud (Microsoft Defender for Cloud, AWS Security Hub) pentru detectarea configurărilor greșite.

> **Rationale:** Configurările greșite cloud sunt cauza #1 a breșelor în mediile cloud. CIS Benchmarks oferă un baseline concret și verificabil pentru securizarea conturilor cloud.

---

### NET-06 — Dezactivarea accesului public la storage cloud `T1`

**NIS2:** — | **GEO 155:** —

Containerele de storage cloud (Azure Blob, AWS S3, Google Cloud Storage) nu trebuie să fie accesibile public implicit. Accesul public trebuie dezactivat la nivel de cont și monitorizat continuu pentru reactivare accidentală.

> **Rationale:** Bucket-urile S3 și containerele Blob publice accidental sunt sursa unor dintre cele mai mari breșe de date. Dezactivarea implicită a accesului public previne scurgerile prin configurare greșită.

---

### NET-07 — Testare de penetrare periodică `T3`

**NIS2:** Art. 21(2)(e) | **GEO 155:** Art. 6(1)

Efectuarea unui test de penetrare extern anual și intern bianual, realizat de un furnizor terț autorizat. Vulnerabilitățile critice identificate trebuie remediate în 30 de zile, cele înalte în 90 de zile.

> **Rationale:** Testele de penetrare identifică vulnerabilități reale înainte ca atacatorii să le exploateze. Sunt obligatorii pentru organizațiile NIS2 din sectoare esențiale.
