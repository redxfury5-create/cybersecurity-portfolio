# Security Audit Report – Botium Toys

## Overview

This project involves conducting an internal security audit for Botium Toys, a small business with both physical and online operations. The purpose of the audit is to evaluate existing security controls and identify risks, vulnerabilities, and compliance gaps.

## Scope and Goals

The audit covers the entire IT infrastructure, including systems, networks, data storage, and business operations. The goal is to improve the organization's security posture and ensure compliance with industry standards.

## Key Findings

### Missing Controls

* No encryption for sensitive data
* No intrusion detection system (IDS)
* No data backups or disaster recovery plan
* No implementation of least privilege or separation of duties
* No password management system

### Weak Controls

* Password policies exist but are weak
* Legacy systems are not regularly monitored

### Existing Controls

* Firewall is implemented
* Antivirus software is active
* Physical security (locks, CCTV, fire systems) is in place

## Compliance Issues

### PCI DSS

* Credit card data is not properly secured
* Encryption is not implemented
* Access control is not restricted

### GDPR

* Data is not fully secured
* Data classification is missing
* Breach notification plan exists

### SOC

* Data integrity and availability are maintained
* Access control policies are not enforced

## Risk Assessment

The organization faces a high level of risk due to missing security controls and lack of compliance with industry standards. Sensitive data such as customer information and payment details are particularly vulnerable.

## Recommendations

* Implement encryption for sensitive data
* Deploy an intrusion detection system (IDS)
* Establish data backup and disaster recovery plans
* Enforce least privilege and separation of duties
* Strengthen password policies and introduce a password manager
* Improve compliance with PCI DSS and GDPR requirements

## Conclusion

This audit highlights several critical security gaps that need immediate attention. Addressing these issues will significantly improve Botium Toys' security posture and reduce the risk of data breaches and regulatory penalties.
