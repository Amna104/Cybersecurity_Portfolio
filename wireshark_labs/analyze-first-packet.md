# Wireshark Lab: Analyze Your First Packet  
**Date:** Dec 1, 2025  

---

## **Objective**
Learn to open, inspect, and filter network packets using Wireshark to analyze traffic to and from a system.

---

## **Tools Used**
- Wireshark (GUI)
- Sample .pcap file

---

## **Tasks and Findings**

### **Task 1: Explore Data**
- Opened `sample.pcap` file in Wireshark  
- First packet with info "Echo (ping) request" used protocol: **ICMP**

---

### **Task 2: Apply IP Filter and Inspect TCP Packet**
- Applied filter: `ip.addr == 142.250.1.139`  
- TCP packet details:
  - Destination port: **80**
  - TCP Flags inspected

---

### **Task 3: Filter by IP or MAC**
- Filter by source IP: `ip.src == 142.250.1.139`  
- Filter by destination IP: `ip.dst == 142.250.1.139`  
- Filter by MAC: `eth.addr == 42:01:ac:15:e0:02`  
- Protocol in IPv4 subtree for this MAC: **TCP**

---

### **Task 4: DNS Analysis**
- Filter: `udp.port == 53`  
- First DNS query: `opensource.google.com`  
- Answers section IP: **142.250.1.139**

---

### **Task 5: TCP Packet Analysis**
- Filter: `tcp.port == 80`  
- First packet details:
  - Time to Live: **64**
  - Frame Length: **54 bytes**
  - Header Length: **20 bytes**
  - Destination IP: **169.254.169.254**
- Filter for TCP containing text `"curl"` for web request analysis

---

## **Key Takeaways**
- Learned to open `.pcap` files and navigate Wireshark UI  
- Applied filters to isolate traffic by IP, MAC, protocol, and payload content  
- Practiced examining DNS, TCP, and ICMP traffic  
- Gained hands-on experience with network packet inspection for security analysis
