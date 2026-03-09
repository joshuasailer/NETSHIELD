

<div align="center">

# 🛡️ NETSHIELD

### Die visuell starke IPv4 Blocklist Suite für Firewall, Threat Intelligence und Geo Blocking

<p>
  <img src="https://img.shields.io/badge/IPv4-Threat%20Feeds-blue?style=for-the-badge" alt="IPv4 Threat Feeds" />
  <img src="https://img.shields.io/badge/GeoIP-249%20L%C3%A4nder-success?style=for-the-badge" alt="249 Länder" />
  <img src="https://img.shields.io/badge/Kontinente-6-orange?style=for-the-badge" alt="6 Kontinente" />
  <img src="https://img.shields.io/badge/Updates-Automatisch-brightgreen?style=for-the-badge" alt="Automatische Updates" />
</p>

<p>
  <img src="https://img.shields.io/badge/OPNsense-Ready-7b3fe4?style=flat-square" alt="OPNsense Ready" />
  <img src="https://img.shields.io/badge/pfSense-Ready-0099cc?style=flat-square" alt="pfSense Ready" />
  <img src="https://img.shields.io/badge/FortiGate-Compatible-e95420?style=flat-square" alt="FortiGate Compatible" />
  <img src="https://img.shields.io/badge/Linux-Firewall%20Friendly-333333?style=flat-square" alt="Linux Firewall Friendly" />
</p>

**Fertige Raw-Listen für OPNsense, pfSense, FortiGate, iptables, nftables und andere Firewalls mit URL/IP-Feed-Unterstützung.**

</div>

---

## ✨ Warum NETSHIELD?

NETSHIELD bündelt **automatisch gepflegte IPv4-Blocklisten** für zwei zentrale Einsatzzwecke:

- **Threat Blocking** gegen bekannte Angreifer, Scanner, Tor-, Proxy- und Exploit-IPs
- **Geo Blocking** nach **Ländern** und **Kontinenten** für Firewall-Policies und Segmentierung

Der Fokus liegt auf einer einfachen Nutzung:

1. **Raw-Link kopieren**  
2. **In der Firewall als URL Table / Alias eintragen**  
3. **Automatische Updates nutzen**

---

## 🚀 Quick Start

### Empfohlene Startlisten

| Einsatz | Datei | Empfehlung |
|---|---|---|
| Allgemeines Threat Blocking | `active_blacklist_ipv4.txt` | Beste Default-Liste für die meisten Firewalls |
| Strengere Threat-Liste | `blacklist_confidence40_ipv4.txt` | Fokus auf höher bewertete Treffer |
| Große Sammelliste | `combined_threat_blacklist_ipv4.txt` | Für Analyse, SOC, Forschung, Feed-Fusion |
| Geo Blocking komplett | `all_countries_ipv4.txt` | Alle Länder in einer Datei |
| Geo Blocking regional | `continents/*.txt` | Pro Kontinent getrennt |
| Spezialschutz | `tor_exit_nodes.txt`, `vpn_proxy_ranges.txt`, `cve_exploit_ips.txt` | Ergänzende Speziallisten |

### Direkt nutzbare Raw-Links

```text
https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt
https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/blacklist_confidence40_ipv4.txt
https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/combined_threat_blacklist_ipv4.txt
https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/all_countries_ipv4.txt
```

---

## 📦 Enthaltene Listen

### 🧠 Threat Intelligence

| Datei | Zweck | Update |
|---|---|---|
| `combined_threat_blacklist_ipv4.txt` | Aggregierte Threat-IPs aus vielen Quellen | alle 6 Stunden |
| `active_blacklist_ipv4.txt` | Aktiv gefilterte Liste für Firewall-Einsatz | automatisch |
| `blacklist_confidence40_ipv4.txt` | IPs mit höherem Confidence-Score | alle 6 Stunden |
| `watchlist_confidence20to39_ipv4.txt` | Beobachtungsliste für schwächere Treffer | alle 6 Stunden |
| `bot_detector_blacklist_ipv4.txt` | Bots, Scraper, Scanner, Abuse-Quellen | alle 6 Stunden |
| `tor_exit_nodes.txt` | Tor Exit Nodes | täglich |
| `cve_exploit_ips.txt` | IPs mit Bezug zu aktiver Exploit-Aktivität | täglich |
| `vpn_proxy_ranges.txt` | VPN-, Proxy- und Anonymisierungs-Ranges | wöchentlich |
| `asn_blocklist_firewall.txt` | Netzwerke mit schlechter Reputation | täglich |

### 🌍 Geo Blocking

| Bereich | Inhalt |
|---|---|
| `all_countries_ipv4.txt` | Zusammengefasste Länderliste |
| `continents/` | 6 Kontinent-Dateien |
| `countries/` | Einzeldateien für Länder nach Kontinent sortiert |

---

## 📊 Snapshot aus dem Projekt

> Basierend auf dem im Repository enthaltenen Report.

| Liste | Größe |
|---|---:|
| `combined_threat_blacklist_ipv4.txt` | **2,344,956** Einträge |
| `active_blacklist_ipv4.txt` | **2,311,839** Einträge |
| `blacklist_confidence40_ipv4.txt` | **2,311,839** Einträge |
| `bot_detector_blacklist_ipv4.txt` | **17,954** Einträge |
| `tor_exit_nodes.txt` | **20,120** Einträge |
| `cve_exploit_ips.txt` | **220,881** Einträge |
| `vpn_proxy_ranges.txt` | **111,974** Einträge |
| `all_countries_ipv4.txt` | **~254,556 CIDR-Ranges** |

