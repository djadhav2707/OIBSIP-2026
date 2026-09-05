# Task 1 – Basic Network Scanning with Nmap

## Objective

The objective of this task is to perform a basic network scan on an authorized local device using Nmap, identify open ports and services, detect service versions, and identify the operating system.

## Tool Used

- Nmap 7.991
- Windows PowerShell
- Windows 11

- ## Target

The scan was performed only on my own local device.

- Target IP: `192.168.0.224`
- Network: Local Wi-Fi network
- Authorization: Own device / authorized system

## Nmap Installation

Nmap was downloaded from the official Nmap website and installed on Windows.

The installation included Nmap and Npcap.

The installation was verified using:
```powershell
nmap --version

The scan also showed 995 closed TCP ports.

## Service and Version Detection

The following command was used:

```powershell
nmap -sV 192.168.0.224

## Operating System Detection

The following command was used:

```powershell
nmap -O 192.168.0.224


The scan identified the target operating system as:

- Operating System: Microsoft Windows 11
- OS Details: Microsoft Windows 11 24H2 - 25H2
- Network Distance: 0 hops

## Open Ports and Services

The scan identified the following open TCP ports:

| Port | Service | Version / Details |
|---|---|---|
| 135/tcp | msrpc | Microsoft Windows RPC |
| 139/tcp | netbios-ssn | Microsoft Windows netbios-ssn |
| 445/tcp | microsoft-ds | Microsoft Windows SMB-related service |
| 3306/tcp | mysql | MySQL (unauthorized version detection) |
| 25734/tcp | unknown | Service not identified |

## Risk Analysis

The open ports identified during the scan may provide network services that should be protected and exposed only when required.

- **Port 135 (MSRPC):** Used by Windows RPC services. If unnecessarily exposed, it can increase the attack surface.
- **Port 139 (NetBIOS):** Used for older Windows network communication. It should be restricted when not required.
- **Port 445 (SMB):** Used for Windows file and printer sharing. SMB exposure can increase security risk if improperly configured.
- **Port 3306 (MySQL):** Used by the MySQL database service. Database ports should not be unnecessarily exposed to untrusted networks.
- **Port 25734 (Unknown):** Nmap could not identify the service. The service should be investigated and disabled if it is not required.

## Security Recommendations

1. Keep Windows and installed services updated with security patches.
2. Use Windows Firewall to restrict unnecessary inbound connections.
3. Disable services and ports that are not required.
4. Restrict SMB and database access to trusted systems only.
5. Investigate the unknown service running on port 25734.
6. Use strong authentication and secure configurations for network services.

## Conclusion

Nmap successfully identified the open ports, services, and operating system information of the authorized local target. The scan demonstrates how network scanning can help identify exposed services and potential security risks. Unnecessary services should be disabled and required services should be protected using firewall rules and secure configurations.
