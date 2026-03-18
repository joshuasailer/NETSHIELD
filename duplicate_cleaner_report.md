# Duplicate Cleaner – Report
**Aktualisiert:** 2026-03-18 06:38 UTC

---
## Dateigrößen

| Datei | IPs |
|---|---|
| ✅ `combined_threat_blacklist_ipv4.txt` | 3,956,086 |
| ✅ `cve_exploit_ips.txt` | 230,581 |
| ✅ `honeypot_ips.txt` | 11,193 |
| ✅ `honeydb_ips.txt` | 12,311 |
| ✅ `bot_detector_blacklist_ipv4.txt` | 17,954 |

---
## Überschneidungen mit combined_threat_blacklist

> Alle Sub-Listen (cve/honeypot/honeydb/botdet) sind LOCAL_FEEDS –

> combined liest sie direkt ein, daher keine Bereinigung nötig.

| Sub-Liste | Gemeinsame IPs | Anteil | Aktion |
|---|---|---|---|
| `cve_exploit_ips.txt` | 230,507 | 100.0% | ⏭️ übersprungen (LOCAL_FEED) |
| `honeypot_ips.txt` | 11,182 | 99.9% | ⏭️ übersprungen (LOCAL_FEED) |
| `honeydb_ips.txt` | 11,188 | 90.9% | ⏭️ übersprungen (LOCAL_FEED) |
| `bot_detector_blacklist_ipv4.txt` | 2,489 | 13.9% | ⏭️ übersprungen (LOCAL_FEED) |

---
## Sub-Listen Überschneidungen (nur Info)

| Paar | Gemeinsame IPs |
|---|---|
| `cve∩honeypot` | 9,228 |
| `cve∩honeydb` | 5,783 |
| `honeypot∩honeydb` | 2,997 |
| `cve∩botdet` | 476 |
| `honeypot∩botdet` | 24 |
| `honeydb∩botdet` | 18 |

*Sub-Listen-Duplikate werden nicht entfernt – combined dedupliziert automatisch.*

---
## Zusammenfassung

| Metrik | Wert |
|---|---|
| Duplikate entfernt | **0** |
| Combined Blacklist (unverändert) | **3,956,086** |

---
*Generiert: 2026-03-18 06:38 UTC*