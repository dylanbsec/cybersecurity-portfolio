# Networking Learning Log

This file tracks my progress as I build my understanding of computer networking through practical labs, coursework and independent study.

---

## Entry 001 - Network Types

**Platform:** Cisco Networking Academy  
**Module:** 1.1 - Network Types  
**Focus:** Understanding different network types and connected devices

### What I Learned

This lesson introduced the different types of computer networks and how they enable communication between devices around the world.

I learned that the Internet is a global collection of interconnected networks that communicate using common networking standards. Data can travel across telephone lines, fibre-optic cables, wireless networks and satellite connections, allowing users to exchange information almost instantly.

I also learned about different network environments, including:

- **SOHO (Small Office/Home Office)** networks for homes and small businesses.
- **Business networks**, which support communication, resource sharing and internet access across organisations.
- The Internet as a **"network of networks"**, made up of thousands of smaller interconnected networks.

The lesson also explored how internet connectivity extends beyond traditional computers to a wide range of connected devices.

### Connected Devices

Examples covered included:

- Smartphones
- Tablets
- Smartwatches
- Smart glasses
- Smart TVs
- Gaming consoles
- Smart home appliances
- Security systems
- Smart sensors and actuators
- RFID tags
- Medical devices
- Connected vehicles

These devices form part of the growing Internet of Things (IoT), allowing information to be collected, shared and acted upon remotely.

### Key Concepts

- Internet
- Local Area Networks (LAN)
- Small Office/Home Office (SOHO) networks
- Business networks
- Internet of Things (IoT)
- Connected devices
- RFID technology
- Sensors and actuators

### Reflection

Before this lesson I thought of networking mainly in terms of computers communicating with each other. I now have a much broader understanding that modern networks connect a huge variety of devices, from household appliances to industrial sensors and medical equipment.

I also gained a better understanding of why the Internet is often described as a "network of networks", with thousands of independent networks working together using common communication standards.

### Next Steps

- Continue through the Cisco Networking Academy modules.
- Learn about network components and common networking hardware.
- Build a stronger understanding of how devices communicate across different types of networks.

---

## Entry 002 - Data Transmission Fundamentals

**Date:** 16 July 2026

**Focus:** Understanding how data is represented and transmitted across computer networks.

### Topics Covered

- Types of data (volunteered, observable, inferred and secret)
- Binary (bits)
- Bytes
- ASCII encoding
- Electrical signals
- Optical signals
- Wireless signals
- Network transmission media

### Reflection

I learned that computers only process and store information as binary digits (bits), with every piece of data ultimately being represented as a series of 0s and 1s. I also learned that eight bits make up a byte, and that standards such as ASCII allow computers to represent letters, numbers and special characters in binary.

The lesson also introduced how binary data is transmitted across networks. Before data can travel, it is converted into signals which are sent over different types of media. I learned the three primary transmission methods: electrical signals over copper cables, optical signals over fibre-optic cables, and wireless signals using radio, microwave or infrared waves.

Finally, I explored different categories of data, including volunteered, observable, inferred and secret data, and gained a better understanding of how information can be collected and interpreted in different ways.

### Next Steps

- Continue the Cisco Networking Academy course.
- Learn how devices communicate using network protocols.
- Build a stronger understanding of data transmission across different network media.

---

## Entry 003 - Networking Fundamentals (Book Study)

**Date:** 24–25 July 2026

**Focus:** Core networking concepts, network types, identification methods, and firewall fundamentals.

### Topics Covered

- Definition of a computer network
- Endpoint devices
- Network Interface Cards (NICs)
- Network Operating Systems (NOS)
- Network media
- Hostnames, IP addresses and MAC addresses
- Internet vs World Wide Web
- Intranet
- Extranet
- Demilitarized Zones (DMZs)
- Host-based firewalls
- Network-based firewalls
- Access Control Entries (ACEs)
- Access Control Lists (ACLs)
- Windows Firewall rules
- Firewall logging
- Firewall rule testing

### Reflection

I spent time studying networking fundamentals from *Networking Fundamentals* by Gordon Davies. I learned that a network is a collection of endpoint devices communicating over a shared medium, and that networking extends far beyond traditional computers to include Internet of Things (IoT) devices.

