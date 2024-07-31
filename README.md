# Network Packet Analyzer with Dash Visualization

This project is a network packet analyzer that captures and analyzes network traffic in real-time. The data is visualized using Dash, providing insights into network behavior, traffic distribution, and protocol breakdowns. The tool supports filtering based on IP addresses, ports, and protocols.

## Features

- **Real-time packet capture and analysis**
- **Protocol-based filtering (TCP, UDP, or ALL)**
- **Source and destination IP filtering**
- **Source and destination port filtering**
- **Real-time data visualization using Dash**
- **Packet count and rate statistics**
- **Data saving in text format for offline analysis**

## Requirements

- Python 3.6+
- Libraries: `pandas`, `matplotlib`, `seaborn`, `scapy`, `dash`

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/network-analyzer.git
   cd network-analyzer
   ```
2. **Install the required libraries:**:
   ```bash
   pip install pandas matplotlib seaborn scapy dash
   ```
## Usage
Run the network analyzer script with optional command-line arguments to filter the traffic:
```bash
python network_analyzer.py --protocol TCP  # Capture only TCP packets
python network_analyzer.py --src_ip 192.168.1.1  # Filter by source IP
python network_analyzer.py --dst_port 80  # Filter by destination port
```
**Command-Line Arguments**
* --protocol: Filter by protocol (TCP, UDP, or ALL).
* --src_ip: Filter by source IP address.
* --dst_ip: Filter by destination IP address.
* --src_port: Filter by source port.
* --dst_port: Filter by destination port.

### Output without parameters
![Network Traffic Analyzer](https://github.com/Fathijem/Network-Traffic-Analyser/blob/27d095510220a8ce041d3e11a776273e58a8ff65/Sample%20Output/NA.jpg)

### Output with parameters
![Network Traffic Analyzer](https://github.com/Fathijem/Network-Traffic-Analyser/blob/6a4606de48c7676367cc0ea4081539f06ca7cfd2/Sample%20Output/NA2.jpg)

## Visualizing Data
After running the script, open a web browser and navigate to http://127.0.0.1:8050/ to view real-time visualizations of the captured traffic.
### Visualization for output without parameters
![Visualization for output without parameters](https://github.com/Fathijem/Network-Traffic-Analyser/blob/6a4606de48c7676367cc0ea4081539f06ca7cfd2/Sample%20Output/NA_visual.jpg)

### Visualization for output with parameters
![Visualization for output with parameters](https://github.com/Fathijem/Network-Traffic-Analyser/blob/6a4606de48c7676367cc0ea4081539f06ca7cfd2/Sample%20Output/NA_visual2.jpg)

## Data Storage
Captured packet data is saved in a text file packet_data.txt in the same directory as the script. Each line in the file represents a captured packet with its timestamp, source IP, destination IP, protocol, and length. You cant view the file using the below command:
```bash
cat packet_data.txt
```
![Packet Captured and stored in text file](https://github.com/Fathijem/Network-Traffic-Analyser/blob/6a4606de48c7676367cc0ea4081539f06ca7cfd2/Sample%20Output/output_view.jpg)

## Stopping the Analyzer
To stop the analyzer and close the Dash application, use Ctrl+C in the terminal.
