# Suricata Intrusion Prevention System Setup

![Project Image](https://github.com/ma7mouddiaa/Suricata-Inline-IPS-Setup/blob/main/screenshot/unknown_2023.10.18-15.05.png)
![Project Image](https://github.com/ma7mouddiaa/Suricata-Inline-IPS-Setup/blob/main/screenshot/unknown_2023.10.12-12.02.png)

**Configuring Suricata IPS on Ubuntu Server for Enhanced Network Security**

I successfully configured Suricata as an Intrusion Prevention System (IPS) on an Ubuntu server in this project. The setup involved isolating Metasploitable machines in a private network (HOME_NET) while having a Kali Linux machine as the external network (EXTERNAL_NET). I then configured Suricata to operate in inline mode, forwarding and routing network traffic between these environments. Utilizing Suricata rules, I enforced security measures like blocking attempts to access the Tomcat admin page and alerting on telnet connections from the external network.

## Table of Contents

- [Introduction](#introduction)
- [Project Architecture](#project-architecture)
- [Setup and Configuration](#setup-and-configuration)
- [Testing](#testing)
- [Data Analysis with JQ](#data-analysis-with-jq)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Network security is a paramount concern, and this project aims to bolster security by implementing an Intrusion Prevention System using Suricata. The IPS is set up in inline mode to actively monitor and block suspicious activity, ensuring a more secure network environment.

## Project Architecture

The project's architecture is designed to simulate a real-world network with isolated segments:

- **HOME_NET (192.168.190.0/24):**
  - Metasploitable machines (Metasploitable 2 and 3) form this isolated internal network.

- **EXTERNAL_NET (10.0.2.0/24):**
  - Kali Linux machine representing the external network, isolated from HOME_NET.

- **Ubuntu Server with Suricata:**
  - Configured as a router to forward traffic between HOME_NET and EXTERNAL_NET, operating as an Intrusion Prevention System (IPS) in inline mode.

## Setup and Configuration

To set up Suricata as an IPS and configure the network:

1. **Network Setup:**
   - Configure VMs (Metasploitable 2, Metasploitable 3, Kali Linux) and Ubuntu server.
   - Isolate HOME_NET and EXTERNAL_NET according to specified IP ranges.

2. **Suricata Installation:**
   - Install and configure Suricata on the Ubuntu server.

3. **IPS Configuration:**
   - Set up Suricata in inline mode to monitor and prevent suspicious activities.
   - ![configration-File](https://github.com/ma7mouddiaa/Suricata-Inline-IPS-Setup/blob/main/screenshot/unknown_2023.10.16-11.23.png)
   - Define rules to block unauthorized access and generate alerts for specific activities.

## Testing

To verify the IPS setup and functionality:

1. **Testing Rules:**
   - Test rules to block access to the Tomcat admin page and detect telnet connections from the external network.
   -![Before-Rule](https://github.com/ma7mouddiaa/Suricata-Inline-IPS-Setup/blob/main/screenshot/unknown_2023.10.15-14.26.png)
   -![After-Rule](https://github.com/ma7mouddiaa/Suricata-Inline-IPS-Setup/blob/main/screenshot/unknown_2023.10.15-15.56_1.png)
  

2. **Ping Tests:**
   - Conduct ping tests to verify network connectivity between the different environments.

## Installing Rules from Emerging Threats
1. **Emerging Threats Rules:** rules.emergingthreats.net/open/suricata/rules/
2. ![one rule is blocking Nmap-scan!](https://github.com/ma7mouddiaa/Suricata-Inline-IPS-Setup/blob/main/screenshot/unknown_2023.10.16-11.30.png)




## Data Analysis with JQ

Utilizing JQ to query the EVE.json log file generated by Suricata, explore custom output types, and analyze the logged data for potential security events.


## Contributing

Contributions to improve and extend this project are welcome! If you have suggestions, ideas, or would like to contribute, please reach out https://www.linkedin.com/comm/in/mahmoud-diaa-cybersamurai

## License

This project is licensed under the [MIT License](LICENSE).
