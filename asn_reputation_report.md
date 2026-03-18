# ASN Reputation Scorer – Report
**Aktualisiert:** 2026-03-18 04:30 UTC  
**Methode:** ScaniteX CIDR-Prefixlisten (kein API-Key, 100% BL-Coverage)  
**Blacklist-IPs gesamt:** 3,693,391  
**Davon in bekannten ASN-Ranges:** 742,746

---

## ASN-Übersicht (nach Score sortiert)

| Rang | ASN | Organisation | Land | Score | BL-Hits | Dichte/1M | DROP | ET | Prefixes |
|---|---|---|---|---|---|---|---|---|---|
| 1 | AS14061 | DigitalOcean | US | 🔴 110 | 202,340 | 66649.0 | +0 | +257 | 827 |
| 2 | AS132203 | Tencent Cloud | CN | 🔴 105 | 22,679 | 9482.0 | +0 | +5 | 1050 |
| 3 | AS51167 | Contabo | DE | 🔴 103 | 11,732 | 24988.1 | +0 | +1 | 567 |
| 4 | AS45102 | Alibaba Cloud | CN | 🟠 95 | 31,850 | 3344.5 | +0 | +0 | 877 |
| 5 | AS20473 | Vultr | US | 🟠 95 | 17,090 | 12482.8 | +0 | +0 | 1453 |
| 6 | AS22612 | Namecheap | US | 🟠 90 | 1,611 | 10514.6 | +0 | +0 | 312 |
| 7 | AS12389 | Rostelecom | RU | 🟠 85 | 13,894 | 807.1 | +0 | +0 | 3183 |
| 8 | AS31898 | Oracle Cloud | US | 🟠 85 | 24,684 | 5203.6 | +0 | +8 | 1971 |
| 9 | AS16509 | Amazon AWS | US | 🟠 85 | 290,416 | 1524.0 | +0 | +18 | 14341 |
| 10 | AS24940 | Hetzner | DE | 🟠 84 | 22,721 | 8083.2 | +0 | +3 | 82 |
| 11 | AS16276 | OVH | FR | 🟠 84 | 38,734 | 8522.3 | +0 | +3 | 600 |
| 12 | AS12876 | Scaleway | FR | 🟠 80 | 8,192 | 14369.1 | +0 | +0 | 22 |
| 13 | AS47583 | Hostinger | LT | 🟠 78 | 2,807 | 3538.2 | +0 | +1 | 860 |
| 14 | AS63949 | Linode (Akamai) | US | 🟠 75 | 10,167 | 8015.1 | +0 | +0 | 341 |
| 15 | AS8560 | IONOS | DE | 🟠 74 | 3,166 | 3712.8 | +0 | +3 | 462 |
| 16 | AS26496 | GoDaddy | US | 🟡 65 | 1,941 | 1554.7 | +0 | +0 | 184 |
| 17 | AS8075 | Microsoft Azure | US | 🟡 61 | 36,620 | 551.6 | +0 | +2 | 931 |
| 18 | AS46606 | Bluehost (Unified Layer) | US | 🟡 60 | 900 | 1045.1 | +0 | +0 | 285 |
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
*Generiert: 2026-03-18 04:30 UTC*