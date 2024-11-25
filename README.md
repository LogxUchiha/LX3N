<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perodua Wireless Pentest Tool</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }
        h1, h2 {
            color: #007acc;
        }
        code {
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            padding: 2px 4px;
            border-radius: 3px;
        }
        pre {
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            padding: 10px;
            overflow-x: auto;
            border-radius: 5px;
        }
        a {
            color: #007acc;
        }
    </style>
</head>
<body>
    <h1>Perodua Wireless Pentest Tool</h1>

    <h2>Description</h2>
    <p>Perodua Wireless Pentest Tool is a Python-based tool designed for network reconnaissance and pentesting. It utilizes <code>airmon-ng</code> and <code>airodump-ng</code> to monitor and scan wireless networks, parses scan results, and enriches them with manufacturer information derived from OUI data.</p>

    <h2>Features</h2>
    <ul>
        <li>Monitor Mode Activation: Enables monitor mode on a wireless network interface.</li>
        <li>Network Scanning: Captures wireless network details, including BSSID, channel, power, and ESSID.</li>
        <li>Data Enrichment: Maps BSSIDs to manufacturers using OUI data.</li>
        <li>CSV Export: Saves enriched network details to a detailed CSV file.</li>
        <li>External IP Address Retrieval: Identifies and displays the external IP address of the system.</li>
    </ul>

    <h2>Requirements</h2>
    <h3>System Requirements</h3>
    <ul>
        <li>Operating System: Linux-based system (e.g., Kali Linux)</li>
        <li>Tools: <code>airmon-ng</code>, <code>airodump-ng</code></li>
        <li>Python: Version 3.7 or higher</li>
    </ul>

    <h3>Python Libraries</h3>
    <pre><code>pip install pandas requests</code></pre>

    <h2>Setup and Installation</h2>
    <ol>
        <li>
            <strong>Clone the Repository</strong>
            <pre><code>git clone https://github.com/yourusername/perodua-wireless-pentest-tool.git
cd perodua-wireless-pentest-tool</code></pre>
        </li>
        <li>
            <strong>Ensure Dependencies</strong>
            <p>Ensure that <code>airmon-ng</code> and <code>airodump-ng</code> are installed and available in your PATH.</p>
            <pre><code>sudo apt update
sudo apt install aircrack-ng</code></pre>
        </li>
        <li>
            <strong>Download the OUI File</strong>
            <p>Download the OUI data file from the IEEE standards website:</p>
            <pre><code>wget https://standards-oui.ieee.org/oui/oui.txt</code></pre>
        </li>
        <li>
            <strong>Run the Tool</strong>
            <pre><code>python3 main.py</code></pre>
        </li>
    </ol>

    <h2>Usage</h2>
    <p>Start the tool, and it will:</p>
    <ul>
        <li>Display a welcome banner and your external IP address.</li>
        <li>Start monitor mode on the default wireless interface (<code>wlan0</code>).</li>
        <li>Scan wireless networks for a specified duration.</li>
        <li>Parse the results and enrich them with manufacturer data.</li>
        <li>Save the results to <code>detailed_ap_scan_results.csv</code>.</li>
        <li>Stop monitor mode after the operation.</li>
    </ul>
    <p>The output CSV file includes details such as:</p>
    <ul>
        <li>BSSID</li>
        <li>Channel</li>
        <li>Signal Power</li>
        <li>Privacy Settings</li>
        <li>Manufacturer (Enriched using OUI)</li>
    </ul>

    <h2>Design</h2>
    <h3>Modules Overview</h3>
    <ul>
        <li><strong>Banner and Welcome:</strong> ASCII art is displayed at the start for branding and user engagement.</li>
        <li><strong>External IP Retrieval:</strong> Uses <code>requests</code> to fetch the system's external IP address via the ipify API.</li>
        <li><strong>Monitor Mode Management:</strong> Handles enabling and disabling monitor mode using <code>airmon-ng</code>.</li>
        <li><strong>Network Scanning:</strong> Executes <code>airodump-ng</code> to capture network data and saves it as a CSV.</li>
        <li><strong>Data Parsing and Enrichment:</strong> Parses the CSV file, validates necessary columns, and enriches it with manufacturer data using the OUI file.</li>
        <li><strong>Manufacturer Mapping:</strong> Processes the OUI file to map MAC address prefixes to manufacturers.</li>
        <li><strong>Output:</strong> Saves enriched scan results to a CSV file for further analysis.</li>
    </ul>

    <h2>Future Enhancements</h2>
    <ul>
        <li>Add graphical output or a web interface for easier interaction.</li>
        <li>Incorporate network attack simulations for advanced pentesting.</li>
        <li>Add support for additional file formats like JSON or SQLite.</li>
    </ul>

    <h2>Contributing</h2>
    <p>Contributions are welcome! Feel free to fork the repository, create feature branches, and submit pull requests.</p>

    <h2>License</h2>
    <p>This project is licensed under the MIT License. See the LICENSE file for details.</p>

    <h2>Disclaimer</h2>
    <p><strong>This tool is intended for educational and ethical use only.</strong> Ensure you have explicit permission before using it for wireless network testing. Misuse of this tool can result in legal consequences.</p>
</body>
</html>
