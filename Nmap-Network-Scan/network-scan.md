# Nmap Network Scan

## Objective

The objective of this project is to demonstrate how network scanning can be used to identify active devices and open ports within a network.

Network scanning helps security professionals understand the attack surface of a system and detect potential security risks.

---

## Tool Used

Nmap (Network Mapper)

Nmap is an open-source network scanning tool used for:

* Network discovery
* Port scanning
* Identifying services running on systems
* Security auditing

---

## Basic Network Scan

Example command used to scan a network:

```
nmap 192.168.1.0/24
```

This command scans all devices on the local network.

---

## Port Scan

Example command:

```
nmap -p 1-1000 192.168.1.1
```

This scans the first 1000 ports of a target system.

---

## Service Detection

Example command:

```
nmap -sV 192.168.1.1
```

This identifies services running on open ports.

---

## Example Output

Typical output may show:

* Open ports
* Running services
* Device status

Example:

```
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
443/tcp  open  https
```

---

## Security Importance

Network scanning helps identify:

* Exposed services
* Misconfigured systems
* Potential attack vectors

Security professionals use scanning to strengthen system defenses.

---

## Conclusion

Nmap is a powerful tool used in cybersecurity for network discovery and security auditing. Regular network scans help identify vulnerabilities and improve security posture.
