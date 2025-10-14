# Botium Toys Security Audit

## Table of contents

1. [Intro](#intro)
2. [Scenario](#scenario)
3. [Security Audit Workflow](#workflow)
4. [Controls Assessment](#control-assessment)
5. [Compliance Checklist](#compliance-checklist)
6. [Stakeholder Memo](#stakeholder-memo)
   
## Introduction <a name="intro">

This report presents a realistic audit of Botium Toys' cybersecurity program to ensure alignment with industry standards and best practices. It identifies vulnerabilities, prioritizes high-risk issues, provides mitigation recommendations, and outlines a strategic plan to enhance the organization's security posture. The report also documents discoveries, develops remediation plans, implements corrective actions, and keeps stakeholders informed throughout the process.
(Originally completed as part of the Google Cybersecurity Professional Certificate.)

## Scenario <a name="scenario">

Botium Toys is a small U.S. business that develops and sells toys. The company operates from a single physical location; however, its growing online presence has attracted customers both domestically and internationally. Their information technology (IT) department is under increasing pressure to support their online market worldwide. 

The IT department manager has decided that an internal IT audit needs to be conducted. She’s worried about maintaining compliance as the company grows. Operations could be disrupted without a clear plan. She believes an internal audit can help better secure the company’s infrastructure while identifying and mitigating risks to critical assets. The manager is also interested in ensuring that they comply with regulations related to processing online payments securely and conducting business in the European Union (EU).   

The IT manager starts by implementing the **National Institute of Standards and Technology Cybersecurity Framework** (NIST CSF), establishing an audit scope and goals, and completing a risk assessment. The audit provides an overview of potential risks in the company’s current security posture. The IT manager wants to use the audit findings as evidence to obtain approval to expand her department.

The goals/objectives for Botium Toys’ internal IT audit are:

- Ensure compliance with the National Institute of Standards and Technology Cybersecurity
Framework (NIST CSF).

- Standardize system management processes to ensure compliance.

- Enhance system controls, such as implementing multi-factor authentication to prevent unauthorized access.

- Implement the concept of least privilege on user credentials management.

- Establish policies and procedures (which include their playbooks).

- Maintain regulatory compliance.

### Internal Security Audit Workflow <a name="workflow">

The internal security audit can be summarized in four key steps:

1. Analyze the scope and goals of the audit/risk assessment.

2. Conduct the audit

   - Complete controls assessment 

     - Select controls required to be implemented.

     - Rate each selected control on priority (e.g., necessary to be implemented immediately or later).

   - Complete compliance checklist
   
     - Describe why selected compliance standards and regulations require adherence.
       
3. Review results from Step 2

   - Document findings.

   - Contemplate how to summarize your recommendations clearly and concisely to stakeholders.

4. Send suggestions and discoveries to stakeholders in a summarized format.

## Assets

Assets managed by the IT Department include:

- On-premises equipment for in-office business needs.

- Employee equipment: end-user devices (desktops/laptops, smartphones),
remote workstations, headsets, cables, keyboards, mice, docking stations,
surveillance cameras, etc.

- Storefront products available for retail sale on site and online; stored in the company’s adjoining warehouse.

- Management of systems, software, and services: accounting, telecommunication, database, security, e-commerce, and inventory management.

- Internet access.

- Internal network.

- Vendor access management.

- Data storage and retention.

- Data center hosting services.
  
- Badge readers.

- Legacy system maintenance: end-of-life systems that require human monitoring.

## Controls Assessment <a name="control-assessment">

### Administrative Controls 
| Control | Type | State | Priority | Notes |
| :-- | :-- | :-- | :-- | :-- |
| Least privilege | Preventative | Not implemented | Severe | Users have broad access, increasing risk of unauthorized changes. |
| Disaster recovery plans | Corrective | Not implemented | Severe | No tested procedures exist to restore systems after outages. |
| Password policies | Preventative | Not implemented | Severe | Weak or default passwords are still allowed, risking compromise. |
| Access control policies | Preventative | Not implemented | Severe | No formal rules on who can access sensitive systems. |
| Account management policies | Preventative | Not implemented | Severe | User accounts are not reviewed or deprovisioned promptly. |
| Separation of Duties (SoD) | Preventative | Not implemented | Severe | Critical functions lack checks, allowing fraud or errors. | 
 
### Technical Controls 
| Control | Type | State | Priority | Notes |
| :-- | :-- | :-- | :-- | :-- | 
| Firewall | Preventative | Implemented | N/A | Blocks standard attacks, but advanced threats may bypass. |
| Intrusion Detection System (IDS) | Detective | Not implemented | Severe | No alerts for suspicious activity will cause breaches to go unseen. | 
| Encryption | Deterrent | Not implemented | Severe | Sensitive data is unprotected, exposure is immediate risk, increasing likelihood of data breaches and regulatory non-compliance. | 
| Backups | Corrective | Not implemented | Severe | Single failure or attack could halt operations. | 
| Password management system | Corrective | Not implemented | Severe | Weak or reused passwords increase breach likelihood. |
| Endpoint Security (Antivirus & EDR) | Corrective | Not implemented | Severe | Endpoints vulnerable to malware and ransomware. | 
| Manual monitoring, maintenance, and intervention | Corrective | Not implemented | Severe | Legacy systems run unchecked causing failures to go unnoticed, and compliance violations could occur. |


### Physical Controls
| Control | Type | State | Priority | Notes | 
| :-- | :-- | :-- | :-- | :--- | 
| Time-controlled safe | Deterrent | Not implemented | Minor | Cash and valuables lack secure containment, raising risk of theft. |
| Adequate lighting | Deterrent | Not implemented | Minor | Poor lighting creates blind spots. |
| Closed-circuit Television (CCTV) surveillance | Detective | Not implemented | Severe | No monitoring: intrusions or errors go unrecorded. |
| Locking cabinets (for network gear) | Preventative | Not implemented | Moderate | Exposed gear causes risk of tampering or downtime. |
| Signage indicating alarm service provider | Deterrent | Not implemented | Minor | No visual deterrent for trespassers. |
| Locks | Preventative | Not implemented | Moderate | Unsecured critical areas causing obvious physical gaps. |
| Fire detection and prevention (fire alarm, etc.) systems | Detective | Not implemented | Moderate | Fire could destroy systems before detection. |


## Compliance Checklist

I discovered that Botium Toys will need to comply with the following standards:

-   General Data Protection Regulation (GDPR)
      
      - GDPR is a European Union (EU) regulation that protects the privacy and processing of European citizens' data inside and outside of Europe. GDPR also states that if a breach occurs in which a European citizen's data is compromised, they must be informed within 72 hours of the incident.

      - Botium Toys is expanding to offer services and handle the data of international customers. GDPR compliance is in scope for handling data and personal information about European customers.
       
-   Payment Card Industry Data Security Standard (PCI DSS)

    - PCI DSS is an international security standard designed to ensure that organizations store, process, accept, and transmit credit card data securely, minimizing the risk of fraud and breaches. 

    - Botium Toys must comply with PCI DSS as it processes and stores customer credit card information online and in physical locations. Adhering to PCI DSS is critical, as non-compliance can lead to severe consequences, including monthly fines ranging from $5,000 to $100,000, costly forensic assessments in the event of a data breach, restrictions on payment processing, reputational damage, and potential lawsuits.

-   System and Organizations Controls (SOC type 1, SOC type 2):

    - SOC 1 and SOC 2 are two types of reports that evaluate an organization's internal controls. SOC 1 assesses financial reporting controls, whereas SOC 2 focuses on controls pertaining to the Trust Services Criteria (TSC) that includes security, availability, processing integrity, confidentiality, and privacy. These reports help organizations demonstrate compliance and mitigate risks. Failures in these areas can lead to security breaches, financial fraud, and a weakened security posture.

    - Botium Toys must establish and maintain proper user access for internal personnel and third-party vendors to mitigate risk and ensure data integrity.
      
To learn more about compliance regulations and standards, read the [controls, frameworks, and compliance](https://www.coursera.org/learn/foundations-of-cybersecurity/supplement/xu4pr/controls-frameworks-and-compliance) document. 
   

## Stakeholder Memorandum <a name="stakeholder-memo">

To: IT Managers, Stakeholders

From: Aayan Zaidi

Date: March 9, 2025

Subject: Internal Security Audit Findings and Recommendations

Dear Colleagues,

Please take a look at the following information on the Botium Toys internal audit, including its scope, goals, critical findings, summary, and recommendations.


### Scope

- The following systems are within scope: 

  - Accounting software 

  - Endpoint Security (Antivirus & EDR)

  - Firewalls

  - Intrusion Detection System (IDS)

  - Security Information and Event Management (SIEM) tools. 

- These systems will be assessed for:

  - Current user permissions.

  - Current implemented controls.

  - Current procedures and protocols.

- Ensure that user permissions, controls, procedures, and asset management comply with GDPR and PCI DSS, covering both hardware and system access.

### Goals

- Ensure compliance with the National Institute of Standards and Technology Cybersecurity
Framework (NIST CSF).

- Standardize system management processes to ensure compliance.

- Enhance system controls, such as implementing multi-factor authentication to prevent unauthorized access.

- Implement the concept of least privilege on user credentials management.

- Establish policies and procedures (which include their playbooks).

- Maintain regulatory compliance.

### Critical findings (require immediate consideration)

- Principle of Least Privilege and Separation of Duties (SoD).

- Disaster recovery plans.

- Password, access control, and account management policies.

- Intrusion Detection System (IDS).

- Encryption (secure website transactions and disk drives containing sensitive information).

- Backups.

- Implementation of a password management system.

- Endpoint Security (Antivirus & EDR).

- Manual monitoring, maintenance, and intervention for legacy systems.

- Closed-circuit Television (CCTV).

- Locks.

- Locking cabinets (for networking gear).

- Fire detection and prevention systems (fire alarm, etc.).

### Findings (to be addressed later)

- Time-controlled safe

- Adequate lighting

- Signage indicating alarm service provider for restricted areas

### Policy development & implementation to

- Meet PCI DSS and GDPR compliance requirements.

- Comply with SOC 1 and SOC 2 guidelines regarding user access policies and overall data security.

### Summary

Addressing critical findings related to PCI DSS and GDPR compliance is crucial, especially as Botium Toys facilitates online payments and expands into international markets, including the European Union (EU). Implementing SOC 1 and SOC 2 guidelines to establish effective policies and enforce the principle of least privilege will help ensure compliance.

Additionally, implementing disaster recovery plans and maintaining regular backups will ensure business continuity during potential incidents. Integrating IDS and antivirus (AV) software will bolster intrusion detection and mitigation. Legacy systems requiring manual monitoring and intervention should be closely observed.

To secure assets physically, implementing locks, CCTV, and a time-controlled safe is highly recommended. Adequate lighting and signage indicating alarm service providers will further strengthen the security posture.

