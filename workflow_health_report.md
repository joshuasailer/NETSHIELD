# Workflow Health Checker – Report
**Aktualisiert:** 2026-03-09 19:31 UTC

**Workflows:** 17 | ✅ 0 OK | ⚠️ 15 Warnung | ❌ 2 Fehler

---
## Übersicht

| Workflow | Status | Fehler | Warnungen | Cron |
|---|---|---|---|---|
| `active_filter.yml` | ⚠️ WARNUNG | 0 | 2 | `15 0 * * *` |
| `asn_reputation_scorer.yml` | ❌ FEHLER | 1 | 4 | `0 2 * * *` |
| `cve_to_ip_mapper.yml` | ⚠️ WARNUNG | 0 | 2 | `0 4 * * *` |
| `duplicate_cleaner.yml` | ⚠️ WARNUNG | 0 | 2 | `30 4 * * *` |
| `false_positive_checker.yml` | ⚠️ WARNUNG | 0 | 4 | `0 5 * * 0` |
| `feed_health_monitor.yml` | ⚠️ WARNUNG | 0 | 2 | `0 1 * * *` |
| `firewall_format_exporter.yml` | ⚠️ WARNUNG | 0 | 4 | `30 0 * * *` |
| `geo_tagger.yml` | ⚠️ WARNUNG | 0 | 3 | `0 6 * * 0` |
| `netshield_report_generator.yml` | ⚠️ WARNUNG | 0 | 2 | `50 0 * * *` |
| `score_decay_monitor.yml` | ⚠️ WARNUNG | 0 | 4 | `0 7 * * 0` |
| `tor_exit_monitor.yml` | ⚠️ WARNUNG | 0 | 2 | `30 23 * * *` |
| `update-blocklist.yml` | ⚠️ WARNUNG | 0 | 3 | `0 3 * * 1`, `0 3 * * 3` |
| `update_bot_detector.yml` | ⚠️ WARNUNG | 0 | 2 | `45 23 * * *` |
| `update_combined_blacklist.yml` | ⚠️ WARNUNG | 0 | 2 | `0 0 * * *` |
| `update_confidence_blacklist.yml` | ⚠️ WARNUNG | 0 | 1 | `15 0 * * *` |
| `vpn_proxy_detector.yml` | ⚠️ WARNUNG | 0 | 2 | `30 3 * * 1` |
| `workflow_health_checker.yml` | ❌ FEHLER | 3 | 2 | `0 1 * * *`, ` in line and line.count(` |

---
## ❌ Fehler im Detail

### `asn_reputation_scorer.yml`

- 🔴 Zeile 125: `str(...).get(...)` – str hat kein .get(), führt zu AttributeError. Korrekt: `(dict_expr).get(...)`

### `workflow_health_checker.yml`

- 🔴 Ungültiger Cron-Ausdruck: ` in line and line.count(` (erwartet 5 Felder)
- 🔴 Zeile 130: `str(...).get(...)` – str hat kein .get(), führt zu AttributeError. Korrekt: `(dict_expr).get(...)`
- 🔴 Zeile 133: `str(...).get(...)` – str hat kein .get(), führt zu AttributeError. Korrekt: `(dict_expr).get(...)`


---
## ⚠️ Warnungen im Detail

### `active_filter.yml`

- 🟡 Zeile 64: `.sort()` ohne `key=` auf IP-Liste – lexikografisch statt numerisch
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `asn_reputation_scorer.yml`

- 🟡 Zeile 125: HTTP-Call in List-Comprehension – kein Rate-Limiting möglich, kann zu API-Sperren führen. Besser: explizite Schleife mit `time.sleep()`
- 🟡 Zeile 148: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Zeile 185: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `cve_to_ip_mapper.yml`

- 🟡 Zeile 178: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `duplicate_cleaner.yml`

- 🟡 Zeile 190: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `false_positive_checker.yml`

- 🟡 Zeile 166: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Zeile 202: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben
- 🟡 Zeile 163: Kommentar erwähnt 'Top-500' aber kein `[:500]`-Slice im Code – irreführend, prüfen ob wirklich alle IPs gemeint sind

### `feed_health_monitor.yml`

- 🟡 Zeile 245: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `firewall_format_exporter.yml`

- 🟡 Zeile 63: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Zeile 100: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Zeile 126: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `geo_tagger.yml`

- 🟡 Zeile 5: Doppelter Kommentar im Cron-Eintrag – bitte bereinigen
- 🟡 Zeile 178: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `netshield_report_generator.yml`

- 🟡 Zeile 100: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `score_decay_monitor.yml`

- 🟡 Zeile 45: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Zeile 99: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Zeile 145: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `tor_exit_monitor.yml`

- 🟡 Zeile 87: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `update-blocklist.yml`

- 🟡 Zeile 65: `sorted(ips)` ohne `key=` – lexikografische Sortierung, nicht numerisch (z.B. '10.x' < '2.x'). Korrekt: `sorted(ips, key=lambda ip: tuple(int(o) for o in ip.split('.')))`
- 🟡 Zeile 66: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `update_bot_detector.yml`

- 🟡 Zeile 42: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `update_combined_blacklist.yml`

- 🟡 Zeile 359: `.sort()` ohne `key=` auf IP-Liste – lexikografisch statt numerisch
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `update_confidence_blacklist.yml`

- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `vpn_proxy_detector.yml`

- 🟡 Zeile 169: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen
- 🟡 Kein `concurrency:`-Block – gleichzeitige schedule+manuell Runs können sich gegenseitig überschreiben

### `workflow_health_checker.yml`

- 🟡 Zeile 156: `sorted(ips)` ohne `key=` – lexikografische Sortierung, nicht numerisch (z.B. '10.x' < '2.x'). Korrekt: `sorted(ips, key=lambda ip: tuple(int(o) for o in ip.split('.')))`
- 🟡 Zeile 236: `open()` ohne `encoding="utf-8"` für Textdatei – kann auf manchen Systemen zu Fehlern führen


---
*Generiert: 2026-03-09 19:31 UTC | 17 Workflow-Dateien geprüft*