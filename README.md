# Perodua Wireless Pentest Tool

## Description
Perodua Wireless Pentest Tool is a Python-based tool designed for network reconnaissance and pentesting. It utilizes `airmon-ng` and `airodump-ng` to monitor and scan wireless networks, parses scan results, and enriches them with manufacturer information derived from OUI data.

---

## Features
- **Monitor Mode Activation:** Enables monitor mode on a wireless network interface.
- **Network Scanning:** Captures wireless network details, including BSSID, channel, power, and ESSID.
- **Data Enrichment:** Maps BSSIDs to manufacturers using OUI data.
- **CSV Export:** Saves enriched network details to a detailed CSV file.
- **External IP Address Retrieval:** Identifies and displays the external IP address of the system.

---

## Requirements

### System Requirements
- **Operating System:** Linux-based system (e.g., Kali Linux)
- **Tools:** `airmon-ng`, `airodump-ng`
- **Python:** Version 3.7 or higher

### Python Libraries
Install the required libraries using `pip`:

```bash
pip install pandas requests
