# Wireshark Packet Analysis

## Objective

The objective of this project is to analyze network traffic using Wireshark and identify different types of network activity.

Packet analysis helps cybersecurity professionals detect suspicious traffic, investigate incidents, and understand how data flows across a network.

---

## Tool Used

Wireshark

Wireshark is a network protocol analyzer used for:

* Capturing network traffic
* Inspecting packets
* Troubleshooting network issues
* Investigating security incidents

---

## Packet Capture Process

Steps used to capture packets:

1. Open Wireshark.
2. Select the active network interface.
3. Start capturing packets.
4. Generate network traffic by browsing websites or using network services.
5. Stop the capture to begin analysis.

---

## Protocol Analysis

During packet capture, several common protocols can be observed:

### HTTP

HTTP packets show communication between a web browser and a web server.

Example information captured:

* Request method
* Host server
* Response codes

---

### DNS

DNS packets show domain name resolution.

Example:

A DNS request translating a domain name into an IP address.

---

### TCP

TCP packets show reliable communication between systems.

Key elements include:

* Source port
* Destination port
* Sequence numbers

---

## Filtering Traffic

Wireshark provides filters to analyze specific types of traffic.

Example filters:

```
http
dns
tcp.port == 80
```

These filters help analysts focus on relevant traffic.

---

## Security Importance

Packet analysis is important for cybersecurity because it helps analysts:

* Detect malicious traffic
* Identify suspicious connections
* Investigate data exfiltration
* Understand network behavior

---

## Conclusion

Wireshark is an essential tool for network analysis and cybersecurity investigations. By capturing and analyzing packets, security analysts can detect threats and b
