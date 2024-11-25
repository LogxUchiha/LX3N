# 🚀 Perodua Wireless Pentest Tool

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.7%2B-brightgreen)
![Platform](https://img.shields.io/badge/platform-Linux-lightgrey)

---

## 📝 Description
**Perodua Wireless Pentest Tool** is a powerful Python-based utility designed for wireless network reconnaissance and pentesting.  
It leverages **airmon-ng** and **airodump-ng** to capture wireless network data, processes it into readable formats, and enriches it with manufacturer information derived from OUI data.

---

## ✨ Features
- **🎛️ Monitor Mode Activation:** Easily switch your wireless interface to monitor mode.
- **📡 Network Scanning:** Capture details like BSSID, channel, signal power, and encryption.
- **🏭 Manufacturer Enrichment:** Map MAC prefixes to manufacturers using IEEE OUI data.
- **📊 CSV Export:** Save enriched results to a structured CSV file.
- **🌐 External IP Address:** Automatically fetch your external IP address.

---

## 🛠️ Requirements

### System Requirements
- **OS:** Linux-based systems (e.g., Kali Linux)
- **Tools:** `airmon-ng`, `airodump-ng`
- **Python Version:** 3.7 or higher

### Python Libraries
Install dependencies with:
```bash
pip install pandas requests

### 🔧 Setup and Installation
Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/perodua-wireless-pentest-tool.git
cd perodua-wireless-pentest-tool
Install Dependencies Ensure airmon-ng and airodump-ng are installed:

bash
Copy code
sudo apt update
sudo apt install aircrack-ng
Download the OUI File Download the latest OUI data from IEEE:

bash
Copy code
wget https://standards-oui.ieee.org/oui/oui.txt
Run the Tool

bash
Copy code
python3 main.py


