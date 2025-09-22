## Day-1-Scan-Your-Local-Network-for-Open-Ports

## Objectives
1. [Install Nmap from official website](#Install-Nmap-from-official-website)
2. [Find your local IP range (e.g., 192.168.1.0/24)](#Find-your-local-IP-range-(e.g.,-192.168.1.0/24))
3. [Run: nmap -sS 192.168.1.0/24 to perform TCP SYN scan](#TCP-SYN-scan)
4. [Note down IP addresses and open ports found](#Note-down-IP-addresses-and-open-ports-found)
5. [Optionally analyze packet capture with Wireshark](#Optionally-analyze-packet-capture-with-Wireshark)
6. [Research common services running on those ports](#Research-common-services-running-on-those-ports)
7. [Identify potential security risks from open ports](#Identify-potential-security-risks-from-open-ports)
8. [Save scan results as a text or HTML file](#Save-scan-results-as-a-text-or-HTML-file)

  
 ## Install Nmap from official website
 - Nmap (Network Mapper) is an open-source network scanning tool used to discover devices, identify open ports, detect services and their versions, and gather information about operating systems on a network. It is widely used for network auditing, security assessments, and troubleshooting. Nmap allows users to do a bunch of things that are related to a wide range of network-related tasks.
 - ➤ https://nmap.org/download.html#windows
 - ![image](https://github.com/NATTOMR/Day-1-Scan-Your-Local-Network-for-Open-Ports/blob/main/image-1.png)

 ## Find your local IP range (e.g., 192.168.1.0/24)
 - ![image](https://github.com/NATTOMR/Day-1-Scan-Your-Local-Network-for-Open-Ports/blob/main/imege-3.png)
 ## Run: nmap -sS 192.168.1.0/24 to perform TCP SYN scan
  - ![image]( https://github.com/NATTOMR/Day-1-Scan-Your-Local-Network-for-Open-Ports/blob/main/image-2.jpg)
 ## Note down IP addresses and open ports found
 ## Optionally analyze packet capture with Wireshark
 - Wireshark is a free and open‑source network protocol analyzer that captures and displays network traffic in real time. It is a powerful tool for network troubleshooting, analysis, software, and communications protocol development. A network packet analyzer like Wireshark presents captured packet data in as much detail as possible, similar to how an electrician uses a voltmeter to inspect an electrical cable, but for network traffic.
 -https://www.wireshark.org/
  - ![image](https://github.com/NATTOMR/Day-1-Scan-Your-Local-Network-for-Open-Ports/blob/main/image-4.png)
 ## Research common services running on those ports
 ### 1. What is TCP?

####TCP (Transmission Control Protocol) is one of the core protocols of the Internet. It is connection-oriented, which means:

- Before data is sent, a connection is established between the client and server (the famous three-way handshake: SYN → SYN-ACK → ACK).

- Data is delivered reliably, in the correct order.

- Errors are detected and corrected if packets are lost.

####TCP is used whenever reliable communication is needed, like:

- Websites (HTTP/HTTPS)

- Email (SMTP, IMAP, POP3)

- File transfers (FTP)

### 2. TCP Ports

A port is like a “door” on a computer where a service listens for incoming traffic.

- Ports are identified by numbers from 0 to 65535.

- Well-known ports: 0–1023 (standard services)

- Registered ports: 1024–49151

- Dynamic/private ports: 49152–65535

### 3. Common TCP ports

- Port 22 → SSH (Secure Shell)

- - Used for remote login and secure command-line access to servers.

- Port 443 → HTTPS (HTTP Secure)

- - Used for encrypted web traffic (websites starting with https://).

So when you use the Wireshark filter:
-  tcp.port == 22 or tcp.port == 443

 ## Identify potential security risks from open ports
 ## Save scan results as a text or HTML file
