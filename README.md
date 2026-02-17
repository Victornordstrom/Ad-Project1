# Cisco Networking Project with Active Directory Server

This project demonstrates a complete network infrastructure setup integrating Cisco networking equipment with Windows Server Active Directory and DHCP services. The lab environment simulates an isolated enterprise network within a school environment.

## Project Overview

This is an enterprise-level networking project that combines:
- **Network Infrastructure**: Cisco router and switch for network connectivity
- **Directory Services**: Windows Server Active Directory (AD) for user and computer management
- **DHCP Services**: Dual DHCP configuration for both public and private network ranges
- **Network Isolation**: NAT implementation to isolate the project network from the school's main network

## Hardware Materials Used

- **Cisco 2960 Switch** - Layer 2 network switch for device connectivity
- **Cisco 2911 Router** - Enterprise router for WAN connectivity and NAT
- **Dell Server** - Windows Server running Active Directory and DHCP services

## Network Architecture

### Network Topology

```
School Main Network (10.0.0.0/24)
         |
         | (10.0.0.1)
         |
    [Cisco 2911 Router]
    (NAT - Isolation Boundary)
         |
    [Cisco 2960 Switch]
         |
    [Dell AD/DHCP Server]
         |
    [Client Devices]
```

![Network Setup Image 1](https://github.com/user-attachments/assets/023e6fd3-0082-478b-bb05-b351041786a1)

### Network Configuration Details

#### Router Configuration
- **Device**: Cisco 2911 Router
- **Connection to School**: Connected to school's main switch
- **WAN Interface**: Configured with DHCP to receive public IP from school's main network
- **Security**: NAT (Network Address Translation) implemented to isolate project network from school network
- **Purpose**: Gateway between school network and project network

![Network Setup Image 2](https://github.com/user-attachments/assets/dd9a6373-b4c6-4aeb-aab7-3e9fa47ddc2b)

#### Switch Configuration
- **Device**: Cisco 2960 Switch
- **Role**: Layer 2 network connectivity hub
- **Connected Devices**: Router, Server, and client machines

![Physical Network Setup](https://github.com/user-attachments/assets/129b7a50-efc9-4578-bc6f-8fa0de79ae41)

#### Server Configuration (Dell Server)
- **Operating System**: Windows Server
- **Primary Services**:
  - **Active Directory**: User authentication and network resource management
  - **DHCP Server**: Dynamic IP address assignment

- **Network Details**:
  - **Network Range**: 192.168.1.0/24
  - **DHCP Scope**: 192.168.1.100 - 192.168.1.200
  - **Gateway/AD Server IP**: 192.168.1.1 (typical configuration)
  - **School Network Gateway**: 10.0.0.1

##### Active Directory Setup

![Active Directory Configuration](https://github.com/user-attachments/assets/7f597350-ff1e-473d-97e3-fab01c90815f)

![AD Server View](https://github.com/user-attachments/assets/870a23f3-bea0-4fbd-b52e-159cf629ac22)

##### DHCP Configuration

![DHCP Server Setup](https://github.com/user-attachments/assets/d5d61453-61f8-415f-9895-db584acfa891)

## Key Features

 **Network Isolation** - NAT configuration protects school network from experimental changes
 **DHCP Management** - Automated IP assignment for client devices
 **Active Directory** - Centralized user and computer management
 **Enterprise Setup** - Mimics real-world corporate network architecture
 **Dual Network Access** - Devices can access both local AD services and school network resources

## Use Cases

This lab environment is ideal for:
- Learning enterprise networking concepts
- Understanding Active Directory implementation
- Practicing Cisco router and switch configuration
- Testing DHCP and network security policies
- Demonstrating network isolation techniques

## Network Access Points

- **School Network Gateway**: 10.0.0.1
- **Project Network**: 192.168.1.0/24
- **DHCP Range**: 192.168.1.100 - 192.168.1.200

## Additional Documentation

![Server Configuration 1](https://github.com/user-attachments/assets/c5400d58-b269-483d-a0b5-210e6a39afb5)

![Server Configuration 2](https://github.com/user-attachments/assets/9ba274bf-ed7a-4500-a8c9-2c8e7e59e0b1)
