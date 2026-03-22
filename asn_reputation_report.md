# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-22 04:25 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,622,923  
**Davon in bekannten ASN-Ranges:** 790,842

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 110 | 207,890 | 68477.1 | +0 | +256 | 827 |
| 2 | AS132203 | Tencent Cloud | CN | 🔴 104 | 22,750 | 9511.6 | +0 | +3 | 1050 |
| 3 | AS51167 | Contabo | DE | 🔴 103 | 11,891 | 25326.7 | +0 | +1 | 567 |
| 4 | AS12389 | Rostelecom | RU | 🔴 100 | 52,917 | 3074.0 | +0 | +0 | 3183 |
| 5 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 32,098 | 3370.5 | +0 | +0 | 877 |
| 6 | AS20473 | Vultr | US | 🟠 95 | 17,364 | 12682.9 | +0 | +0 | 1453 |
| 7 | AS22612 | Namecheap | US | 🟠 90 | 1,616 | 10547.2 | +0 | +0 | 312 |
| 8 | AS31898 | Oracle Cloud | US | 🟠 85 | 24,873 | 5243.4 | +0 | +6 | 1971 |
| 9 | AS16509 | Amazon AWS | US | 🟠 85 | 292,488 | 1534.9 | +0 | +18 | 14341 |
| 10 | AS16276 | OVH | FR | 🟠 84 | 38,620 | 8497.2 | +0 | +3 | 600 |
| 11 | AS24940 | Hetzner | DE | 🟠 81 | 22,766 | 8099.2 | +0 | +2 | 82 |
| 12 | AS12876 | Scaleway | FR | 🟠 80 | 8,245 | 14462.1 | +0 | +0 | 22 |
| 13 | AS47583 | Hostinger | LT | 🟠 78 | 2,821 | 3555.8 | +0 | +1 | 860 |
| 14 | AS63949 | Linode (Akamai) | US | 🟠 75 | 10,476 | 8258.7 | +0 | +0 | 341 |
| 15 | AS8560 | IONOS | DE | 🟠 74 | 3,190 | 3740.9 | +0 | +3 | 462 |
| 16 | AS26496 | GoDaddy | US | 🟡 65 | 1,946 | 1558.7 | +0 | +0 | 184 |
| 17 | AS8075 | Microsoft Azure | US | 🟡 61 | 36,780 | 554.0 | +0 | +2 | 931 |
| 18 | AS46606 | Bluehost (Unified Layer) | US | 🟡 60 | 909 | 1055.5 | +0 | +0 | 285 |
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
*Generiert: 2026-03-22 04:25 UTC*