# 🔐 Wazuh SIEM Homelab - Enterprise Security Operations

## 🎯 Overview
A production-ready Security Information and Event Management (SIEM) deployment using **Wazuh** for 24/7 threat detection, compliance monitoring, and incident response. This homelab simulates real SOC operations with live alerting, log correlation, and threat intelligence integration.

## 🔥 Why Wazuh?
- **Open Source** → No licensing costs, sustainable homelab
- **All-in-One** → SIEM + HIDS + FIM + Vulnerability Detection
- **Enterprise Features** → Custom rules, dashboards, API integrations
- **Production Proven** → Used by organizations worldwide

## 🛠️ Lab Components
1. **Wazuh Manager** - Centralized management & correlation
2. **Wazuh Agents** - Endpoint monitoring (Linux/Windows)
3. **Elastic Stack** - Kibana dashboards for visualization
4. **External Integrations** - VirusTotal, AlienVault OTX, AbuseIPDB

## 🚨 Incident Scenario: "Credential Harvesting Campaign"
Attackers use phishing emails to harvest credentials, then perform lateral movement and data exfiltration. Wazuh detects multiple stages of the attack chain.

## 📊 Key Capabilities Demonstrated
- **Real-time Log Analysis** - Syslog, Windows Event Logs, application logs
- **Custom Detection Rules** - XML-based rules for specific threats
- **File Integrity Monitoring** - Critical file change detection
- **Vulnerability Detection** - CVE scanning and reporting
- **Threat Intelligence** - Automated IOC ingestion and alerting

## 📁 Repository Structure
```
wazuh-siem-homelab/
├── README.md                          # Project overview
├── deployment/
│   ├── docker-compose.yml            # One-click deployment
│   └── install-wazuh.sh              # Manual install script
├── configs/
│   ├── custom-rules.xml              # Custom detection rules
│   ├── ossec.conf                    # Main configuration
│   └── decoders/                     # Custom log decoders
├── screenshots/
│   ├── wazuh-dashboard.png           # Security Events dashboard
│   ├── alerts-view.png               # Alert details
│   └── rules-configuration.png       # Rule management
├── incident-reports/
│   └── INCIDENT-2024-001.md          # Real incident investigated
├── integrations/
│   ├── virustotal-api.py             # Threat intel script
│   └── otx-feeder.sh                 # AlienVault OTX integration
└── docs/
    ├── architecture.md               # System design
    ├── detection-rules-guide.md      # How to write rules
    └── response-playbooks.md         # SOC procedures
```

👨‍💻 Author
Renaldi | Cloud Security SOC Analyst

