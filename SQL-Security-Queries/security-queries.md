# SQL Security Queries

## Objective

The objective of this exercise is to demonstrate how SQL queries can be used to analyze login data and detect suspicious activity that may indicate a potential cyber attack.

---

## Background

Security analysts often review authentication logs to detect suspicious behavior such as:

* Multiple failed login attempts
* Logins from unusual locations
* Access attempts outside normal working hours

SQL allows analysts to quickly filter and analyze large datasets.

---

## Example Table: Login Attempts

Assume a database table called **login_attempts** containing the following fields:

* user_id
* username
* login_time
* ip_address
* login_status

---

## Detect Multiple Failed Login Attempts

This query identifies users who have multiple failed login attempts.

```
SELECT username, COUNT(*) AS failed_attempts
FROM login_attempts
WHERE login_status = 'failed'
GROUP BY username
HAVING COUNT(*) > 5;
```

Security analysts use queries like this to detect **possible brute-force attacks**.

---

## Identify Suspicious Login Times

This query identifies login attempts outside normal business hours.

```
SELECT username, login_time
FROM login_attempts
WHERE login_time NOT BETWEEN '08:00:00' AND '18:00:00';
```

This helps detect **unusual activity that might indicate unauthorized access**.

---

## Identify Suspicious IP Addresses

This query lists login attempts from unknown or suspicious IP addresses.

```
SELECT username, ip_address, login_time
FROM login_attempts
WHERE ip_address NOT IN ('192.168.1.10', '192.168.1.20');
```

Security teams often monitor unfamiliar IP addresses to detect possible intrusions.

---

## Security Importance

SQL queries allow cybersecurity professionals to:

* Detect brute-force attacks
* Identify suspicious login patterns
* Investigate unauthorized access
* Monitor system activity

By analyzing log data, analysts can detect threats early and respond quickly.

---

## Conclusion

SQL is an important tool for cybersecurity professionals because it allows efficient analysis of security logs and authentication data. Proper use of SQL queries helps detect suspicious activity and improve overall system security.
