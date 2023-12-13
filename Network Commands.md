# Network Commands CheatSheet for Sysadmins

This is a **CheatSheet** README.md file that provides information on common network commands used by system administrators on **Linux**, **PowerShell**, and **Command Prompt**.

# Table of Contents
1. [Ping](#1-ping)
2. [Traceroute](#2-traceroute)
3. [Netstat](#3-netstat)
4. [Nmap](#4-nmap)
5. [IPConfig](#5-ipconfig)
6. [NSLookup](#6-nslookup)
7. [Route](#7-route)
8. [Test-Connection](#8-test-connection)
9. [Telnet](#9-telnet)
10. [Curl/Wget](#10-curlwget)

## 1. Ping

#### **Purpose**: Ping is used to test the reachability of a host on an Internet Protocol (IP) network. It sends ICMP echo requests to the destination and waits for responses, providing information about network connectivity and round-trip time.

### 1.1 Linux
- **Usage:** `ping <hostname or IP>`
- **Description:** Sends ICMP echo requests to a destination.

```bash
ping google.com
```

### 1.2 PowerShell
- **Usage**: `Test-Connection -ComputerName <hostname or IP>`
- **Description**: Tests network connectivity using ICMP.

```powershell
Test-Connection -ComputerName google.com
```

### 1.3 Command Prompt
- **Usage**: `ping <hostname or IP>`
- **Description**: Sends ICMP echo requests to a destination.

```cmd
ping google.com
```

## 2. Traceroute

#### **Purpose**: Traceroute is used to trace the route that packets take to reach a destination host. It shows the IP addresses of the routers along the path and measures the time taken for each hop, helping diagnose network issues.

### 2.1 Linux
- **Usage**: `traceroute <hostname or IP>`
- **Description**: Displays the route and measures transit delays to a destination.

```bash
traceroute google.com
```

### 2.2 PowerShell
- **Usage**: `Test-NetConnection -TraceRoute -ComputerName <hostname or IP>`
- **Description**: Traces the route to a destination.
```powershell
Test-NetConnection -TraceRoute -ComputerName google.com
```
### 2.3 Command Prompt
- **Usage**: `tracert <hostname or IP>`
- **Description**: Displays the route and measures transit delays to a destination.
```cmd
tracert google.com
```

## 3. Netstat

#### **Purpose**: Netstat is a command-line tool that provides information about network connections, routing tables, interface statistics, masquerade connections, and multicast memberships. It helps administrators monitor and troubleshoot network-related issues.

### 3.1 Linux
- **Usage**: `netstat -an`
- **Description**: Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
```bash
netstat -an
```
### 3.2 PowerShell
- **Usage**: `Get-NetTCPConnection`
- **Description**: Retrieves information about TCP connections.
```powershell
Get-NetTCPConnection
```
### 3.3 Command Prompt
- **Usage**: `netstat -an`
- **Description**: Displays active network connections.
```cmd
netstat -an
```
## 4. Nmap

#### **Purpose**: Nmap is a powerful network scanning tool used to discover hosts and services on a computer network, creating a map of the network. It can identify open ports, services running, and other details, aiding in security assessments.

### 4.1 Linux
- **Usage**: `nmap <hostname or IP>`
- **Description**: Scans a target for open ports and services.
```bash
nmap google.com
```
### 4.2 PowerShell
- **Usage**: `Test-NetConnection -ComputerName <hostname or IP> -Port <port>`
- **Description**: Tests network connectivity to a specific port.
```powershell
Test-NetConnection -ComputerName google.com -Port 80
```
### 4.3 Command Prompt
- **Usage**: `nmap <hostname or IP>`
- **Description**: Scans a target for open ports and services.
```cmd
nmap google.com
```
## 5. IPConfig

#### **Purpose**: IPConfig (on Windows) or ifconfig (on Linux) displays information about the network interfaces on a system. It shows IP addresses, subnet masks, gateway addresses, and other details, assisting in network configuration and troubleshooting.

### 5.1 Linux
- **Usage**: `ifconfig`
- **Description**: Displays network interface configuration.
```bash
ifconfig
```
### 5.2 PowerShell
- **Usage**: `Get-NetIPAddress`
- **Description**: Retrieves IP address configuration.
```powershell
Get-NetIPAddress
```
### 5.3 Command Prompt
- **Usage**: `ipconfig`
- **Description**: Displays IP configuration for all interfaces.
```cmd
ipconfig
```
## 6. NSLookup

#### **Purpose**: NSLookup is used to query DNS servers to obtain domain name or IP address information. It helps resolve domain names to IP addresses and vice versa, aiding in DNS-related troubleshooting.

### 6.1 Linux
- **Usage**: `nslookup <hostname or IP>`
- **Description**: Queries DNS servers for information about a domain.
```bash
nslookup google.com
```
### 6.2 PowerShell
- **Usage**: `Resolve-DnsName -Name <hostname or IP>`
- **Description**: Resolves DNS names to IP addresses.
```powershell
Resolve-DnsName -Name google.com
```
### 6.3 Command Prompt
- **Usage**: `nslookup <hostname or IP>`
- **Description**: Queries DNS servers for information about a domain.
```cmd
nslookup google.com
```
## 7. Route

#### **Purpose**: The route command displays and manipulates the IP routing table. It shows the routing information for the system, including the destination network, gateway, and interface, helping manage network traffic.

### 7.1 Linux
- **Usage**: `route -n`
- **Description**: Displays and manipulates the IP routing table.
```bash
route -n
```
### 7.2 PowerShell
- **Usage**: `Get-NetRoute`
- **Description**: Retrieves information about IP routing tables.
```powershell
Get-NetRoute
```
### 7.3 Command Prompt
- **Usage**: `route print`
- **Description**: Displays the IP routing table.
```cmd
route print
```
## 8. Test-Connection

#### **Purpose**: Test-Connection is a PowerShell cmdlet that tests network connectivity using ICMP. It provides a simple way to check if a remote host is reachable and measure the round-trip time.

### 8.1 Linux (using PowerShell Core)
- **Usage**: `Test-Connection -ComputerName <hostname or IP>`
- **Description**: Tests network connectivity using ICMP.
```powershell
Test-Connection -ComputerName google.com
```
### 8.2 PowerShell
- **Usage**: `Test-Connection -ComputerName <hostname or IP>`
- **Description**: Tests network connectivity using ICMP.
```powershell
Test-Connection -ComputerName google.com
```
### 8.3 Command Prompt
- **Usage**: `ping <hostname or IP>`
- **Description**: Sends ICMP echo requests to a destination.
```cmd
ping google.com
```

## 9. Telnet

#### **Purpose**: Telnet is a network protocol used to establish a bidirectional interactive text-oriented communication session. It is often used to check if a specific port on a remote host is open or for debugging network services

### 9.1 Linux
- **Usage**: `telnet <hostname or IP> <port>`
- **Description**: Connects to a remote host using the Telnet protocol.
```bash
telnet google.com 80
```
### 9.2 PowerShell
- **Usage**: `New-Object System.Net.Sockets.TcpClient("<hostname or IP>", <port>)`
- **Description**: Creates a TCP connection to a remote host.
```powershell
$client = New-Object System.Net.Sockets.TcpClient("google.com", 80)
```
### 9.3 Command Prompt
- **Usage**: `telnet <hostname or IP> <port>`
- **Description**: Connects to a remote host using the Telnet protocol.
```cmd
telnet google.com 80
```

## 10. Curl/Wget

#### **Purpose (Curl)**: Curl is a command-line tool for transferring data with URLs. It supports various protocols, including HTTP, HTTPS, FTP, FTPS, SCP, SFTP, and more, making it versatile for downloading or uploading data from the command line.
#### **Purpose (Wget)**: Wget is a command-line utility for downloading files from the web. It supports HTTP, HTTPS, and FTP protocols and can recursively download entire directories, making it useful for batch downloads.

### 10.1 Linux
- **Usage** `(Curl): curl <URL>`
- **Description**: Downloads content from a URL.
```bash
curl https://example.com/file.txt
```
- **Usage** `(Wget): wget <URL>`
- **Description**: Downloads content from a URL.
```bash
wget https://example.com/file.txt
```
### 10.2 PowerShell
- **Usage**: `Invoke-WebRequest -Uri <URL>`
- **Description**: Downloads content from a URL.
```powershell
Invoke-WebRequest -Uri https://example.com/file.txt
```
### 10.3 Command Prompt
- **Usage** (Curl): Not available by default. Can be installed separately.
- **Usage** (Wget): Not available by default. Can be installed separately.
```cmd
# For Wget, you need to install it separately.
```


## Author / Contributor
These snippets were gathered and organized by **Vladimir Balabanov** / **Grrr1337** .

