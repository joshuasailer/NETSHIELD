# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-13 04:18 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,112,983  
**Davon in bekannten ASN-Ranges:** 686,547

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 106 | 180,880 | 59580.3 | +0 | +2 | 827 |
| 2 | AS51167 | Contabo | DE | 🔴 100 | 10,523 | 22413.0 | +0 | +0 | 567 |
| 3 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 29,113 | 3057.1 | +0 | +0 | 877 |
| 4 | AS132203 | Tencent Cloud | CN | 🟠 95 | 18,549 | 7755.2 | +0 | +0 | 1050 |
| 5 | AS20473 | Vultr | US | 🟠 95 | 16,164 | 11806.4 | +0 | +0 | 1453 |
| 6 | AS12389 | Rostelecom | RU | 🟠 85 | 10,259 | 596.0 | +0 | +0 | 3183 |
| 7 | AS16509 | Amazon AWS | US | 🟠 81 | 281,496 | 1477.2 | +0 | +2 | 14341 |
| 8 | AS12876 | Scaleway | FR | 🟠 80 | 7,692 | 13492.1 | +0 | +0 | 22 |
| 9 | AS24940 | Hetzner | DE | 🟠 75 | 20,877 | 7427.2 | +0 | +0 | 82 |
| 10 | AS16276 | OVH | FR | 🟠 75 | 35,070 | 7716.1 | +0 | +0 | 600 |
| 11 | AS47583 | Hostinger | LT | 🟠 75 | 2,119 | 2671.0 | +0 | +0 | 860 |
| 12 | AS22612 | Namecheap | US | 🟠 75 | 1,465 | 9561.7 | +0 | +0 | 312 |
| 13 | AS31898 | Oracle Cloud | US | 🟠 75 | 24,351 | 5133.4 | +0 | +0 | 1971 |
| 14 | AS63949 | Linode (Akamai) | US | 🟠 70 | 8,170 | 6440.8 | +0 | +0 | 341 |
| 15 | AS26496 | GoDaddy | US | 🟡 65 | 1,535 | 1229.5 | +0 | +0 | 184 |
| 16 | AS8560 | IONOS | DE | 🟡 65 | 2,866 | 3360.9 | +0 | +0 | 462 |
| 17 | AS46606 | Bluehost (Unified Layer) | US | 🟡 60 | 937 | 1088.0 | +0 | +0 | 285 |
| 18 | AS8075 | Microsoft Azure | US | 🟡 55 | 33,332 | 502.0 | +0 | +0 | 931 |
| 19 | AS36351 | IBM Cloud | US | 🟡 50 | 1,149 | 281.9 | +0 | +0 | 328 |

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
*Generiert: 2026-03-13 04:18 UTC*