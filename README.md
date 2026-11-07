# NETWORKWALKS-Bright-Arthur-B084-WK1-PM2-WIRESHARK-SOC-LABS
Inspecting and interpreting network traffic with Wireshark to detect suspicious activities, recognize security threats, and support Security Operations Center (SOC) monitoring and incident investigations.

## **1. Project Overview**

This project presents a collection of practical exercises focused on network traffic analysis and Security Operations Center (SOC) investigation using Wireshark.

The activities involved capturing network packets, examining device communication, applying filters to isolate relevant traffic, and investigating various network activities. Through these exercises, I gained practical experience in understanding how network protocols operate, recognizing suspicious communication patterns, and identifying security risks associated with unprotected network traffic.

I carried out the project in the NetworkWalks cybersecurity training environment, using a simulated Windows 11 system with Wireshark installed.


 # 2. Project Objectives

The primary goal of these exercises was to develop practical skills in network monitoring, packet inspection, and security investigation.

The specific objectives were to:

Gain hands-on experience collecting network data and reviewing packet contents.

Explore how computers exchange information through various networking protocols.

Apply Wireshark filtering techniques to make traffic analysis more focused and manageable.

Trace communication between devices by examining IP addresses, ports, and connection details.

Learn how to identify unusual TCP connection patterns associated with port scanning.

Examine FTP login activity and recognize patterns that may suggest repeated password attempts.

Explore web traffic to understand how requests and server responses can reveal security issues.

Demonstrate how sensitive login information can become visible when transmitted without encryption.

Study internet-based voice communication by examining SIP signaling and RTP media packets.

Follow and reconstruct network conversations to better understand the exchanged data.

Develop awareness of how encryption helps maintain the privacy and security of information transmitted across networks.

# 3. Purpose of the Laboratory

The purpose of these exercises was to gain hands-on experience with network traffic monitoring and basic SOC investigation procedures.

Wireshark was used to examine network communication, identify potentially suspicious activities, and understand how information moves between connected systems.

The laboratory activities included:

Capturing and examining network packets.

Investigating suspicious IP addresses and connection attempts.

Identifying possible port scanning activities.

Reconstructing TCP communication using Follow TCP Stream.

Examining HTTP requests, responses, and server information.

Investigating credentials transmitted through unencrypted HTTP.

Analyzing SIP signaling and RTP voice traffic.

Understanding the security implications of unencrypted communication.

Note: All activities were conducted for educational purposes within an authorized laboratory environment. Network captures were handled responsibly, with consideration for the confidentiality of sensitive information.

## 4. Laboratory Environment and Configuration

| **Component** | **Details** |
|---|---|
| Operating System | Windows 11 |
| Packet Analysis Software | Wireshark |
| Cybersecurity Training Platform | NetworkWalks |
| Web Communication Protocols | HTTP, HTTPS |
| Voice Communication Protocols | SIP, RTP |
| Number of Laboratory Exercises | 6 |
| Main Area of Focus | Network Traffic Analysis and Security Monitoring |

# 5. Practical Exercises and Investigation Process

**Exercise 1: Accessing the Wireshark Laboratory**

I began by accessing the Wireshark SOC laboratory through the NetworkWalks training platform.

The environment provided a simulated Windows 11 desktop with Wireshark already installed, allowing me to perform packet capture and traffic analysis without configuring a separate physical laboratory.


<img width="1262" height="747" alt="Image" src="https://github.com/user-attachments/assets/2610af78-e734-48b1-b08f-ceeb44c4d1dc" />


**Exercise 2: Capturing Network Traffic**

After entering the virtual environment using the provided login credentials, I launched Wireshark and selected the active Wi-Fi network interface.

I started the packet capture process and observed the network traffic generated within the environment.

This exercise introduced me to the process of collecting network packets and examining the communication taking place between connected systems.

<img width="1270" height="750" alt="Image" src="https://github.com/user-attachments/assets/bd895afa-312a-4951-852e-49b1266768c5" />

** Exercise 3: Investigating TCP SYN Scanning**

To investigate connection attempts and possible port scanning activity, I applied the following Wireshark display filter:

tcp.flags.syn == 1

This filter helped me isolate TCP packets with the SYN flag set and examine connection initiation attempts.

By reviewing the source and destination addresses, as well as the destination ports, I investigated patterns that could indicate TCP SYN scanning.

Information examined:

Source IP address associated with the connection attempts.

Destination IP address of the target system.

Ports targeted during the connection attempts.

Ports responding to connection requests.

Connection patterns associated with potential scanning activity.

Indicators that could help distinguish suspicious traffic from normal communication.

This exercise helped me understand how network analysts examine connection attempts and identify possible reconnaissance activities.

** Exercise 4: Reconstructing TCP Communication**

I used Wireshark's Conversations feature to identify TCP communication involving port 5000.

The following display filter was applied:

tcp.port == 5000

After identifying the relevant packets, I used Follow → TCP Stream to reconstruct the communication between the client and server.

This made it easier to examine the conversation as a continuous exchange rather than analyzing individual packets separately.

Findings:

Identified the communicating client and server IP addresses.

Examined the TCP conversation and stream number.

Reconstructed the exchanged chat messages.

Observed information transmitted in readable text.

Recognized the risks associated with sending sensitive information without encryption.

This exercise demonstrated how TCP stream analysis can help investigators understand communication during a network investigation.