---

## 🏗️ Projektstruktur

```text
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
├── countries/                          # Länder-Dateien nach Region sortiert
└── NETSHIELD_REPORT.md                 # Automatisch generierter Projektstatus
```

---

## ⚙️ Automatisierung

NETSHIELD nutzt mehrere **GitHub Actions Workflows**, um Listen automatisch zu:

- aktualisieren
- bereinigen
- bewerten
- zusammenführen
- exportieren
- überwachen

### Beispiele für vorhandene Workflows

- `update-blocklist.yml`
- `update_combined_blacklist.yml`
- `update_confidence_blacklist.yml`
- `false_positive_checker.yml`
- `feed_health_monitor.yml`
- `workflow_health_checker.yml`
- `firewall_format_exporter.yml`
- `tor_exit_monitor.yml`
- `vpn_proxy_detector.yml`
- `asn_reputation_scorer.yml`

Das Projekt ist damit nicht nur eine statische IP-Sammlung, sondern eher ein **automatisiertes Feed- und Blocklist-Framework**.

---

## 🎯 Empfohlene Einsatzszenarien

### Für OPNsense / pfSense

- URL Table Alias mit `active_blacklist_ipv4.txt`
- zusätzliche Alias-Feeds für `tor_exit_nodes.txt` und `vpn_proxy_ranges.txt`
- Geo Blocking über `continents/*.txt` oder einzelne Länderdateien

### Für Webserver / Reverse Proxies

- `bot_detector_blacklist_ipv4.txt`
- `tor_exit_nodes.txt`
- `vpn_proxy_ranges.txt`

### Für SOC / Lab / Forschung

- `combined_threat_blacklist_ipv4.txt`
- `blacklist_geo_enriched.json`
- Reports und Workflow-Outputs

---

## 🧪 Beispiel: OPNsense Alias

### Alias URL

```text
https://raw.githubusercontent.com/juergen2025sys/NETSHIELD/main/active_blacklist_ipv4.txt
```

### Typ

```text
URL Table (IPs)
```

### Sinnvolle Ergänzungen

- `tor_exit_nodes.txt`
- `vpn_proxy_ranges.txt`
- `countries/europe/russia_ipv4.txt`
- `continents/asia_ipv4.txt`

---

## 🛡️ Confidence-Modell in Kurzform

NETSHIELD arbeitet im Projekt mit einem **gewichteten Score-Modell** für bestimmte Listen.

Einträge werden unter anderem nach diesen Kriterien bewertet:

- Quelle bzw. Feed-Qualität
- Mehrfachsichtung in mehreren Feeds
- Aktualität
- Persistenz über Zeit

Damit ist eine Trennung möglich zwischen:

- **blocken** (`blacklist_confidence40_ipv4.txt`)
- **beobachten** (`watchlist_confidence20to39_ipv4.txt`)

---

## 🌐 Länder- und Kontinentdateien

### Kontinente

- `continents/africa_ipv4.txt`
- `continents/asia_ipv4.txt`
- `continents/europe_ipv4.txt`
- `continents/north_america_ipv4.txt`
- `continents/south_america_ipv4.txt`
- `continents/oceania_ipv4.txt`

### Einzelne Länder

Die Länderdateien liegen unter:

```text
countries/{kontinent}/{land}_ipv4.txt
```

Beispiele:

```text
countries/europe/germany_ipv4.txt
countries/europe/france_ipv4.txt
countries/asia/japan_ipv4.txt
countries/north_america/united_states_ipv4.txt
```

---

## ✅ Stärken des Projekts

- sehr breite Abdeckung
- klar getrennte Listen nach Einsatzzweck
- gute Struktur für Firewalls
- Geo Blocking und Threat Blocking in einem Repo
- automatische Pflege per GitHub Actions
- direkt per Raw-Link nutzbar

---

## ⚠️ Wichtige Hinweise

### GeoIP ist nie perfekt

Country- und Kontinent-Listen basieren auf administrativer IP-Zuordnung. Das kann bei diesen Umgebungen zu False Positives führen:

- CDN-Infrastruktur
- Cloud-Provider
- Gaming-Dienste
- globale Anycast-/Edge-Netze
- VPN-/Hosting-Plattformen

### Große Listen testen

Vor produktivem Einsatz empfehlen sich:

- Staging / Testregeln
- Log-Monitoring
- schrittweise Aktivierung
- Whitelisting legitimer Ziele

---

## 💡 Empfehlung für neue Nutzer

Wenn du NETSHIELD zum ersten Mal einsetzt, starte mit dieser Reihenfolge:

1. `active_blacklist_ipv4.txt`
2. `tor_exit_nodes.txt`
3. `vpn_proxy_ranges.txt`
4. optional `bot_detector_blacklist_ipv4.txt`
5. Geo Blocking erst danach gezielt ergänzen

---

## 📄 Lizenz / Nutzung

Im Repository ist keine ausführliche Lizenzsektion erkennbar. Für produktive oder kommerzielle Nutzung sollte die Lizenzlage im Projekt klar dokumentiert werden.

---

<div align="center">

## 🔥 NETSHIELD ist nicht nur eine Liste.
### Es ist ein automatisiertes Blocklist-Framework für echte Firewall-Workflows.

**Wenn dir das Projekt gefällt, nutze die Raw-Feeds direkt in deiner Firewall und beobachte die automatischen Updates über GitHub Actions.**

</div>
