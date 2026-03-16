# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-16 04:45 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,657,368  
**Davon in bekannten ASN-Ranges:** 731,909

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 110 | 194,240 | 63980.9 | +0 | +257 | 827 |
| 2 | AS132203 | Tencent Cloud | CN | 🔴 105 | 22,646 | 9468.1 | +0 | +6 | 1050 |
| 3 | AS51167 | Contabo | DE | 🔴 103 | 11,634 | 24779.3 | +0 | +1 | 567 |
| 4 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 31,649 | 3323.4 | +0 | +0 | 877 |
| 5 | AS20473 | Vultr | US | 🟠 95 | 17,002 | 12418.5 | +0 | +0 | 1453 |
| 6 | AS22612 | Namecheap | US | 🟠 90 | 1,606 | 10481.9 | +0 | +0 | 312 |
| 7 | AS12389 | Rostelecom | RU | 🟠 85 | 13,722 | 797.1 | +0 | +0 | 3183 |
| 8 | AS31898 | Oracle Cloud | US | 🟠 85 | 24,584 | 5182.5 | +0 | +6 | 1971 |
| 9 | AS16509 | Amazon AWS | US | 🟠 85 | 289,499 | 1519.2 | +0 | +20 | 14341 |
| 10 | AS16276 | OVH | FR | 🟠 84 | 38,344 | 8436.5 | +0 | +3 | 600 |
| 11 | AS24940 | Hetzner | DE | 🟠 81 | 22,420 | 7976.1 | +0 | +2 | 82 |
| 12 | AS12876 | Scaleway | FR | 🟠 80 | 8,133 | 14265.6 | +0 | +0 | 22 |
| 13 | AS47583 | Hostinger | LT | 🟠 78 | 2,802 | 3531.9 | +0 | +1 | 860 |
| 14 | AS8560 | IONOS | DE | 🟠 71 | 3,157 | 3702.2 | +0 | +2 | 462 |
| 15 | AS63949 | Linode (Akamai) | US | 🟠 70 | 9,915 | 7816.4 | +0 | +0 | 341 |
| 16 | AS26496 | GoDaddy | US | 🟡 65 | 1,940 | 1553.8 | +0 | +0 | 184 |
| 17 | AS8075 | Microsoft Azure | US | 🟡 61 | 36,516 | 550.0 | +0 | +2 | 931 |
| 18 | AS46606 | Bluehost (Unified Layer) | US | 🟡 60 | 898 | 1042.8 | +0 | +0 | 285 |
| 19 | AS36351 | IBM Cloud | US | 🟡 50 | 1,202 | 294.9 | +0 | +0 | 328 |

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
*Generiert: 2026-03-16 04:45 UTC*