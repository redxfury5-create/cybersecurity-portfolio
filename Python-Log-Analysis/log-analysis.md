# Python Log Analysis

## Objective

The objective of this project is to demonstrate how Python can be used to analyze authentication logs and detect suspicious activity such as repeated failed login attempts.

Automating log analysis helps security teams quickly identify potential attacks and unusual behavior.

---

## Tools Used

* Python
* Authentication log files
* Basic scripting for log parsing

---

## Example Log File

Example authentication log entries:

```
2026-03-13 10:15:22 LOGIN_FAILED user=admin ip=192.168.1.45
2026-03-13 10:15:30 LOGIN_FAILED user=admin ip=192.168.1.45
2026-03-13 10:15:35 LOGIN_FAILED user=admin ip=192.168.1.45
2026-03-13 10:16:10 LOGIN_SUCCESS user=john ip=192.168.1.20
```

These logs help identify suspicious login behavior.

---

## Python Script Example

```python
log_file = open("auth_log.txt", "r")

failed_attempts = {}

for line in log_file:
    if "LOGIN_FAILED" in line:
        ip = line.split("ip=")[1].strip()

        if ip in failed_attempts:
            failed_attempts[ip] += 1
        else:
            failed_attempts[ip] = 1

for ip, count in failed_attempts.items():
    if count > 3:
        print("Suspicious activity detected from IP:", ip)
```

---

## How the Script Works

1. The script reads a log file containing authentication events.
2. It identifies failed login attempts.
3. It counts how many times each IP address fails to authenticate.
4. If an IP exceeds a threshold of failed attempts, it is flagged as suspicious.

---

## Security Importance

Automated log analysis helps security analysts:

* Detect brute-force attacks
* Identify suspicious login activity
* Monitor authentication systems
* Respond quickly to potential threats

---

## Conclusion

Python scripting can significantly improve the efficiency of cybersecurity monitoring. Automating log analysis allows faster detection of suspicious activity and strengthens security operations.
