# 🚀 Perodua Wireless Pentest Tool

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.7%2B-brightgreen)
![Platform](https://img.shields.io/badge/platform-Linux-lightgrey)

---

## 📝 Description
**Perodua Wireless Pentest Tool** is a Python-based utility for wireless network reconnaissance and pentesting.  
It automates tasks like enabling monitor mode, scanning wireless networks, enriching network data with manufacturer details, and exporting results to CSV.

---

## 🔧 Setup and Installation

### Prerequisites
- **OS:** Linux-based systems (e.g., Kali Linux)
- **Tools:** `airmon-ng`, `airodump-ng`
- **Python Version:** 3.7 or higher

### Installation Steps
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/perodua-wireless-pentest-tool.git
   cd perodua-wireless-pentest-tool

Install Dependencies Ensure airmon-ng and airodump-ng are installed:

  	```bash
    sudo apt update
    sudo apt install aircrack-ng
---

Download the OUI File Download the latest OUI data from IEEE:

---

    wget https://standards-oui.ieee.org/oui/oui.txt

---

Install Python Libraries Install required Python libraries:

    pip install pandas requests
    Run the Tool
  	python3 main.py

--- 

📚 Usage
Start the Tool: Run main.py to initiate the tool.
Welcome and IP Display: Displays a welcome message and fetches your external IP address.
Enable Monitor Mode: Automatically activates monitor mode on the wlan0 interface.
Scan Networks: Captures nearby wireless networks and their details.
Enrich Data: Maps BSSIDs to manufacturers using the OUI file.
Save Results: Outputs enriched data to detailed_ap_scan_results.csv.
Disable Monitor Mode: Restores the interface to its original state.
Output Details


--- 

The CSV file contains:

BSSID: Access Point Identifier.
Channel: Wireless channel in use.
Signal Power: Strength of the signal.
Encryption: Network privacy details.
Manufacturer: Derived from OUI data.

---

🖥️ Design Overview
Key Features:
Welcome Banner: Prints an ASCII art banner and displays the external IP.
Monitor Mode Management: Uses airmon-ng to enable/disable monitor mode.
Network Scanner: Executes airodump-ng for data collection.
Data Enrichment: Maps MAC prefixes to manufacturers using the OUI file.
CSV Export: Saves all results in a readable, enriched CSV format.


---

Code Flow:
Welcome and Setup: Displays info and initializes monitor mode.
Network Scanning: Captures raw wireless network data.
Data Parsing: Reads and validates the captured CSV.
Data Enrichment: Maps manufacturer information to BSSIDs.
Save and Cleanup: Outputs enriched results to a CSV and disables monitor mode.


---


🛡️ Future Enhancements
GUI Integration: Add a graphical interface for easier user interaction.
Advanced Pentesting: Include real-time attack simulations.
Data Formats: Support additional export formats like JSON and SQLite.
Real-Time Scanning: Add live visualization of network traffic.

---

⚖️ License
This project is licensed under the MIT License.
You can find the full license details in the LICENSE file.

--- 

🌟 Disclaimer
This tool is intended for educational and ethical use only.
Ensure you have explicit permission before using it for wireless network testing. Misuse of this tool may result in legal consequences.


### Instructions:
- Replace the placeholders (`logxtron`) with your own details.
- Save this as `README.md` in your repository.

Let me know if you need additional adjustments! 🚀





