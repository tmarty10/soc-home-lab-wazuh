## Windows 11 Endpoint Setup

This section documents the configuration of the Windows 11 endpoint used in the Wazuh SOC home lab.

The Windows system is configured with the Wazuh agent which communicates with the Wazuh manager running on an Ubuntu server VM.

Environment:

Windows VM IP: 192.168.147.128
Ubuntu Wazuh Manager IP: 192.168.147.129
Agent Version: 4.14.3
Operating System: Windows 11 Enterprise
VM specs: 4GB Ram , 1 Processor , 2 Cores

Before installing the Wazuh agent, network connectivity between the Windows endpoint and the Wazuh manager was verified using ping and traceroute.

The results confirm successful communication between the two systems.

(insert ping screenshot)

Ports 1514 and 1515 are used by Wazuh agents to communicate with the manager.

Using Test-NetConnection confirmed that both ports are reachable from the Windows endpoint.

(port connectivity screenshot)

The Wazuh agent installer was downloaded from the official Wazuh repository.

File used: wazuh-agent-4.14.3-1.msi

(agent download screenshot)

The Wazuh agent was installed silently using the MSI installer and configured to connect directly to the Wazuh manager IP address.

(wazuh install screenshot

After installation the Wazuh service was started and verified using PowerShell.

The service status confirms the agent is running successfully.

(service running screenshot)

After the agent connected successfully, the Windows endpoint appeared in the Wazuh dashboard under the Endpoints section.

The agent status shows as Active indicating successful communication with the Wazuh manager.

(wazuh dashboard agent active ss)

The Windows 11 endpoint is now successfully connected to the Wazuh manager and ready for monitoring.

This endpoint will be used to generate security events and simulate attack scenarios for detection testing.






