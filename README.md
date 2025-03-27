Shadow IoT Scanner
Version
License

A specialized network monitoring tool that discovers and secures unauthorized IoT devices on your network before they become security vulnerabilities.

Overview
Shadow IoT Scanner is a comprehensive security solution designed to detect, identify, and secure IoT devices that may otherwise remain hidden in your network infrastructure. Using passive scanning techniques, device fingerprinting, and behavioral analysis, it provides visibility into all connected IoT devices and helps enforce appropriate security policies.

Key Features
Passive Network Scanning: Identifies all connected devices without disrupting network operations
Device Fingerprinting: Accurately identifies device manufacturers, models, and firmware versions
Risk Classification: Assigns risk scores based on device type, vulnerabilities, and behavior
Automatic Policy Enforcement: Applies appropriate security controls to discovered devices
Vulnerability Assessment: Checks devices against known IoT vulnerability databases
Behavioral Anomaly Detection: Identifies unusual device activities that may indicate compromise
Network Segmentation Recommendations: Suggests optimal network isolation strategies
SIEM Integration: Seamlessly forwards device discovery and security events to existing security platforms
Installation
Prerequisites
Ruby 2.7+
Libpcap development libraries
Network access with appropriate permissions
YAML for configuration
Basic Installation
bash

Hide
# Install required system libraries
sudo apt-get install libpcap-dev ruby-dev

# Install required gems
gem install pcap ipaddr mqtt rest-client yaml

# Clone the repository
git clone https://github.com/yourusername/shadow-iot-scanner.git
cd shadow-iot-scanner

# Configure your environment
cp config.example.yml config.yml
# Edit config.yml with your network settings

# Run the scanner
ruby shadow_iot_scanner.rb
Configuration
Shadow IoT Scanner uses a YAML configuration file with the following key sections:

yaml

Hide
# Network interfaces to monitor
network_interfaces:
  - eth0
  - wlan0

# Enable/disable scanning methods
enable_passive_scanning: true
enable_active_scanning: false
enable_mdns_scanning: true
enable_upnp_scanning: true
enable_mqtt_scanning: true

# Device database path
device_db_path: "data/device_fingerprints.json"

# Vulnerability database path
vulnerability_db_path: "data/vulnerability_db.json"

# Authorized devices (whitelist)
authorized_devices:
  - mac_address: "00:11:22:33:44:55"
    name: "Conference Room Camera"
  - mac_address: "AA:BB:CC:DD:EE:FF"
    name: "Smart Thermostat"

# SIEM integration
siem:
  enabled: true
  endpoint: "https://your-siem-server.com/api/events"
  api_key: "your-api-key-here"

# Security policies
policies:
  - name: "High Risk Isolation"
    priority: 1
    device_types: ["camera", "microphone"]
    risk_levels: ["high"]
    network_control: "isolate"
    enhanced_monitoring: true
    alert_threshold: "medium"
    remediation_action: "notify_admin"

# Logging configuration
log_file: "logs/scanner.log"
log_level: "info"
Usage
Basic Usage
bash

Hide
ruby shadow_iot_scanner.rb
Running as a Service
To run Shadow IoT Scanner as a system service:

bash

Hide
# Install as a systemd service
sudo cp shadow-iot-scanner.service /etc/systemd/system/
sudo systemctl enable shadow-iot-scanner
sudo systemctl start shadow-iot-scanner

# Check service status
sudo systemctl status shadow-iot-scanner
Generating Reports
bash

Hide
# Generate a comprehensive IoT device report
ruby shadow_iot_scanner.rb --report > iot_report.json

# Generate a security recommendations report
ruby shadow_iot_scanner.rb --recommendations > recommendations.txt
Use Cases
Healthcare Facilities: Discover and secure medical IoT devices
Smart Buildings: Monitor and control building automation systems
Manufacturing Facilities: Protect industrial IoT devices from compromise
Enterprise Networks: Identify and secure employee-owned IoT devices
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Ruby Pcap library contributors
IoT Security Foundation
OWASP IoT Security Verification Standard
