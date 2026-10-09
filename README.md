# Netskope Log Analyzer

A zero-dependency, single-file HTML diagnostic tool for analyzing Netskope Client log bundles. Runs entirely in the browser — no installation, no server, no data transmitted.

---

## Quick Start

1. Download `netskope_log_analyzer_v1.23.2.html` (stable) or `index.html` (latest beta) from this repo.
2. Open the file in any modern browser (Chrome, Edge, Firefox, Safari).
3. Drop a Netskope Client log ZIP onto the drop zone.
4. Review findings, explore logs, and export a diagnostic report.

No account, no login, no internet connection required after download.

---

## Features

### Device Bar
A pinned header that persists across all tabs, showing the most important context at a glance:

| Chip | What it shows |
|---|---|
| HOST | Device hostname and OS version |
| USER | Authenticated user and tenant |
| CLIENT | Netskope Client version and release tag |
| TENANT | Tenant hostname |
| GATEWAY | Active PoP and tunnel status |
| STEERING | Steering configuration and traffic mode |
| FINDINGS | Count and severity of detected issues |
| LOG RANGE | Time span covered by the loaded logs |

### Tabs

| Tab | Purpose |
|---|---|
| 🔍 **Findings & Recommendations** | Detected issues ranked by severity with evidence links and recommended actions |
| 📊 **Log Summary** | Histogram, file inventory, and log-level breakdown |
| 📋 **Log Viewer** | Virtual-scroll log viewer with filter, regex, invert, and per-finding quick-jump |
| 🔄 **Traffic** | Steering events, bypass activity, and tunnel transitions |
| 🌐 **GSLB** | Gateway selection history and PoP switching analysis |
| 🔒 **NPA** | Private Access tunnel events and connectivity status |
| 🛡️ **EPDLP** | Endpoint DLP events extracted from client logs |
| 🤖 **AI Discovery** | AI app usage detected in steering logs |
| ⚡ **Flow Path** | Step-by-step connection flow visualization |
| 📈 **Timeline** | Event timeline and lifecycle strip |
| 🔬 **PCAP** | Packet capture summary (when included in log bundle) |
| ⚙️ **Config Files** | Raw config file viewer (steering, policy, device info) |
| 💻 **Device Details** | Enrollment status, network interfaces, DEM probes, and full system info |

### Findings Engine
- Pattern-based detection across all log files simultaneously
- GTF (Group Troubleshooting Framework) checks run alongside native patterns
- Findings are severity-ranked: Critical → High → Warning → Info
- Each finding card links directly to matching log lines via **↗ Log Viewer**
- Evidence is collapsed by default to keep the view clean

### Export
Generate a self-contained HTML diagnostic report from any loaded log bundle — includes Case Summary, all findings with severity, device info, enrollment state, network interfaces, EPDLP/SD-WAN/DEM sections, and the log file inventory. No external dependencies; the report opens in any browser.

---

## Branches

| Branch | Status | Description |
|---|---|---|
| `main` | **Stable** | Recommended for field use |
| `beta` | Development | Latest features; may contain work-in-progress |

Stable releases are tagged as `netskope_log_analyzer_vX.Y.Z.html` files in each branch. To roll back to a prior version, open the corresponding versioned file directly.

---

## Requirements

- A modern browser (Chrome 90+, Edge 90+, Firefox 88+, Safari 15+)
- A Netskope Client log bundle (ZIP exported from the client or collected via support tools)

No internet connection is required after downloading the tool. All analysis runs locally in your browser — no log data is ever uploaded or transmitted.

---

## Support

This tool is maintained by the Netskope SE team. For issues or feature requests, open a GitHub Issue on this repository.