I developed a clearer understanding of how devices are identified using hostnames, IP addresses and MAC addresses, as well as the distinction between the Internet, the World Wide Web, intranets and extranets. I also learned about DMZs and how they differ from extranets by exposing selected services to the public while protecting internal networks.

The chapter introduced firewall concepts, including the differences between host-based and network-based firewalls. I learned that firewall rules are built from Access Control Entries (ACEs), which together form Access Control Lists (ACLs), and that rules can be applied to both inbound and outbound traffic. Finally, I learned the importance of verifying firewall configurations through testing and reviewing firewall logs rather than assuming a rule has been applied correctly.

### Next Steps

- Continue reading *Networking Fundamentals*.
- Build a stronger understanding of network devices and topologies.
- Reinforce these concepts through practical labs and packet analysis.

---

## Entry 004 - Bandwidth & Throughput

**Date:** 12 August 2026

**Focus:** Understanding network bandwidth, throughput, latency and the factors that affect real-world data transfer speeds.

### Topics Covered

- Bandwidth
- Throughput
- Bits per second (bps)
- Kilobits per second (Kbps)
- Megabits per second (Mbps)
- Gigabits per second (Gbps)
- Terabits per second (Tbps)
- Network latency
- Network bottlenecks
- Factors affecting data transfer speeds

### Reflection

Today I continued studying networking fundamentals through Cisco Networking Academy, focusing on bandwidth and throughput.

I learned that **bandwidth represents the theoretical capacity of a network medium to carry data**, typically measured in bits per second. Common measurements include Kbps, Mbps and Gbps.

I also learned that **throughput represents the amount of data actually transferred over a connection during a given period**. Although a connection may have a particular bandwidth, its real-world throughput can be lower due to factors such as network traffic, the type of data being transmitted, latency and the devices encountered between the source and destination.

An important concept was that a network path is limited by its slowest segment. Even if most of the connection supports high bandwidth, a lower-bandwidth section can become a bottleneck and reduce overall throughput.

I also developed my understanding of **latency**, which refers to the time and delays involved in data travelling from one point to another.

### Next Steps

- Continue the Cisco Networking Basics course.
- Develop my understanding of network performance and latency.
- Apply these concepts when learning more about network troubleshooting and traffic analysis.

---

## Entry 005 - The OSI Reference Model

**Date:** 27 August 2026

**Focus:** Understanding the seven-layer OSI model and how it can be used to describe and troubleshoot network communication.

### Topics Covered

- OSI (Open Systems Interconnection) model
- The seven OSI layers
- Physical network infrastructure
- MAC addressing
- IP addressing and routing
- TCP and UDP
- Sessions between devices
- Data presentation and encryption
- Application-layer protocols
- Using the OSI model for troubleshooting

### The Seven Layers

Layer 7. **Application** - Network services used by applications and users, including protocols such as HTTP and HTTPS.
Layer 6. **Presentation** - Prepares data for applications, including formatting, encoding and encryption.
Layer 5. **Session** - Establishes, maintains and manages communication sessions between devices.
Layer 4. **Transport** - Handles end-to-end data transport using protocols such as TCP and UDP.
Layer 3. **Network** - Handles logical addressing and routing between networks using IP.
Layer 2. **Data Link** - Handles communication between devices on the local network, including MAC addressing and Ethernet.
Layer 1. **Physical** - Covers physical network components and signalling, including cables, fibre, connectors and network interfaces.
   
### Reflection

Today I studied Professor Messer's Network+ lesson on the **OSI Reference Model**.

I learned that the OSI model divides network communication into seven conceptual layers, with each layer responsible for a different part of the communication process. Although real-world networking does not always divide perfectly into these layers, the model provides a useful framework for understanding how different technologies and protocols interact.

I particularly found the troubleshooting aspect useful. Instead of treating a network problem as one large issue, the OSI model can help isolate where the problem might exist. For example, a Physical layer problem could involve a damaged cable or network adapter, while a Network layer problem could involve IP addressing or routing.

I also reinforced several concepts I have encountered previously, including MAC addresses at Layer 2, IP addressing and routing at Layer 3, TCP and UDP at Layer 4, and protocols such as HTTP and HTTPS at Layer 7.

### Next Steps

- Continue Professor Messer's Network+ material.
- Become more confident identifying which technologies and protocols operate at each OSI layer.
- Apply the OSI model when practising network troubleshooting.
- Compare the OSI model with the TCP/IP model.
