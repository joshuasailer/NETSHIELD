# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-15 04:37 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,215,709  
**Davon in bekannten ASN-Ranges:** 693,488

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 106 | 185,489 | 61098.4 | +0 | +2 | 827 |
| 2 | AS51167 | Contabo | DE | 🔴 100 | 10,815 | 23035.0 | +0 | +0 | 567 |
| 3 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 29,260 | 3072.5 | +0 | +0 | 877 |
| 4 | AS132203 | Tencent Cloud | CN | 🟠 95 | 17,605 | 7360.5 | +0 | +0 | 1050 |
| 5 | AS20473 | Vultr | US | 🟠 95 | 16,383 | 11966.4 | +0 | +0 | 1453 |
| 6 | AS12389 | Rostelecom | RU | 🟠 85 | 10,245 | 595.1 | +0 | +0 | 3183 |
| 7 | AS16509 | Amazon AWS | US | 🟠 81 | 282,819 | 1484.1 | +0 | +2 | 14341 |
| 8 | AS12876 | Scaleway | FR | 🟠 80 | 7,415 | 13006.2 | +0 | +0 | 22 |
| 9 | AS24940 | Hetzner | DE | 🟠 75 | 21,239 | 7556.0 | +0 | +0 | 82 |
| 10 | AS16276 | OVH | FR | 🟠 75 | 35,006 | 7702.1 | +0 | +0 | 600 |
| 11 | AS47583 | Hostinger | LT | 🟠 75 | 2,521 | 3177.7 | +0 | +0 | 860 |
| 12 | AS22612 | Namecheap | US | 🟠 75 | 1,531 | 9992.4 | +0 | +0 | 312 |
| 13 | AS31898 | Oracle Cloud | US | 🟠 75 | 24,506 | 5166.0 | +0 | +0 | 1971 |
| 14 | AS63949 | Linode (Akamai) | US | 🟠 70 | 8,316 | 6555.9 | +0 | +0 | 341 |
| 15 | AS26496 | GoDaddy | US | 🟡 65 | 1,803 | 1444.1 | +0 | +0 | 184 |
| 16 | AS8560 | IONOS | DE | 🟡 65 | 2,815 | 3301.1 | +0 | +0 | 462 |
| 17 | AS8075 | Microsoft Azure | US | 🟡 55 | 33,703 | 507.6 | +0 | +0 | 931 |
| 18 | AS36351 | IBM Cloud | US | 🟡 50 | 1,162 | 285.1 | +0 | +0 | 328 |
| 19 | AS46606 | Bluehost (Unified Layer) | US | ⚪ 45 | 855 | 992.8 | +0 | +0 | 285 |

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
*Generiert: 2026-03-15 04:37 UTC*