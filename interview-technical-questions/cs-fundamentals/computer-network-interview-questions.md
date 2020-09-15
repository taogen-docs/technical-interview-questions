# Computer Network Interview Questions

### Content

- [Computer Networks and the Internet](#Computer Networks and the Internet)
  - [What is the Internet, Network Edge, Network Core](#What is the Internet, Network Edge, Network Core)
    - [x] [Q: What is a Network?](#Q: What is a Network?)
    - [x] [Q: What is a Node?](#Q: What is a Node?)
    - [x] [Q: What is Network Topology?](#Q: What is Network Topology?)
    - [x] [Q: What is Data Encapsulation?](#Q: What is Data Encapsulation?)
    - [x] [Q: What is the difference between the Internet, Intranet, and Extranet?](#Q: What is the difference between the Internet, Intranet, and Extranet?)
    - [x] [Q: What are the different types of a network? Explain each briefly.](#Q: What are the different types of a network? Explain each briefly.)
    - [x] [Q: Differentiate Communication and Transmission?](#Q: Differentiate Communication and Transmission?)
  - [Delay, Loss and Throughput](#Delay, Loss and Throughput)
  - [Protocol Layers and Service Models](#Protocol Layers and Service Models)
    - [x] [Q: What is the OSI reference model?](#Q: What is the OSI reference model?)
    - [x] [Q: What are the layers in OSI Reference Models? Describe each layer briefly.](#Q: What are the layers in OSI Reference Models? Describe each layer briefly.) 
    - [x] [Q: Explain TCP/IP Model?](#Q: Explain TCP/IP Model?)
  - [History of Computer Networking and the Internet](#History of Computer Networking and the Internet)
- [Application Layer](#Application Layer)
  - [Principles of Network Applications](#Principles of Network Applications)
  - [The Web and HTTP](#The Web and HTTP)
    - [x] [Q: What is HTTP and what port does it use?](#Q: What is HTTP and what port does it use?)
    - [x] [Q: What is HTTPs and what port does it use?](#Q: What is HTTPs and what port does it use?)
    - [x] [Q: What is a Proxy Server and how do they protect the computer network?](#Q: What is a Proxy Server and how do they protect the computer network?)
  - [Electronic Mail](#Electronic Mail)
  - [DNS--the Internet's Directory Service](#DNS--the Internet's Directory Service)
    - [x] [Q: What is DNS?](#Q: What is DNS?)
    - [x] [Q:  What is the difference between a Domain and a Workgroup?](#Q:  What is the difference between a Domain and a Workgroup?) 
  - [Peer-to-Peer Applications](#Peer-to-Peer Applications)
  - [Video Streaming and Content Distribution Networks](#Video Streaming and Content Distribution Networks)
  - [Socket Programming](#Socket Programming)
- [Transport Layer](#Transport Layer)
  - [Basics](#Basics)
    - [x] [Q: What are TCP and UDP?](#Q: What are TCP and UDP? ) 
  - [Transport-Layer Services](#Transport-Layer Services)
  - [Multiplexing and Demultiplexing](#Multiplexing and Demultiplexing)
  - [Connectionless Transport: UDP](#Connectionless Transport: UDP)
  - [Principles of Reliable Data Transfer](#Principles of Reliable Data Transfer)
  - [**Connection-Oriented Transport: TCP**](#Connection-Oriented Transport: TCP)
    - [x] [Q: What is TCP Three-Way Handshake?](#Q: What is TCP Three-Way Handshake?)
    - [x] [Q: What is Process of Close TCP Connection?](#Q: What is Process of Close TCP Connection?)
  - [Principles of Congestion Control](#Principles of Congestion Control)
  - [TCP Congestion Control](#TCP Congestion Control)
- [The Network Layer: Data Plane](#The Network Layer: Data Plane)
  - [Inside a Router](#Inside a Router)
    - [x] [Q: What are Routers?](#Q: What are Routers?)
    - [x] [Q: What is the difference between Hub, Switch, and Router?](#Q: What is the difference between Hub, Switch, and Router?)
  - [The Internet Protocol (IP)](#The Internet Protocol (IP)) (IPv4, addressing, IPv6, DCHP)
    - [x] [Q: What are IP classes and how can you identify the IP class of given an IP address?](#Q: What are IP classes and how can you identify the IP class of given an IP address?)
    - [x] [Q: What is meant by 127.0.0.1 and localhost?](#Q: What is meant by 127.0.0.1 and localhost? ) 
    - [x] [Q: What are Ipconfig and Ifconfig?](#Q: What are Ipconfig and Ifconfig?)
    - [x] [Q: Explain DHCP briefly?](#Q: Explain DHCP briefly?)
  - [Generalized Forwarding and SDN](#Generalized Forwarding and SDN)
- [The Network Layer: Control Plane](#The Network Layer: Control Plane)
  - [Routing Algorithms](#Routing Algorithms)
  - [Intra-AS Routing in the Internet: OSPF](#Intra-AS Routing in the Internet: OSPF)
  - [Routing Among the ISPs: BGP](#Routing Among the ISPs: BGP)
  - [The SDN Control Plane](#The SDN Control Plane)
  - [ICMP: The Internet Control Message Protocol](#ICMP: The Internet Control Message Protocol)
  - [Network Management and SNMP](#Network Management and SNMP)
    - [x] [Q: What is SNMP?](#Q: What is SNMP? ) 
- [Data Link Layer and LANs](#Data Link Layer and LANs)
  - [Introduction to Link Layer](#Introduction to Link Layer)
    - [x] [Q: What is NIC?](#Q: What is NIC?)
  - [Error-Detection and Correction Techniques](#Error-Detection and Correction Techniques)
  - [Multiple Access Links and Protocols](#Multiple Access Links and Protocols)
  - [Switched Local Area Networks](#Switched Local Area Networks)
  - [Link Virtualization: A Network as a Link Layer](#Link Virtualization: A Network as a Link Layer)
  - Data Center Networking
- [Wireless and Mobile Networks](#Wireless and Mobile Networks)
- [Physical Layer](#Physical Layer)
  - [Basic Data Communication](#Basic Data Communication)
  - [Transmission Media](#Transmission Media)
- [Network Security](#Network Security)
  - [Introduction](#Introduction)
  - [Principles of Cryptography](#Principles of Cryptography)
  - [Message Integrity and Digital Signatures](#Message Integrity and Digital Signatures)
  - [End-Point Authentication](#End-Point Authentication)
  - [Securing E-Mail](#Securing E-Mail)
  - [Securing TCP Connections: SSL](#Securing TCP Connections: SSL)
  - [Network-Layer Security: IPsec and Virtual Private Networks (VPN)](#Network-Layer Security: IPsec and Virtual Private Networks (VPN))
    - [x] [Q: What is a VPN?](#Q: What is a VPN? ) 	
  - Securing Wireless LANs
  - [Operational Security: Firewalls and Intrusion Detection Systems](#Operational Security: Firewalls and Intrusion Detection Systems)
    - [x] [Q: What is a Firewall?](#Q: What is a Firewall?) 
- [x] [Multimedia Networking](#Multimedia Networking)
- [Others](#Others)
  - [x] [Q: Full process a HTTP Request?](#Q: Full process a HTTP Request?)
- [x] [References](#References)

## Main



## Computer Networks and the Internet

### What is the Internet, Network Edge, Network Core

### Q: What is a Network?

Network is defined as a set of devices connected to each other using a physical transmission medium.

**For Example,** A computer network is a group of computers connected with each other to communicate and share information and resources like hardware, data, and software. In a network, nodes are used to connect two or more networks.

### Q: What is a Node?

Two or more computers are connected directly by an optical fiber or any other cable. A node is a point where a connection is established. It is a network component that is used to send, receive and forward the electronic information.

A device connected to a network is also termed as Node. Let's consider that in a network there are 2 computers, 2 printers, and a server are connected, then we can say that there are five nodes on the network.

### Q: What is Network Topology?

Network topology is a physical layout of the computer network and it defines how the computers, devices, cables, etc are connected to each other.

### Q: What is Data Encapsulation?

In a computer network, to enable data transmission from one computer to another, the network devices send messages in the form of packets. These packets are then added with the IP header by the OSI reference model layer.

The Data Link Layer encapsulates each packet in a frame that contains the hardware address of the source and the destination computer. If a destination computer is on the remote network then the frames are routed through a gateway or router to the destination computer.

### Q: What is the difference between the Internet, Intranet, and Extranet?

The terminologies Internet, Intranet, and Extranet are used to define how the applications in the network can be accessed. They use similar TCP/IP technology but differ in terms of access levels for each user inside the network and outside the network.

- **Internet**: Applications are accessed by anyone from any location using the web.
- **Intranet**: It allows limited access to users in the same organization.
- **Extranet**: External users are allowed or provided with access to use the network application of the organization.

### Q: What are the different types of a network? Explain each briefly.

There are 4 major types of networks.

**Let's take a look at each of them in detail.**

1. **Personal Area Network (PAN)**: It is the smallest and basic network type that is often used at home. It is a connection between the computer and another device such as phone, printer, modem tablets, etc
2. **Local Area Network (LAN)**: LAN is used in small offices and Internet cafes to connect a small group of computers to each other. Usually, they are used to transfer a file or for playing the game in a network.
3. **Metropolitan Area Network (MAN):** It is a powerful network type than LAN. The area covered by MAN is a small town, city, etc. A huge server is used to cover such a large span of area for connection.
4. **Wide Area Network (WAN)**: It is more complex than LAN and covers a large span of the area typically a large physical distance. The Internet is the largest WAN which is spread across the world. WAN is not owned by any single organization but it has distributed ownership.

**There are some other types of the network as well:**

- Storage Area Network (SAN)
- System Area Network (SAN)
- Enterprise Private Network (EPN)
- Passive Optical Local Area Network (POLAN)

### Q: Differentiate Communication and Transmission?

Through Transmission the data gets transferred from source to destination (only one way). It is treated as the physical movement of data.

Communication means the process of sending and receiving data between two media (data is transferred between source and destination in both ways).

### Delay, Loss and Throughput

### Protocol Layers and Service Models

### Q: What is the OSI reference model?

**O**pen **S**ystem **I**nterconnection, the name itself suggests that it is a reference model that defines how applications can communicate with each other over a networking system.

It also helps to understand the relationship between networks and defines the process of communication in a network.

### Q: What are the layers in OSI Reference Models? Describe each layer briefly. 

**Given below are the seven layers of OSI Reference Models:**

**a) Physical Layer** **(Layer 1):** It converts data bits into electrical impulses or radio signals. **Example:** Ethernet.

**b) Data Link Layer (Layer 2):** At the Data Link layer, data packets are encoded and decoded into bits and it provides a node to node data transfer. This layer also detects the errors that occurred at Layer 1.

**c) Network Layer** **(Layer 3):** This layer transfers variable length data sequence from one node to another node in the same network. This variable-length data sequence is also known as **“Datagrams”**.

**d) Transport Layer (Layer 4):** It transfers data between nodes and also provides acknowledgment of successful data transmission. It keeps track of transmission and sends the segments again if the transmission fails.

**e) Session Layer (Layer 5):** This layer manages and controls the connections between computers. It establishes, coordinates, exchange and terminates the connections between local and remote applications.

**f) Presentation Layer (Layer 6):** It is also called as “Syntax Layer”. Layer 6 transforms the data into the form in which the application layer accepts.

**g) Application Layer** **(Layer 7):** This is the last layer of the OSI Reference Model and is the one that is close to the end-user. Both end-user and application layer interacts with the software application. This layer provides services for email, file transfer, etc.

![](images/cs-computer-network-OSI-reference-model.jpg)

### Q: Explain TCP/IP Model?

The most widely used and available protocol is TCP/IP i.e. Transmission Control Protocol and Internet Protocol. TCP/IP specifies how data should be packaged, transmitted and routed in their end to end data communication.

**There are four layers as shown in the below diagram:**

![](images/cs-computer-network-tcpip-model.png)

**Given below is a brief explanation of each layer:**

- **Application Layer**: This is the top layer in the TCP/IP model. It includes processes that use the Transport Layer Protocol to transmit the data to their destination. There are different Application Layer Protocols such as HTTP, FTP, SMTP, SNMP protocols, etc.
- **Transport Layer**: It receives the data from the Application Layer which is above the Transport Layer. It acts as a backbone between the host's system connected with each other and it mainly concerns about the transmission of data. TCP and UDP are mainly used as Transport Layer protocols.
- **Network or Internet Layer**: This layer sends the packets across the network. Packets mainly contain source & destination IP addresses and actual data to be transmitted.
- **Network Interface Layer**: It is the lowest layer of the TCP/IP model. It transfers the packets between different hosts. It includes encapsulation of IP packets into frames, mapping IP addresses to physical hardware devices, etc.

### History of Computer Networking and the Internet



## Application Layer

### Principles of Network Applications

### The Web and HTTP

### Q: What is HTTP and what port does it use?

HTTP is HyperText Transfer Protocol and it is responsible for web content. Many web pages are using HTTP to transmit the web content and allow the display and navigation of HyperText. It is the primary protocol and port used here is TCP port 80.

### Q: What is HTTPs and what port does it use?

HTTPs is a Secure HTTP. HTTPs is used for secure communication over a computer network. HTTPs provides authentication of websites that prevents unwanted attacks.

In bi-directional communication, the HTTPs protocol encrypts the communication so that the tampering of the data gets avoided. With the help of an SSL certificate, it verifies if the requested server connection is a valid connection or not. HTTPs use TCP with port 443.

### Q: What is a Proxy Server and how do they protect the computer network?

For data transmission, IP addresses are required and even DNS uses IP addresses to route to the correct website. It means without the knowledge of correct and actual IP addresses it is not possible to identify the physical location of the network.

Proxy servers prevent external users who are unauthorized to access such IP addresses of the internal network. It makes the computer network virtually invisible to external users.

Proxy Server also maintains the list of blacklisted websites so that the internal user is automatically prevented from getting easily infected by viruses, worms, etc.

### Electronic Mail

### DNS--the Internet's Directory Service

### Q: What is DNS?

Domain Name Server (DNS), in a non-professional language and we can call it an Internet’s phone book. All the public IP addresses and their hostnames are stored in the DNS and later it translates into a corresponding IP address.

For a human being, it is easy to remember and recognize the domain name, however, the computer is a machine that does not understand the human language and they only understand the language of IP addresses for data transfer.

There is a “Central Registry” where all the domain names are stored and it gets updated on a periodic basis. All Internet service providers and different host companies usually interact with this central registry to get the updated DNS details.

**For Example**, When you type a website [www.softwaretestinghelp.com](https://www.softwaretestinghelp.com/), then your Internet service provider looks for the DNS associated with this domain name and translates this website command into a machine language – IP address – 151.144.210.59 (note that, this is the imaginary IP address and not the actual IP for the given website) so that you will get redirected to the appropriate destination.

### Q:  What is the difference between a Domain and a Workgroup? 

In a computer network, different computers are organized in different methods and these methods are – Domains and Workgroups. Usually, computers which run on the home network belong to a Workgroup.

However, computers that are running on an office network or any workplace network belong to the Domain.

**Their differences are as follows:**

| Workgroup                                                    | Domain                                                       |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| All computers are peers and no computer has control over another computer | Network admin uses one or more computer as a server and provide all accesses, security permission to all other computers in a network |
| In a Workgroup, each computer maintains their own database   | The domain is a form of a computer network in which computers, printers, and user accounts are registered in a central database. |
| Each computer has their own authentication rule for every user account | It has centralized authentication servers which set the rule of authentication |
| Each computer has set of user account. If user has account on that computer then only user able to access the computer | If user has an account in a domain then user can login to any computer in a domain |
| Workgroup does not bind to any security permission or does not require any password | Domain user has to provide security credentials whenever they are accessing the domain network |
| Computer settings need to change manually for each computer in a Workgroup | In a domain, changes made in one computer automatically made same changes to all other computers in a network |
| All computers must be on same local area network             | In a domain, computers can be on a different local network   |
| In a Workgroup, there can be only 20 computers connected     | In a domain, thousands of computers can be connected         |

### Peer-to-Peer Applications

### Video Streaming and Content Distribution Networks

### Socket Programming



## Transport Layer

### Basics

### Q: What are TCP and UDP? 

**Common factors in TCP and UDP are:**

- TCP and UDP are the most widely used protocols that are built on the top of the IP protocol.
- Both protocols TCP and UDP are used to send bits of data over the Internet, which is also known as ‘packets’.
- When packets are transferred using either TCP or UDP, it is sent to an IP address. These packets are traversed through routers to the destination.

**The difference between TCP and UDP are enlisted in the below table:**

| TCP                                                          | UDP                                                          |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| TCP stands for Transmission Control Protocol                 | UDP is stands for User Datagram Protocol or Universal Datagram Protocol |
| Once the connection is setup, data can be sent bi-directional i.e. TCP is a connection oriented protocol | UDP is connectionless, simple protocol. Using UDP, messages are sent as packets |
| The speed of TCP is slower than UDP                          | UDP is faster compared to TCP                                |
| TCP is used for the application where time is not critical part of data transmission | UDP is suitable for the applications which require fast transmission of data and time is crucial in this case. |
| TCP transmission occurs in a sequential manner               | UDP transmission also occurs in a sequential manner but it does not maintain the same sequence when it reaches the destination |
| It is heavy weight connection                                | It is lightweight transport layer                            |
| TCP tracks the data sent to ensure no data loss during data transmission | UDP does not ensure whether receiver receives packets are not. If packets are misses then they are just lost |

### Transport-Layer Services

### Multiplexing and Demultiplexing

### Connectionless Transport: UDP

### Connection-Oriented Transport: TCP

### Q: What is TCP Three-Way Handshake?

![](images/cs-computer-network-tcp-three-way-handshake.png)

- 客户端发送一个特殊的 TCP 报文段（SYN segment），请求建立连接。这个特殊的报文段没有应用层数据。报文段头部设置为：SYN bit 设为1；随机设置一个initial sequence number（client_isn）。
- 服务端收到 TCP SYN 报文段。响应给客户端一个 TCP 报文段，这个响应的报文段也没有应用层数据，报文段头部设置为：SYN bit 设为1；acknowledgement number 设为 client_isn + 1；设置一个initial sequence number（server_isn）。
- 客户端收到 SYNACK 报文段。分配连接的缓存和变量。然后发送一个 TCP 报文段给服务端，表示收到服务端的响应。这个报文段同样没有应用层数据，报文段头部设置为：SYN bit 设置为0；acknowledgement number 设置为 server_isn + 1；设置 sequence number 为 client_isn + 1。

> 为什么建立 TCP 连接需要三次握手？
>
> 三次握手为了确定双方都准备好了，确保可以正常通信了。
>
> SYN: synchronize
>
> ACK: acknowledges 

### Q: What is Process of Close TCP Connection?

关闭 TCP 连接的过程：四次挥手

![](images/cs-computer-network-close-tcp-connection.png)

- 客户端请求关闭 TCP 连接。发送一个特殊的报文段，报文段头部设置为： FIN bit 设为1。
- 服务端响应客户端请求。
- 服务端确认可以关闭TCP请求后，发送关闭 TCP 请求。发送一个特殊的报文段，报文头部设置为：FIN bit 设为1.
- 客户端响应服务端请求。

通过四次通信后，客户端和服务端可以关闭 TCP 连接，释放 TCP 连接资源，如缓存和变量。

> FIN: finish.

### Principles of Reliable Data Transfer

### Principles of Congestion Control

### TCP Congestion Control



## The Network Layer: Data Plane

### Inside a Router

### Q: What are Routers?

The router is a network device that connects two or more network segments. It is used to transfer information from the source to the destination.

Routers send the information in terms of data packets and when these data packets are forwarded from one router to another router then the router reads the network address in the packets and identifies the destination network.

### Q: What is the difference between Hub, Switch, and Router?

| Hub                                                          | Switch                                                       | Router                                                       |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| Hub is least expensive, least intelligent and least complicated of the three. It broadcast all data to every port which may cause serious security and reliability concern | Switches work similarly like Hubs but in a more efficient manner. It creates connections dynamically and provides information only to the requesting port | The router is smartest and most complicated out of these three. It comes in all shapes and sizes. Routers are similar like little computers dedicated for routing network traffic |
| In a Network, Hub is a common connection point for devices connected to the network. Hub contains multiple ports and is used to connect segments of LAN | Switch is a device in a network which forwards packets in a network | Routers are located at gateway and forwards data packets     |

### The Internet Protocol (IP)

### Q: What are IP classes and how can you identify the IP class of given an IP address?

An IP address has 4 sets (octets) of numbers each with a value up to 255.

**For Example**, the range of the home or commercial connection started primarily between 190 x or 10 x. IP classes are differentiated based on the number of hosts it supports on a single network. If IP classes support more networks then very few IP addresses are available for each network.

There are three types of IP classes and are based on the first octet of IP addresses which are classified as Class A, B or C. If the first octet begins with 0 bit then it is of type Class A.

Class A type has a range up to 127.x.x.x (except 127.0.0.1). If it starts with bits 10 then it belongs to Class B. Class B having a range from 128.x to 191.x.  IP class belongs to Class C if the octet starts with bits 110. Class C has a range from 192.x to 223.x.

### Q: What is meant by 127.0.0.1 and localhost? 

IP address 127.0.0.1, is reserved for loopback or localhost connections. These networks are usually reserved for the biggest customers or some of the original members of the Internet. To identify any connection issue, the initial step is to ping the server and check if it is responding.

If there is no response from the server then there are various causes like the network is down or the cable needs to be replaced or the network card is not in good condition. 127.0.0.1 is a loopback connection on the Network Interface Card (NIC) and if you are able to ping this server successfully, then it means that the hardware is in a good shape and condition.

127.0.0.1 and localhost are the same things in most of the computer network functioning.

### Q: What are Ipconfig and Ifconfig?

**Ipconfig** stands for Internet Protocol Configuration and this command is used on Microsoft Windows to view and configure the network interface.

The command Ipconfig is useful for displaying all TCP/IP network summary information currently available on a network.  It also helps to modify the DHCP protocol and DNS setting.

**Ifconfig** (Interface Configuration) is a command that is used on Linux, Mac, and UNIX operating systems. It is used to configure, control the TCP/IP network interface parameters from CLI i.e. Command Line Interface. It allows you to see the IP addresses of these network interfaces.

### Q: Explain DHCP briefly?

DHCP stands for Dynamic Host Configuration Protocol and it automatically assigns IP addresses to the network devices. It completely removes the process of manual allocation of IP addresses and reduces the errors caused due to this.

This entire process is centralized so that the TCP/IP configuration can also be completed from a central location. DHCP has a “pool of IP addresses” from which it allocates the IP address to the network devices. DHCP cannot recognize if any device is configured manually and assigned with the same IP address from the DHCP pool.

In this situation, it throws the “IP address conflict” error.

DHCP environment requires DHCP servers to set-up the TCP/IP configuration. These servers then assign, release and renew the IP addresses as there might be a chance that network devices can leave the network and some of them can join back to the network.

### Generalized Forwarding and SDN

## The Network Layer: Control Plane

### Routing Algorithms

### Intra-AS Routing in the Internet: OSPF

### Routing Among the ISPs: BGP

### The SDN Control Plane

### ICMP: The Internet Control Message Protocol

### Network Management and SNMP

### Q: What is SNMP? 

SNMP stands for Simple Network Management Protocol. It is a network protocol used for collecting organizing and exchanging information between network devices. SNMP is widely used in network management for configuring network devices like switches, hubs, routers, printers, servers.

**SNMP consists of the below components:**

- SNMP Manager
- Managed device
- SNMP Agent
- Management Information Base (MIB)

**The below diagram shows how these components are connected with each other in the SNMP architecture:**

![](images/cs-computer-network-SNMP.jpg)

SNMP is a part of the TCP/IP suite. There are 3 main versions of SNMP which include SNMPv1, SNMPv2, and SNMPv3.

## Data Link Layer and LANs

### Introduction to Link Layer

### Q: What is NIC?

NIC stands for Network Interface Card. It is also known as Network Adapter or Ethernet Card. It is in the form of an add-in card and is installed on a computer so that the computer can be connected to a network.

Each NIC has a MAC address which helps in identifying the computer on a network.

### Error-Detection and Correction Techniques

### Multiple Access Links and Protocols

### Switched Local Area Networks

### Link Virtualization: A Network as a Link Layer

### Data Center Networking

## Wireless and Mobile Networks

## Physical Layer

### Basic Data Communication

### Transmission Media

### Wireless Transmission

## Network Security

### Introduction

### Principles of Cryptography

### Message Integrity and Digital Signatures

### End-Point Authentication

### Securing E-Mail

### Securing TCP Connections: SSL

### Network-Layer Security: IPsec and Virtual Private Networks (VPN)

### Q: What is a VPN? 

VPN is the Virtual Private Network and is built on the Internet as a private wide area network. Internet-based VPNs are less expensive and can be connected from anywhere in the world.

VPNs are used to connect offices remotely and are less expensive when compared to WAN connections. VPNs are used for secure transactions and confidential data can be transferred between multiple offices. VPN keeps company information secure against any potential intrusion.

**Given below are the 3 types of VPN's:**

1. **Access VPN**: Access VPN's provide connectivity to mobile users and telecommuters. It is an alternative option for dial-up connections or ISDN connections. It provides low-cost solutions and a wide range of connectivity.
2. **Intranet VPN**: They are useful for connecting remote offices using shared infrastructure with the same policy as a private network.
3. **Extranet VPN**: Using shared infrastructure over an intranet, suppliers, customers, and partners are connected using dedicated connections.

### Securing Wireless LANs

### Operational Security: Firewalls and Intrusion Detection Systems

### Q: What is a Firewall?

Firewall is a network security system that is used to protect computer networks from unauthorized access. It prevents malicious access from outside to the computer network. A firewall can also be built to grant limited access to outside users.

The firewall consists of a hardware device, software program or a combined configuration of both. All the messages that route through the firewall are examined by specific security criteria and the messages which meet the criteria are successfully traversed through the network or else those messages are blocked.

Firewalls can be installed just like any other computer software and later can be customized as per the need and have some control over the access and security features. 

Windows Firewall” is an inbuilt Microsoft Windows application that comes along with the operating system. This “Windows Firewall” also helps to prevent viruses, worms, etc.

## Multimedia Networking

## Others

### Q: Full process a HTTP Request?

要实现一个 HTTP 请求，大致可以分为三个阶段。首先客户端要连接网络，获取自己的 IP 地址；然后客户端通过 DNS 域名解析得到目标域名的 IP 地址；最后客户端和服务端建立一个 TCP 连接进行网络通信。

一、客户端连接网络，获取一个 IP 地址

要访问 HTTP 服务器，首先客户端需要连接网络。获取到一个 IP 地址的过程如下：

- 广播一个 DHCP 请求报文，报文封装成 UDP 报文段，设置源端口和目标端口。进而封装成 IP 数据报，目标 IP 地址为 255.255.255.255，源地址 IP 地址为 0.0.0.0。
- IP 数据报封装成 以太网帧，目标 MAC 地址为 FF:FF:FF:FF:FF:FF。
- DHCP 服务器在路由器中。路由器接收到 DHCP 请求。路由器可以分配的地址的 CIDR block 68.85.2.0/24。DHCP 服务器分配地址 68.85.2.101 给客户端。DHCP 服务器创建一个 DHCP ACK 报文，包含分配的 IP 地址，DNS 服务器 IP 地址 68.87.71.226，默认网关路由器IP地址 68.85.2.1，子网掩码 68.85.2.0/24。DHCP ACK 报文封装为 UDP 报文，进而封装为 IP 数据报，最后封装为 以太网帧，源 MAC 地址为路由器的 MAC 地址，目标 MAC 地址为客户端 MAC 地址。
- 客户端收到 DHCP ACK 报文，获取到自己的IP地址和其它地址。

二、域名解析

浏览器输入要访问的 URL。浏览器创建一个 TCP Socket 来发送 HTTP 请求。为了创建 Socket 需要知道目标域名的 IP 地址。因此需要进行 DNS 解析。

- 创建一个 DNS query 报文。封装为 UDP 报文段。设置目标端口。封装为 IP 数据报目标地址为域名服务器的 IP 地址（通过之前 DHCP 获取的）。
- 客户端以太网帧需要知道目标地址的 MAC 地址。通过 ARP 协议获取到网关路由器的 MAC 地址。
- 客户端创建 ARP query 报文。目标IP 地址为默认网关 IP 地址。ARP 报文封装为以太网帧，通过广播报文到达路由器。
- 路由器接收到 ARP query 报文，响应请求，发送 ARP replay 报文。包含路由器的 MAC 地址。
- 客户端收到 路由器的 MAC 地址，将 DNS query 报文发送给路由器。DNS query 报文封装为 IP 报文，目标 IP 地址是 DNS 服务器，最后封装为链路层报文目标地址是路由器的 MAC 地址。
- 路由器收到 DNS query 报文，根据转发表将报文转发到下一跳路由器。
- 经过 ISP 内路由协议和 ISP 之间的路由协议，最终 IP 报文到达 DNS 服务器。DNS 服务器查询缓存得到目标域名的 IP 地址，响应请求，发送 DNS reply 报文。
- 客户端通过 DNS reply 报文得到目标域名的 IP 地址。

三、通过 HTTP 和 TCP 请求服务器

客户端创建 TCP Socket，发送 HTTP GET 报文给服务器。首先需要 TCP 三次握手。

- 客户但创建一个 TCP SYN 报文段，目标端口为 80。TCP 报文封装为 IP 报文，目标地址为服务器 IP 地址。最后封装为链路层报文，目标 MAC 地址为网关路由器 MAC 地址。
- 路由器转发包含 TCP SYN 的 IP 报文给服务器。经过 ISP 内路由协议和 ISP 之间的路由协议，最终 IP 报文到达服务器。
- 服务器响应一个 TCP SYNACK 报文。
- 客户端收到 TCP SYNACK 报文，发送应答报文。TCP 连接成功建立。
- 客户端浏览器创建 HTTP GET 报文，将 HTTP 报文写入 Socket 中，HTTP GET 报文作为 TCP 报文段的负载，进而封装为 IP 报文，经过路由转发请求报文发送到服务器。
- 服务器通过 Socket 收到 HTTP GET 请求报文，然后创建一个 HTTP response 报文，把网页内容放到 HTTP 响应报文的 body 中。把报文发送给 Socket。通过报文封装和路由转发，响应报文发送到客户端。
- 客户端通过 Socket 收到收到 HTTP 响应报文，提取 HTTP 响应报文 body，显示网页。

## References

- [Top 60 Networking Interview Questions And Answers](https://www.softwaretestinghelp.com/networking-interview-questions-2/)