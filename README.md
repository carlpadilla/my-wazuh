# Intrusion Detection and Incident Response with Wazuh

## Project Overview

This project demonstrates a practical implementation of Wazuh, an open-source security monitoring tool, for intrusion detection and incident response within a virtualized environment. Leveraging a Proxmox server, this setup includes a dedicated Linux VM running Wazuh, monitoring three physical endpoints and a virtualized Plex media server. The primary goal is to enhance the security posture through real-time monitoring, threat detection, and effective incident response.

## Environment Setup

- **Proxmox VE**: Hosts the virtualized components of this environment, providing a robust and scalable platform for running the Linux server VM.
- **Linux Server VM**: A virtual machine running on Proxmox, dedicated to hosting the Wazuh manager, responsible for collecting and analyzing data from monitored endpoints.
- **Endpoints**: Three physical machines integrated with Wazuh agents, sending comprehensive monitoring data to the Wazuh manager for threat detection and alerting.
- **Plex Server**: A virtualized instance of Plex Media Server, also monitored by Wazuh to ensure the security of media content and accessibility.

## Key Components

- **Wazuh Manager**: Installed on the Linux VM, centralizes data processing and analysis, providing insights and alerts regarding potential security threats.
- **Wazuh Agents**: Deployed on each physical endpoint and the Plex server VM, these agents monitor system and application activities, reporting back to the Wazuh manager.
- **Proxmox VE**: Serves as the virtualization environment, hosting the Linux VM and the virtualized Plex server, facilitating easy management and scalability.

## Installation and Configuration

### Proxmox Server Setup

1. Install Proxmox VE on your server following the official [Proxmox Installation Guide](https://pve.proxmox.com/wiki/Installation).
2. Create a new VM within Proxmox for the Linux server, allocating sufficient resources based on your workload.

### Linux Server VM Setup

1. Install your preferred Linux distribution on the VM.
2. Follow the [Wazuh Manager Installation Guide](https://documentation.wazuh.com/current/installation-guide/wazuh-manager/index.html) to set up Wazuh on the VM.

### Endpoint Configuration

1. On each physical endpoint and the Plex server VM, install the Wazuh agent by following the [Wazuh Agent Installation Guide](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html).
2. Configure each agent to communicate with the Wazuh manager, ensuring data is sent for analysis.

### Plex Server VM Setup

1. Set up a new VM in Proxmox for the Plex Media Server.
2. Install Plex Media Server following the official [Plex Installation Guide](https://support.plex.tv/articles/200288586-installation/).
3. Configure the Wazuh agent to monitor Plex activities and report to the Wazuh manager.

## Usage

Once the setup is complete, the Wazuh manager will start receiving data from the agents. You can use the Wazuh dashboard to view alerts, analyze threats, and manage incident responses effectively. Regularly review the alerts and adjust your security policies as needed to mitigate identified risks.

