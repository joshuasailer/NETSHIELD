# Duplicate Cleaner – Report
**Aktualisiert:** 2026-03-09 05:41 UTC

---
## Dateigrößen

| Datei | IPs |
|---|---|
| ✅ `combined_threat_blacklist_ipv4.txt` | 2,312,776 |
| ✅ `tor_exit_nodes.txt` | 20,120 |
| ✅ `cve_exploit_ips.txt` | 220,881 |
| ✅ `vpn_proxy_ranges.txt` | 111,974 |
| ✅ `bot_detector_blacklist_ipv4.txt` | 15,912 |

---
## Überschneidungen mit combined_threat_blacklist

| Sub-Liste | Gemeinsame IPs | Anteil | Aktion |
|---|---|---|---|
| `tor_exit_nodes.txt` | 20,120 | 100.0% | 🔒 behalten (HQ-Feed) |
| `cve_exploit_ips.txt` | 203,823 | 92.3% | 🔒 behalten (HQ-Feed) |
| `vpn_proxy_ranges.txt` | 4,022 | 3.6% | 🗑️ 4022 entfernt |
| `bot_detector_blacklist_ipv4.txt` | 2,042 | 12.8% | 🗑️ 2042 entfernt |

---
## Sub-Listen Überschneidungen (nur Info)

| Paar | Gemeinsame IPs |
|---|---|
| `tor∩cve` | 18,577 |
| `cve∩botdet` | 440 |
| `cve∩vpn` | 133 |
| `tor∩botdet` | 47 |
| `tor∩vpn` | 10 |
| `vpn∩botdet` | 1 |

*Sub-Listen-Duplikate werden nicht entfernt – combined dedupliziert automatisch.*

---
## Zusammenfassung

| Metrik | Wert |
|---|---|
| Duplikate entfernt (vpn + botdet) | **6,064** |
| Tor/CVE behalten (HQ-Markierung) | **223,943** |
| Combined Blacklist (unverändert) | **2,312,776** |

---
*Generiert: 2026-03-09 05:41 UTC*