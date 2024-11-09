Monitoring Stack Setup - README.md
This document describes the setup of a monitoring stack consisting of Prometheus, Alertmanager, Grafana, and Node Exporter. The components are deployed on a machine with a static IP address of 192.168.1.12.

Accessing Services
Node Exporter: http://192.168.1.12:9100/
Alertmanager: http://192.168.1.12:9093/
Prometheus: http://192.168.1.12:9091/
Grafana: http://192.168.1.12:3001/
Note: Default credentials for Grafana might be required depending on the installation method.

Static IP Configuration
The machine has a static IP address assigned using the nmcli command. The configuration details are provided below:

IP Address: 192.168.1.12/24
Gateway: 192.168.1.1
DNS Servers: 8.8.8.8, 8.8.4.4
Important: This information reflects the specific setup on this machine. You might need to adjust these details based on your network configuration.

Assigning Static IP with nmcli (For reference)
The following commands were used to assign the static IP address using nmcli. While these commands are included for reference, it's recommended to modify network configurations through your preferred method (e.g., network manager GUI).

nmcli connection show  # Display available network connections
nmcli connection up static  # Activate the connection named "static"
nmcli connection mod static autoconnect yes  # Set the "static" connection to automatically connect on boot