# Workflow Health Checker – Report
**Aktualisiert:** 2026-03-15 19:34 UTC

**Workflows:** 19 | ✅ 13 OK | ⚠️ 6 Warnung | ❌ 0 Fehler

---
## ⚠️ Warnungen

| Datei | Check | Detail |
|---|---|---|
| `workflow_health_checker.yml + workflow_health_checker.yml` | Cron-Kollision | '(.+?)' – beide Workflows laufen gleichzeitig |
| `community_ip_report.yml` | Encoding fehlt | Block 0: open(..., 'w') ohne encoding= – UnicodeEncodeError möglich |
| `duplicate_cleaner.yml` | Encoding fehlt | Block 0: open(..., 'w') ohne encoding= – UnicodeEncodeError möglich |
| `false_positive_checker.yml` | Encoding fehlt | Block 0: open(..., 'w') ohne encoding= – UnicodeEncodeError möglich |
| `honeydb_monitor.yml` | Encoding fehlt | Block 0: open(..., 'w') ohne encoding= – UnicodeEncodeError möglich |
| `honeypot_monitor.yml` | Encoding fehlt | Block 0: open(..., 'w') ohne encoding= – UnicodeEncodeError möglich |
| `tor_exit_monitor.yml` | Encoding fehlt | Block 0: open(..., 'w') ohne encoding= – UnicodeEncodeError möglich |

## Übersicht

| Workflow | Status | Fehler | Warnungen | Cron |
|---|---|---|---|---|
| `asn_reputation_scorer.yml` | ✅ OK | 0 | 0 | `0 2 * * *` |
| `auto_feed_discovery.yml` | ✅ OK | 0 | 0 | `30 4 * * 0` |
| `community_ip_report.yml` | ⚠️ | 0 | 1 | – |
| `cve_to_ip_mapper.yml` | ✅ OK | 0 | 0 | `0 4 * * *` |
| `duplicate_cleaner.yml` | ⚠️ | 0 | 1 | `30 5 * * *` |
| `false_positive_checker.yml` | ⚠️ | 0 | 1 | `0 5 * * *`, `0 13 * * *`, `0 20 * * *` |
| `feed_health_monitor.yml` | ✅ OK | 0 | 0 | `0 1 * * *` |
| `geo_tagger.yml` | ✅ OK | 0 | 0 | `45 6 * * 0` |
| `honeydb_monitor.yml` | ⚠️ | 0 | 1 | `15 22 * * *` |
| `honeypot_monitor.yml` | ⚠️ | 0 | 1 | `0 23 * * *` |
| `netshield_report_generator.yml` | ✅ OK | 0 | 0 | `0,30 * * * *` |
| `score_decay_monitor.yml` | ✅ OK | 0 | 0 | `0 7 * * 0` |
| `tor_exit_monitor.yml` | ⚠️ | 0 | 1 | `30 23 * * *` |
| `update-blocklist.yml` | ✅ OK | 0 | 0 | `30 2 * * 1`, `30 2 * * 3` |
| `update_bot_detector.yml` | ✅ OK | 0 | 0 | `45 22 * * *` |
| `update_combined_blacklist.yml` | ✅ OK | 0 | 0 | `0 */3 * * *` |
| `update_confidence_blacklist.yml` | ✅ OK | 0 | 0 | `30 0 * * *`, `30 3 * * *`, `30 6 * * *`, `30 9 * * *`, `30 12 * * *`, `30 15 * * *`, `30 18 * * *`, `30 21 * * *` |
| `vpn_proxy_detector.yml` | ✅ OK | 0 | 0 | `45 3 * * 1` |
| `workflow_health_checker.yml` | ✅ OK | 0 | 0 | `15 1 * * *`, `(.+?)`, `(.+?)` |

---
*Generiert: 2026-03-15 19:34 UTC | 19 Workflow-Dateien geprüft*