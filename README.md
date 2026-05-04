# Python Network Packet Sniffer (Raw Sockets)

**Project Description**
This is a high-performance network analysis tool built in **Python** and executed on Kali Linux. It utilizes raw sockets to intercept and decode live network traffic, providing a detailed view of data as it travels across the OSI model layers.

### **Key Technical Features**
* **Raw Socket Interception:** Uses `socket.AF_PACKET` and `socket.SOCK_RAW` to bypass the standard OS network stack.
* **Manual Header Parsing:** Leverages the `struct` library to unpack binary data into human-readable network headers.
* **Multi-Protocol Support:** Decodes and analyzes several key protocols:
    * **Layer 2:** Ethernet Frames (MAC Address extraction)
    * **Layer 3:** IPv4 (IP Address and TTL analysis)
    * **Layer 4:** TCP, UDP, and ICMP (Port and Flag analysis).

### **Technical Analysis of Captured Data**
Based on the execution results, the tool successfully provides:
* **Real-time Tracking:** Monitors traffic between local hosts (e.g., 10.0.2.15) and external servers.
* **Port Identification:** Detects specific application traffic, such as **HTTPS via Port 443**.
* **Encrypted Payload Detection:** Captures and displays raw hex data, identifying encrypted TLS/SSL handshakes through hex signatures.

### **How to Use**
1. Open your **Kali Linux** terminal.
2. Navigate to the script directory.
3. Execute with administrative privileges:
   ```bash
   sudo python3 sniffer.py
