<!-- Networking -->
# Computer Networks
## Overview
what is networking?
- Networking is the practice of connecting computers and other devices together to share resources and information. It involves the design, implementation, and management of networks, including both hardware and software components.
- Networking enables communication between devices, allowing them to exchange data, access shared resources, and collaborate on tasks.
## Key Concepts
- **Network Types**: Understanding the different types of networks (e.g., LAN, WAN, MAN) and their use cases.
- **Protocols**: Familiarity with networking protocols (e.g., TCP/IP, HTTP, FTP) that govern data transmission.
- **IP Addressing**: Knowledge of IP addressing schemes (e.g., IPv4, IPv6) and subnetting.
- **Network Devices**: Awareness of various network devices (e.g., routers, switches, firewalls) and their roles.
- **Security**: Understanding network security principles, including encryption, VPNs, and firewalls.
## Network layers and OSI model:
- **Physical Layer**: The physical medium for data transmission (e.g., cables, wireless signals).
- **Data Link Layer**: Responsible for node-to-node data transfer and error detection (e.g., Ethernet).
- **Network Layer**: Handles routing and forwarding of data packets (e.g., IP).
- **Transport Layer**: Ensures reliable data transfer and error recovery (e.g., TCP, UDP).
- **Session Layer**: Manages sessions and controls the dialog between applications (e.g., NetBIOS).
- **Presentation Layer**: Transforms data for the application layer, handling encryption and compression (e.g., SSL/TLS).
- **Application Layer**: Provides network services to end-user applications (e.g., HTTP, FTP, DNS).

## Common Protocols:
- **TCP/IP**: The fundamental protocol suite for internet communication, consisting of Transmission Control Protocol (TCP) and Internet Protocol (IP).
- **HTTP/HTTPS**: Hypertext Transfer Protocol (Secure) used for web communication.
- **FTP/SFTP**: File Transfer Protocol (Secure) for transferring files over a network.
- **DNS**: Domain Name System, which translates domain names into IP addresses.
- **DHCP**: Dynamic Host Configuration Protocol, which automatically assigns IP addresses to devices on a network.
- **SMTP/POP3/IMAP**: Protocols for sending and receiving email (Simple Mail Transfer Protocol, Post Office Protocol, Internet Message Access Protocol).

## Devices:
- **Router**: A device that forwards data packets between computer networks, directing traffic on the internet.
- **Switch**: A device that connects devices within a single network, allowing them to communicate efficiently.
- **Firewall**: A security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
- **Access Point**: A device that allows wireless devices to connect to a wired network using Wi-Fi.
- **Modem**: A device that modulates and demodulates signals for data transmission over telephone lines or cable systems.
- **Network Interface Card (NIC)**: A hardware component that connects a computer to a network, enabling communication over the network.
- **Repeater**: A device that amplifies or regenerates signals to extend the range of a network.
- **Bridge**: A device that connects two or more network segments, allowing them to function as a single network.
- **Hub**: A basic networking device that connects multiple devices in a network, allowing them to communicate as a single network segment.
<!-- About intranet and firewall -->
## Intranet and Firewall
- **Intranet**: A private network that uses internet protocols and technologies to share information within an organization. It is accessible only to authorized users and is often used for internal communication, collaboration, and resource sharing.
- **Firewall**: A security device or software that monitors and controls incoming and outgoing network traffic based on predetermined security rules. It acts as a barrier between a trusted internal network and untrusted external networks, protecting against unauthorized access and threats.

<!-- Some terms -->
## Common Networking Terms

### Node
- A device connected to a network, such as a computer, printer, or router.

### Host
- A computer or device that provides services or resources to other devices on a network.

### Client
- A device or software application that requests services or resources from a server.

### Server
- A device or software application that provides services or resources to clients on a network.

### Router
- A device that forwards data packets between networks, directing traffic based on IP addresses.

### Switch
- A device that connects devices within a single network, allowing them to communicate efficiently by forwarding data to the correct destination.

### Hub
- A basic networking device that connects multiple devices in a network, allowing them to communicate as a single network segment. Unlike switches, hubs do not filter data and send incoming data packets to all connected devices.

### WAN
- **Wide Area Network** — a network that covers a large geographical area, connecting multiple local area networks (LANs) or metropolitan area networks (MANs).

### LAN
- **Local Area Network** — a network that connects devices within a limited geographical area, such as a home, office, or campus.

### MAN
- **Metropolitan Area Network** — a network that connects devices within a city or a large campus, typically larger than a LAN but smaller than a WAN.

### VPN
- **Virtual Private Network** — a secure connection that allows users to access a private network over the internet, encrypting data to protect it from unauthorized access.


<!-- watch yt videos of these topics (Fundamental of networking, Project lifecycle, terraform, jenkins, data docs, jira->(SRE, Agile)) -->
<!-- /Yt video to watch -->
## Additional Resources(watch Their yt video)
- Fundamental of Networking
- Project Lifecycle
- Terraform
- Jenkins
- Data Docs
- Jira (SRE, Agile)

<!-- virtualisation introdction -->
## Virtualization
Virtualization is the process of creating virtual versions of physical resources, such as servers, storage devices, and networks. It allows multiple virtual instances to run on a single physical machine, improving resource utilization and flexibility.
<!-- explain using the flow diagram -->
<!-- what is VM -->
## Overview
Virtualization enables the abstraction of physical hardware, allowing multiple virtual machines (VMs) to run on a single physical host. This technology is widely used in cloud computing, data centers, and enterprise environments to optimize resource usage, enhance scalability, and improve disaster recovery capabilities.
<!-- what is hypervisor -->
<!-- host OS, Guest OS,Virtual mahcine monitor -->



## Key Concepts
- **Hypervisor**: A software layer that enables virtualization by allowing multiple virtual machines (VMs) to run on a single physical host. It manages the allocation of resources to each VM.
    <!-- what hypervisor is AWS uses ? --> 
- **Types of Hypervisors**:
  - **Type 1 Hypervisor**: Runs directly on the host's hardware (e.g., VMware ESXi, Microsoft Hyper-V, Xen,KVM).
  - **Type 2 Hypervisor**: Runs on top of a host operating system (e.g., Oracle VirtualBox, VMware Workstation).
- **Virtual Machine (VM)**: An emulation of a physical computer that runs an operating system and applications as if it were a separate physical machine.
- **Containerization**: A lightweight form of virtualization that packages applications and their dependencies into containers, allowing them to run consistently across different environments (e.g., Docker).
- **Orchestration**: The process of managing and automating the deployment, scaling, and operation of virtualized resources, often using tools like Kubernetes for containers or VMware vSphere for VMs.



