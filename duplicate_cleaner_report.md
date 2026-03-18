# Duplicate Cleaner – Report
**Aktualisiert:** 2026-03-18 19:32 UTC

---
## Ergebnis

| Datei | Vorher | Nachher | Intern | Cross-list | Aktion |
|---|---|---|---|---|---|
| ✅ `combined_threat_blacklist_ipv4.txt` | 3,970,399 | 3,970,399 | 0 | 0 | ✅ sauber |
| ✅ `cve_exploit_ips.txt` | 230,581 | 230,581 | 0 | 0 | ⏭️ cross-list übersprungen |
| ✅ `honeypot_ips.txt` | 11,193 | 0 | 0 | 11,193 | 🗑️ 11193 entfernt |
| ✅ `honeydb_ips.txt` | 12,311 | 0 | 0 | 12,311 | 🗑️ 12311 entfernt |
| ✅ `bot_detector_blacklist_ipv4.txt` | 17,950 | 15,458 | 0 | 2,492 | 🗑️ 2492 entfernt |

---
## Cross-list Überschneidungen mit combined

> `cve_exploit_ips.txt` wird nicht cross-bereinigt – ist eigenständige Feed-Quelle.

| Sub-Liste | Überschneidung | Anteil |
|---|---|---|
| `cve_exploit_ips.txt` | 230,581 | 100.0% |
| `honeypot_ips.txt` | 11,193 | 100.0% |
| `honeydb_ips.txt` | 12,311 | 100.0% |
| `bot_detector_blacklist_ipv4.txt` | 2,492 | 13.9% |

---
## Sub-Listen untereinander (nur Info)

| Paar | Gemeinsame IPs |
|---|---|
| `cve∩honeypot` | 9,228 |
| `cve∩honeydb` | 5,783 |
| `honeypot∩honeydb` | 2,997 |
| `cve∩botdet` | 476 |
| `honeypot∩botdet` | 24 |
| `honeydb∩botdet` | 18 |

---
## Zusammenfassung

| Metrik | Wert |
|---|---|
| Interne Duplikate entfernt | **0** |
| Cross-list Duplikate entfernt | **25,996** |
| Gesamt entfernt | **25,996** |
| Combined (nach Bereinigung) | **3,970,399** |

---
*Generiert: 2026-03-18 19:32 UTC*