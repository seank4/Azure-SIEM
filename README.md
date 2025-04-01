# Azure SIEM

## Objective

This project aimed to set up a cybersecurity monitoring and analysis environment on Azure. The goal is to create a virtual machine that acts as a honeypot, collect logs, and utilize Sentinel and Log Analytics to centralize and query security event data. Additionally, the project integrates geographic location data for log enrichment and builds an attack map for visualization.
### Skills Learned


- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Experience with Kusto Query Language (KQL)
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Azure for setting up resource group, virtual network, and virtual machine. 
- Security Information and Event Management system (Sentinel) for log ingestion and analysis.
- KQL for mapping IP addresses to geographical data.

### Result


![Attack Map](https://github.com/user-attachments/assets/7c4f2145-bdc5-43e6-a89e-424966996b88)




## Steps

### Part 1: Created the Honeypot (Azure Virtual Machine)

Created Windows 10 Virtual Machine:
The Azure portal was used to create a Windows 10 VM.

Configured Network Security:
The Network Security Group was modified to allow all inbound traffic, setting up the VM as a honeypot for simulated attacks.

Disabled Windows Firewall:
The firewall was disabled after logging into the VM, allowing unrestricted traffic.


### Part 2: Log Forwarding and KQL
Created Log Analytics Workspace:
A Log Analytics Workspace was set up and integrated with Azure Sentinel for centralized log aggregation.

Connected Security Events:
The "Windows Security Events via AMA" connector was configured to forward logs to Log Analytics.

Queried Logs:
KQL was used to query security logs for insights into failed login events.

### Part 3: Enriched Logs with Location Data
Imported Geographic Data:
A CSV file containing IP-to-location data was imported as a Sentinel Watchlist to enrich the logs with geographic information.

Queried Enriched Logs:
KQL was used to correlate IP addresses with geographic data, helping to identify the origin of attacks.

### Part 4: Created an Attack Map
Built Attack Map:
A Workbook was created in Sentinel with a query element and configured to display an attack map using JSON.

Visualized Attack Locations:
The attack map was used to visualize the geographic distribution of security events.

