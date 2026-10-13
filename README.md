# Netskope Log Analyzer

A zero-dependency, single-file HTML diagnostic tool for analyzing Netskope Client log bundles. Runs entirely in the browser — no installation, no server, no data transmitted.

---

## Quick Start

1. Go to the **[`main` branch](../../tree/main)** for the stable release, or **[`beta`](../../tree/beta)** for the latest development version.
2. Download **`index.html`** from whichever branch you want.
3. Open it in any modern browser (Chrome, Edge, Firefox, Safari).
4. Drop a Netskope Client log ZIP onto the drop zone.

`index.html` is always the current version of that branch. Prior releases are archived in the [`releases/`](releases/) folder.

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
Generate a self-contained HTML diagnostic report from any loaded log bundle — includes Case Summary, all findings with severity, device info, enrollment state, network interfaces, EPDLP/SD-WAN/DEM sections, and the log file inventory.

---

## Repository Structure

```
index.html          ← current version of this branch (download this)
releases/           ← archived prior releases (netskope_log_analyzer_vX.Y.Z.html)
```

The `main` branch always contains the latest stable release. The `beta` branch contains active development. Prior versions in `releases/` are provided for rollback — download the specific file and open it directly in your browser.

---

## Requirements

- A modern browser (Chrome 90+, Edge 90+, Firefox 88+, Safari 15+)
- A Netskope Client log bundle (ZIP exported from the client or collected via support tools)

No internet connection is required after downloading the tool. All analysis runs locally — no log data is ever uploaded or transmitted.

---

## License

Apache 2.0 — see [LICENSE](LICENSE).

---

## Support

This tool is maintained by the Netskope SE team. For issues or feature requests, open a GitHub Issue on this repository.
