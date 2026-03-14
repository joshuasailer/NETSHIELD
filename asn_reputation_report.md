# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-14 04:16 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,256,013  
**Davon in bekannten ASN-Ranges:** 696,713

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 109 | 184,840 | 60884.7 | +0 | +3 | 827 |
| 2 | AS51167 | Contabo | DE | 🔴 100 | 10,816 | 23037.1 | +0 | +0 | 567 |
| 3 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 29,263 | 3072.8 | +0 | +0 | 877 |
| 4 | AS132203 | Tencent Cloud | CN | 🟠 95 | 18,635 | 7791.2 | +0 | +0 | 1050 |
| 5 | AS20473 | Vultr | US | 🟠 95 | 16,393 | 11973.7 | +0 | +0 | 1453 |
| 6 | AS22612 | Namecheap | US | 🟠 90 | 1,539 | 10044.6 | +0 | +0 | 312 |
| 7 | AS12389 | Rostelecom | RU | 🟠 85 | 10,471 | 608.3 | +0 | +0 | 3183 |
| 8 | AS16509 | Amazon AWS | US | 🟠 81 | 283,250 | 1486.4 | +0 | +2 | 14341 |
| 9 | AS12876 | Scaleway | FR | 🟠 80 | 7,909 | 13872.7 | +0 | +0 | 22 |
| 10 | AS24940 | Hetzner | DE | 🟠 75 | 21,338 | 7591.2 | +0 | +0 | 82 |
| 11 | AS16276 | OVH | FR | 🟠 75 | 36,075 | 7937.2 | +0 | +0 | 600 |
| 12 | AS47583 | Hostinger | LT | 🟠 75 | 2,581 | 3253.3 | +0 | +0 | 860 |
| 13 | AS31898 | Oracle Cloud | US | 🟠 75 | 24,468 | 5158.0 | +0 | +0 | 1971 |
| 14 | AS63949 | Linode (Akamai) | US | 🟠 70 | 8,408 | 6628.4 | +0 | +0 | 341 |
| 15 | AS26496 | GoDaddy | US | 🟡 65 | 1,816 | 1454.5 | +0 | +0 | 184 |
| 16 | AS8560 | IONOS | DE | 🟡 65 | 2,959 | 3470.0 | +0 | +0 | 462 |
| 17 | AS46606 | Bluehost (Unified Layer) | US | 🟡 60 | 997 | 1157.7 | +0 | +0 | 285 |
| 18 | AS8075 | Microsoft Azure | US | 🟡 55 | 33,793 | 509.0 | +0 | +0 | 931 |
| 19 | AS36351 | IBM Cloud | US | 🟡 50 | 1,162 | 285.1 | +0 | +0 | 328 |

---

### Score-Formel (normalisiert auf ASN-Größe)
```
score = A (Abuse-Dichte) + B (Absolute Präsenz) + C (Feed-Bonus) + D (Basis-Reputation)
A: BL-Hits pro 1M IPs im ASN  → max 60
B: Absolute BL-Treffer-Stufe   → max 20
C: Spamhaus DROP + ET-Bonus    → max 10
D: Basis-Reputation (RU/CN++)  → max 40
```
- **Abuse-Dichte**: verhindert dass große Netze (AWS) kleine (Contabo) verdrängen
- **Absolute Präsenz**: große Netze mit viel Abuse bleiben trotzdem trackbar
- **Feed-Bonus**: IPs auch in Spamhaus DROP oder Emerging Threats

---
*Datenquelle: [ScaniteX ASN Database](https://scanitex.com/en/resources/asn-database) (BGP via RIPE Stat, kein API-Key)*  
*Generiert: 2026-03-14 04:16 UTC*