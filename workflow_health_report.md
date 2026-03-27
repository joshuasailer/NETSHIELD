# Workflow Health Checker – Report
**Aktualisiert:** 2026-03-27 04:06 UTC

**Workflows:** 16 | ✅ 13 OK | ⚠️ 3 Warnung | ❌ 0 Fehler

---
## ⚠️ Warnungen

| Datei | Check | Detail |
|---|---|---|
| `auto_feed_discovery.yml` | Git Push ohne Retry-Schleife | git push ohne Retry-Schleife – Race-Condition bei parallelen Runs (kein 'for attempt in ...') |
| `community_ip_report.yml` | Git Push ohne Retry-Schleife | git push ohne Retry-Schleife – Race-Condition bei parallelen Runs (kein 'for attempt in ...') |
| `feed_health_monitor.yml` | Git Push ohne Retry-Schleife | git push ohne Retry-Schleife – Race-Condition bei parallelen Runs (kein 'for attempt in ...') |

## Übersicht

| Workflow | Status | Fehler | Warnungen | Cron |
|---|---|---|---|---|
| `asn_reputation_scorer.yml` | ✅ OK | 0 | 0 | `0 2 * * *` |
| `auto_feed_discovery.yml` | ⚠️ | 0 | 1 | `30 4 * * 0` |
| `community_ip_report.yml` | ⚠️ | 0 | 1 | – |
| `cve_to_ip_mapper.yml` | ✅ OK | 0 | 0 | `0 4 * * *` |
| `false_positive_checker.yml` | ✅ OK | 0 | 0 | `0 5 * * *`, `0 13 * * *`, `0 20 * * *` |
| `feed_health_monitor.yml` | ⚠️ | 0 | 1 | `0 1 * * *` |
| `geo_tagger.yml` | ✅ OK | 0 | 0 | `45 6 * * 0` |
| `honeydb_monitor.yml` | ✅ OK | 0 | 0 | `15 22 * * *` |
| `honeypot_monitor.yml` | ✅ OK | 0 | 0 | `0 23 * * *` |
| `netshield_report_generator.yml` | ✅ OK | 0 | 0 | `5 * * * *` |
| `score_decay_monitor.yml` | ✅ OK | 0 | 0 | `0 7 * * 0` |
| `update-blocklist.yml` | ✅ OK | 0 | 0 | `30 1 * * 1`, `30 1 * * 3` |
| `update_bot_detector.yml` | ✅ OK | 0 | 0 | `45 22 * * *` |
| `update_combined_blacklist.yml` | ✅ OK | 0 | 0 | `0 */3 * * *` |
| `update_confidence_blacklist.yml` | ✅ OK | 0 | 0 | `30 0 * * *`, `30 3 * * *`, `30 6 * * *`, `30 9 * * *`, `30 12 * * *`, `30 15 * * *`, `30 18 * * *`, `30 21 * * *` |
| `workflow_health_checker.yml` | ✅ OK | 0 | 0 | – |

---
*Generiert: 2026-03-27 04:06 UTC | 16 Workflow-Dateien geprüft*