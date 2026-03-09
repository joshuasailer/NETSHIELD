
<div align="center">

# 🛡️ NETSHIELD

**Die IPv4 Blocklist Suite für Firewall, Threat Intelligence und Geo Blocking**

[![IPv4 Threat Feeds](https://img.shields.io/badge/IPv4-Threat%20Feeds-blue?style=for-the-badge)](https://github.com/juergen2025sys/NETSHIELD)
[![GeoIP 249 Länder](https://img.shields.io/badge/GeoIP-249%20L%C3%A4nder-success?style=for-the-badge)](https://github.com/juergen2025sys/NETSHIELD/tree/main/countries)
[![6 Kontinente](https://img.shields.io/badge/Kontinente-6-orange?style=for-the-badge)](https://github.com/juergen2025sys/NETSHIELD/tree/main/continents)
[![Automatische Updates](https://img.shields.io/badge/Updates-Automatisch-brightgreen?style=for-the-badge)](https://github.com/juergen2025sys/NETSHIELD/tree/main/.github/workflows)

[![OPNsense](https://img.shields.io/badge/OPNsense-Ready-7b3fe4?style=flat-square)](#opnsense--pfsense)
[![pfSense](https://img.shields.io/badge/pfSense-Ready-0099cc?style=flat-square)](#opnsense--pfsense)
[![FortiGate](https://img.shields.io/badge/FortiGate-Compatible-e95420?style=flat-square)](#einsatzszenarien)
[![Linux](https://img.shields.io/badge/Linux-Firewall%20Friendly-333333?style=flat-square)](#einsatzszenarien)

Fertige Raw-Listen für OPNsense, pfSense, FortiGate, iptables, nftables und jede Firewall mit URL-Feed-Unterstützung.

</div>

---

## ✨ Was ist NETSHIELD?

NETSHIELD bündelt **automatisch gepflegte IPv4-Blocklisten** für zwei zentrale Einsatzzwecke:

- **Threat Blocking** – gegen bekannte Angreifer, Scanner, Tor-, Proxy- und Exploit-IPs
- **Geo Blocking** – nach Ländern und Kontinenten für Firewall-Policies und Netzwerksegmentierung

Die Nutzung ist bewusst einfach gehalten:

1. Raw-Link kopieren
2. In der Firewall als URL Table / Alias eintragen
3. Automatische Updates laufen über GitHub Actions

---

## 🚀 Quick Start

### Empfohlene Einstiegslisten

| Einsatz | Feed | Empfehlung |
|---|---|---|
| Allgemeines Threat Blocking | [active_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt) | Beste Default-Liste für die meisten Firewalls |
| Strengere Threat-Liste | [blacklist_confidence40_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/blacklist_confidence40_ipv4.txt) | Fokus auf höher bewertete Treffer |
| Maximale Abdeckung | [combined_threat_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/combined_threat_blacklist_ipv4.txt) | Für Analyse, SOC, Feed-Fusion |
| Geo Blocking (alle Länder) | [all_countries_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/all_countries_ipv4.txt) | Alle Länder in einer Datei |
| Geo Blocking nach Kontinent | [continents/](https://github.com/juergen2025sys/NETSHIELD/tree/main/continents) | 6 Kontinent-Dateien einzeln |
| Spezialschutz | [tor_exit_nodes.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/tor_exit_nodes.txt) · [vpn_proxy_ranges.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/vpn_proxy_ranges.txt) · [cve_exploit_ips.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/cve_exploit_ips.txt) | Ergänzende Speziallisten |

> **Empfehlung für Einsteiger:** Starte mit [`active_blacklist_ipv4.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt), füge dann schrittweise `tor_exit_nodes.txt` und `vpn_proxy_ranges.txt` hinzu. Geo Blocking erst danach ergänzen.

---

## 📦 Enthaltene Listen

### 🧠 Threat Intelligence

| Datei | Zweck | Update-Intervall |
|---|---|---|
| [combined_threat_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/combined_threat_blacklist_ipv4.txt) | Aggregierte Threat-IPs aus vielen Quellen | alle 6 Stunden |
| [active_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt) | Aktiv gefilterte Firewall-Blockliste | automatisch |
| [blacklist_confidence40_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/blacklist_confidence40_ipv4.txt) | IPs mit höherem Confidence-Score | alle 6 Stunden |
| [watchlist_confidence20to39_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/watchlist_confidence20to39_ipv4.txt) | Beobachtungsliste für schwächere Treffer | alle 6 Stunden |
| [bot_detector_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/bot_detector_blacklist_ipv4.txt) | Bots, Scraper, Scanner, Abuse-Quellen | alle 6 Stunden |
| [tor_exit_nodes.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/tor_exit_nodes.txt) | Tor Exit Nodes | täglich |
| [cve_exploit_ips.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/cve_exploit_ips.txt) | IPs mit Bezug zu aktiver Exploit-Aktivität | täglich |
| [vpn_proxy_ranges.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/vpn_proxy_ranges.txt) | VPN-, Proxy- und Anonymisierungs-Ranges | wöchentlich |
| [asn_blocklist_firewall.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/asn_blocklist_firewall.txt) | Netzwerke mit schlechter Reputation (ASN) | täglich |

### 🌍 Geo Blocking

| Datei | Inhalt |
|---|---|
| [all_countries_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/all_countries_ipv4.txt) | Alle Länder zusammengefasst |
| [continents/](https://github.com/juergen2025sys/NETSHIELD/tree/main/continents) | 6 Kontinent-Dateien |
| [countries/](https://github.com/juergen2025sys/NETSHIELD/tree/main/countries) | Einzeldateien nach Kontinent sortiert |

---

## 📊 Listengröße (aktueller Snapshot)

| Liste | Einträge |
|---|---:|
| [combined_threat_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/combined_threat_blacklist_ipv4.txt) | **2.344.956** |
| [active_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt) | **2.311.839** |
| [blacklist_confidence40_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/blacklist_confidence40_ipv4.txt) | **2.311.839** |
| [cve_exploit_ips.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/cve_exploit_ips.txt) | **220.881** |
| [vpn_proxy_ranges.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/vpn_proxy_ranges.txt) | **111.974** |
| [tor_exit_nodes.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/tor_exit_nodes.txt) | **20.120** |
| [bot_detector_blacklist_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/bot_detector_blacklist_ipv4.txt) | **17.954** |
| [all_countries_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/all_countries_ipv4.txt) | **~254.556 CIDR-Ranges** |

---

## 🏗️ Projektstruktur

```
NETSHIELD/
├── .github/workflows/                  # Automatische Build-, Prüf- und Export-Workflows
├── active_blacklist_ipv4.txt           # Empfohlene aktive Firewall-Blockliste
├── combined_threat_blacklist_ipv4.txt  # Große aggregierte Threat-Liste
├── blacklist_confidence40_ipv4.txt     # Höhere Confidence / strengere Filterung
├── bot_detector_blacklist_ipv4.txt     # Bot-, Scraper- und Scanner-Erkennung
├── tor_exit_nodes.txt                  # Tor Exit Nodes
├── cve_exploit_ips.txt                 # Exploit-nahe IPs
├── vpn_proxy_ranges.txt                # VPN- und Proxy-Ranges
├── all_countries_ipv4.txt              # Alle Länder in einer Datei
├── continents/                         # Kontinent-Dateien
├── countries/                          # Länderdateien nach Region sortiert
└── NETSHIELD_REPORT.md                 # Automatisch generierter Projektstatus
```

---

## ⚙️ Automatisierung via GitHub Actions

NETSHIELD ist kein statisches IP-Archiv, sondern ein **automatisiertes Blocklist-Framework**. Workflows pflegen Listen kontinuierlich:

| Workflow | Aufgabe |
|---|---|
| `update-blocklist.yml` | Hauptliste aktualisieren |
| `update_combined_blacklist.yml` | Kombinierte Liste zusammenführen |
| `update_confidence_blacklist.yml` | Confidence-basierte Filterung |
| `false_positive_checker.yml` | False-Positive-Erkennung |
| `feed_health_monitor.yml` | Feed-Qualität überwachen |
| `firewall_format_exporter.yml` | Exportformate erzeugen |
| `tor_exit_monitor.yml` | Tor Exit Nodes tracken |
| `vpn_proxy_detector.yml` | VPN/Proxy-Ranges erkennen |
| `asn_reputation_scorer.yml` | ASN-Reputationsbewertung |

---

## 🎯 Einsatzszenarien

### OPNsense / pfSense

- URL Table Alias mit [`active_blacklist_ipv4.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt) als Typ `URL Table (IPs)`
- Zusätzliche Alias-Feeds: [`tor_exit_nodes.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/tor_exit_nodes.txt) und [`vpn_proxy_ranges.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/vpn_proxy_ranges.txt)
- Geo Blocking über [continents/](https://github.com/juergen2025sys/NETSHIELD/tree/main/continents) oder einzelne Länderdateien

### Webserver / Reverse Proxies

- [`bot_detector_blacklist_ipv4.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/bot_detector_blacklist_ipv4.txt)
- [`tor_exit_nodes.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/tor_exit_nodes.txt)
- [`vpn_proxy_ranges.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/vpn_proxy_ranges.txt)

### SOC / Lab / Forschung

- [`combined_threat_blacklist_ipv4.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/combined_threat_blacklist_ipv4.txt) als umfassender Feed
- `blacklist_geo_enriched.json` für angereicherte Daten
- [NETSHIELD_REPORT.md](https://github.com/juergen2025sys/NETSHIELD/blob/main/NETSHIELD_REPORT.md) für aktuelle Projektstatus-Reports

---

## 🛡️ Confidence-Modell

NETSHIELD bewertet IPs anhand eines **gewichteten Score-Modells**:

- Feed-Qualität und Quellenreputation
- Mehrfachsichtung über verschiedene Feeds
- Aktualität und zeitliche Persistenz

Das ermöglicht eine klare Trennung:

| Score | Liste | Empfehlung |
|---|---|---|
| ≥ 40 | [`blacklist_confidence40_ipv4.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/blacklist_confidence40_ipv4.txt) | Direkt blocken |
| 20–39 | [`watchlist_confidence20to39_ipv4.txt`](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/watchlist_confidence20to39_ipv4.txt) | Beobachten / loggen |

---

## 🌐 Geo Blocking – Kontinente & Länder

### Kontinente

| Datei | Region |
|---|---|
| [africa_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/continents/africa_ipv4.txt) | Afrika |
| [asia_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/continents/asia_ipv4.txt) | Asien |
| [europe_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/continents/europe_ipv4.txt) | Europa |
| [north_america_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/continents/north_america_ipv4.txt) | Nordamerika |
| [south_america_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/continents/south_america_ipv4.txt) | Südamerika |
| [oceania_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/continents/oceania_ipv4.txt) | Ozeanien |

### Einzelne Länder

Länderdateien liegen unter `countries/{kontinent}/{land}_ipv4.txt`, z. B.:

- [countries/europe/germany_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/countries/europe/germany_ipv4.txt)
- [countries/europe/russia_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/countries/europe/russia_ipv4.txt)
- [countries/asia/japan_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/countries/asia/japan_ipv4.txt)
- [countries/north_america/united_states_ipv4.txt](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/countries/north_america/united_states_ipv4.txt)

Alle 249 Länder sind im [countries/](https://github.com/juergen2025sys/NETSHIELD/tree/main/countries) Verzeichnis verfügbar.

---

## ⚠️ Hinweise

**GeoIP ist eine Näherung.** Country- und Kontinentlisten basieren auf administrativer IP-Zuordnung. Bei CDN-Infrastruktur, Cloud-Providern, Gaming-Diensten, globalen Anycast-/Edge-Netzen und VPN-/Hosting-Plattformen kann es zu False Positives kommen.

**Große Listen testen.** Vor dem Produktiveinsatz empfehlen sich Staging-Regeln, Log-Monitoring, schrittweise Aktivierung und Whitelisting legitimer Ziele.

---

## 📄 Lizenz

Im Repository ist aktuell keine Lizenz dokumentiert. Für produktive oder kommerzielle Nutzung sollte die Lizenzlage beim Projektinhaber erfragt werden.

---

<div align="center">

## 🔥 NETSHIELD ist nicht nur eine Liste.
### Es ist ein automatisiertes Blocklist-Framework für echte Firewall-Workflows.

[→ Zum Repository](https://github.com/juergen2025sys/NETSHIELD) · [→ Direkter Feed-Einstieg](https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt) · [→ Projektstatus](https://github.com/juergen2025sys/NETSHIELD/blob/main/NETSHIELD_REPORT.md)

</div>
