# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-23 04:34 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,628,516  
**Davon in bekannten ASN-Ranges:** 793,045

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 110 | 208,999 | 68842.4 | +0 | +256 | 827 |
| 2 | AS132203 | Tencent Cloud | CN | 🔴 104 | 22,755 | 9513.7 | +0 | +3 | 1050 |
| 3 | AS51167 | Contabo | DE | 🔴 103 | 11,932 | 25414.0 | +0 | +1 | 567 |
| 4 | AS12389 | Rostelecom | RU | 🔴 100 | 53,004 | 3079.0 | +0 | +0 | 3183 |
| 5 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 32,142 | 3375.1 | +0 | +0 | 877 |
| 6 | AS20473 | Vultr | US | 🟠 95 | 17,408 | 12715.0 | +0 | +0 | 1453 |
| 7 | AS22612 | Namecheap | US | 🟠 90 | 1,615 | 10540.7 | +0 | +0 | 312 |
| 8 | AS31898 | Oracle Cloud | US | 🟠 85 | 24,918 | 5252.9 | +0 | +6 | 1971 |
| 9 | AS16509 | Amazon AWS | US | 🟠 85 | 293,072 | 1537.9 | +0 | +18 | 14341 |
| 10 | AS16276 | OVH | FR | 🟠 84 | 38,667 | 8507.5 | +0 | +3 | 600 |
| 11 | AS24940 | Hetzner | DE | 🟠 81 | 22,826 | 8120.6 | +0 | +2 | 82 |
| 12 | AS12876 | Scaleway | FR | 🟠 80 | 8,246 | 14463.8 | +0 | +0 | 22 |
| 13 | AS47583 | Hostinger | LT | 🟠 78 | 2,825 | 3560.9 | +0 | +1 | 860 |
| 14 | AS63949 | Linode (Akamai) | US | 🟠 75 | 10,564 | 8328.1 | +0 | +0 | 341 |
| 15 | AS8560 | IONOS | DE | 🟠 74 | 3,205 | 3758.5 | +0 | +3 | 462 |
| 16 | AS26496 | GoDaddy | US | 🟡 65 | 1,944 | 1557.0 | +0 | +0 | 184 |
| 17 | AS8075 | Microsoft Azure | US | 🟡 61 | 36,813 | 554.5 | +0 | +2 | 931 |
| 18 | AS46606 | Bluehost (Unified Layer) | US | 🟡 60 | 909 | 1055.5 | +0 | +0 | 285 |
| 19 | AS36351 | IBM Cloud | US | 🟡 50 | 1,201 | 294.6 | +0 | +0 | 328 |

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
*Generiert: 2026-03-23 04:34 UTC*