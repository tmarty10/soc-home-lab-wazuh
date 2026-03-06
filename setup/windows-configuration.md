## Windows 11 Endpoint Setup

This section documents the configuration of the Windows 11 endpoint used in the Wazuh SOC home lab.

The Windows system is configured with the Wazuh agent which communicates with the Wazuh manager running on an Ubuntu server VM.

## Environment Configuration

Environment:

Windows VM IP: 192.168.147.128
Ubuntu Wazuh Manager IP: 192.168.147.129
Agent Version: 4.14.3
Operating System: Windows 11 Enterprise
VM specs: 4GB Ram , 1 Processor , 2 Cores

## Network Connectivity Verification

Before installing the Wazuh agent, network connectivity between the Windows endpoint and the Wazuh manager was verified using ping and traceroute.

The results confirm successful communication between the two systems.

![Ubuntu Ping](windows-screenshots/ubuntu-ping.png)

## Wazuh Agent Port Connectivity Test

Ports 1514 and 1515 are used by Wazuh agents to communicate with the manager.

Using Test-NetConnection confirmed that both ports are reachable from the Windows endpoint.

![Port Connectivity](windows-screenshots/wazuh-ports.png)

## Downloading/Installing the Wazuh Agent

The Wazuh agent installer was downloaded from the official Wazuh repository online.

File used: wazuh-agent-4.14.3-1.msi

The Wazuh agent was installed silently using the MSI installer and configured to connect directly to the Wazuh manager IP address.

![Wazuh Agent Install](windows-screenshots/windows-agent-install.png)

## Verifying Wazuh Agent Service

After installation the Wazuh service was started and verified using PowerShell.

The service status confirms the agent is running successfully.

(service running screenshot)

## Agent Registration in Wazuh Dashboard

After the agent connected successfully, the Windows endpoint appeared in the Wazuh dashboard under the Endpoints section.

The agent status shows as Active indicating successful communication with the Wazuh manager.

![Wazuh Agent Active](windows-screenshots/wazuh-dashboard-with-windows.png)

## Verifying Windows Event Log Collection



(insert screenshot verifying windows logs are being collected by the agent. eventvwr)

The Windows 11 endpoint is now successfully connected to the Wazuh manager and ready for monitoring.

This endpoint will be used to generate security events and simulate attack scenarios for detection testing.







