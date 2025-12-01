# Capture Your First Packet with tcpdump  
**Lab Activity – Google Cybersecurity Certificate**  
**Date:** Dec 2025  

---

## **Objective**
Gain hands-on experience capturing, filtering, and analyzing network traffic using `tcpdump` on a Linux system.

---

## **Tools Used**
- Linux Terminal  
- `ifconfig`  
- `tcpdump`  
- `curl`  
- `.pcap` files

---

## **Tasks Completed**

---

## **Task 1: Identify Network Interfaces**
Commands used:
```bash
sudo ifconfig
sudo tcpdump -D
```
## Key findings:
- Identified Ethernet interface: eth0
- Verified available interfaces using tcpdump -D

---

## **Task 2: Inspect Live Network Traffic with tcpdump**

``` bash
sudo tcpdump -i eth0 -v -c5
```

## Skills gained:
- Captured 5 live packets
- Understood packet timestamp, TTL, protocol, flags, checksums, sequence numbers
- Interpreted TCP flags (e.g., PUSH, ACK)

---

## **Task 3: Capture Network Traffic into a pcap File**

Command used to capture only HTTP traffic:
```bash
sudo tcpdump -i eth0 -nn -c9 port 80 -w capture.pcap &
```

Generated traffic:
```bash
curl opensource.google.com
```

Verified capture:
```bash
ls -l capture.pcap
```

## Outcome:
- Successfully captured a 9-packet HTTP session
- Saved to capture.pcap for later analysis

---

## **Task 4: Filter and Analyze Saved Packet Data**

Read pcap with verbose header data:
```bash
sudo tcpdump -nn -r capture.pcap -v
```

View hex + ASCII payload:
```bash
sudo tcpdump -nn -r capture.pcap -X
```

## Learned:
- How to analyze hex and ASCII output
- How to identify anomalies
- How TCP handshake packets look in raw form

---

## **Key Takeaways**
- Identified network interfaces used for packet capturing
- Captured both live and filtered network traffic
- Created and analyzed .pcap files
- Used tcpdump filtering (port filters, hex view, verbose flags)
- Improved packet inspection and command-line analysis skills