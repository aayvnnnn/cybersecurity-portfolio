# Botium Toys Security Audit

## Table of contents

1. [Intro](#intro)
2. [Scenario](#scenario)
3. [Security Audit Workflow](#workflow)
4. [Controls Assessment](#control-assessment)
5. [Compliance Checklist](#compliance-checklist)
6. [Stakeholder Memo](#stakeholder-memo)
7. [Conclusion](#conclusion)

## Introduction <a name="intro">

An internal security audit performed on Botium Toys, a fictional toy company. Completed as a part of my cybersecurity portfolio and as a part of the <a href='https://www.coursera.org/learn/manage-security-risks?specialization=cybersecurity-certificate'> Play It Safe: Manage Security Risks </a> course 
in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>.
   
The goal is to audit Botium Toys' cybersecurity program to ensure it aligns with industry standards and best practices. The audit will identify vulnerabilities, prioritize "high-risk" issues, and provide suggestions for mitigation. It will also outline a strategic plan to strengthen the organization's security posture. The audit team will document their discoveries, develop remediation plans, implement corrective actions, and keep stakeholders updated throughout the process.

## Scenario <a name="scenario">

Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location. However, its online presence has grown, attracting customers in the U.S. and abroad. Their information technology (IT) department is under increasing pressure to support their online market worldwide. 

The manager of the IT department has decided that an internal IT audit needs to be conducted. She's worried about maintaining compliance and business operations as the company grows without a clear plan. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets. The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).   

The IT manager starts by implementing the **National Institute of Standards and Technology Cybersecurity Framework** (NIST CSF), establishing an audit scope and goals, and completing a risk assessment. The goal of the audit is to provide an overview of the risks the company might experience due to the current state of its security posture. The IT manager wants to use the audit findings as evidence to obtain approval to expand his department.

The goals/objectives for Botium Toys’ internal IT audit are:

- Comply with the National Institute of Standards and Technology Cybersecurity
Framework (NIST CSF).

- Initiate a better process for their systems to ensure they are compliant.

- Bolster system controls.

- Implement the concept of least privilege pertaining to user credentials management.

- Establish policies and procedures (which includes their playbooks).

- Ensure they are fulfilling compliance requirements.

### Internal Security Audit Workflow <a name="workflow">

The internal security audit can be boiled down into these 4 steps.

1. Analyze the scope and goals of the audit/risk assessment.

2. Conduct the audit

   - Complete controls assessment 

     - Select controls required to be implemented.

     - Rate each selected control on priority (e.g, necessary to be implemented immediately or later).

   - Complete compliance checklist
   
     - Describe why selected compliance standards and regulations require adherence.
       
4. Review results from Step 2

   - Document findings.

   - Contemplate how to summarize your recommendations clearly and concisely to stakeholders.

6. Send suggestions and discoveries to stakeholders in a summarized format.

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
| Control | Type | State | Priority |
| --- | --- | --- | --- |
| Least privilege | Preventative | Not implemented | Severe |
| Disaster recovery plans | Corrective | Not implemented | Severe |
| Password policies | Preventative | Not implemented | Severe |
| Access control policies | Preventative | Not implemented | Severe |
| Account management policies | Preventative | Not implemented | Severe |
| Separation of Duties (SoD) | Preventative | Not implemented | Severe |
 
### Technical Controls 
| Control | Type | State | Priority |
| --- | --- | --- | --- |
| Firewall | Preventative | Implemented | N/A |
| Intrusion Detection System (IDS) | Detective | Not implemented | Severe |
| Encryption | Deterrent | Not implemented | Severe |
| Backups | Corrective | Not implemented | Severe |
| Password management system | Corrective | Not implemented | Severe |
| Antivirus (AV) software | Corrective | Not implemented | Severe |
| Manual monitoring, maintenance, and intervention | Preventative/Corrective | Not implemented | Severe/Moderate |


### Physical Controls
| Control | Type | State | Priority |
| --- | --- | --- | --- |
| Time-controlled safe | Deterrent | Not implemented | Minor |
| Adequate lighting | Deterrent | Not implemented | Minor |
| Closed-circuit Television (CCTV) surveillance | Preventative/detective | Not implemented | Severe/Moderate |
| Locking cabinets (for network gear) | Preventative | Not implemented | Moderate |
| Signage indicating alarm service provider | Deterrent | Not implemented | Minor |
| Locks | Preventative | Not implemented | Moderate/Minor |
| Fire detection and prevention (fire alarm, etc.) | Detective/Preventative | Not implemented | Moderate |


## Compliance Checklist

I discovered that Botium Toys will need to comply with the following standards:

-   General Data Protection Regulation (GDPR)
      
      - GDPR is a European Union (E.U.) regulation that protects the privacy and processing of European citizens' data inside and outside of Europe. GDPR also states that if a breach occurs in which a European citizen's data is compromised, they must be informed within 72 hours of the incident.

      - Botium Toys is expanding to offer services and handle the data of international customers. GDPR compliance is in scope for handling data and personal information about European customers.
       
-   Payment Card Industry Data Security Standard (PCI DSS)

    - PCI DSS is an international security standard designed to ensure that organizations store, process, accept, and transmit credit card data securily, minimizing the risk of fraud and breaches. 

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

</br>

Dear Colleagues,

Please take a look at the following information on the Botium Toys internal audit, including its scope, goals, critical findings, summary, and recommendations.


### Scope

- The following systems are within scope: 

  - Accounting software 

  - Endpoint detection solutions

  - Firewalls

  - intrusion detection systems

  - Security Information and Event Management (SIEM) tools. 

- These systems will be assessed for:

  - Current user permissions.

  - Current implemented controls.

  - Current procedures and protocols.

- Ensuring that current user permissions, controls, procedures, protocols, technology, and asset management align with GDPR and PCI DSS compliance requirements while accounting for both hardware and system access.

### Goals

- Comply with the National Institute of Standards and Technology Cybersecurity
Framework (NIST CSF).

- Initiate a better process for their systems to ensure they are compliant.

- Bolster system controls.

- Implement the concept of least privilege pertaining to user credentials management.

- Establish policies and procedures (which includes their playbooks).

- Ensure they are fulfilling compliance requirements.

### Critical findings (require immediate consideration)

- Principle of Least Privilege and Separation of Duties (SoD).

- Disaster recovery plans.

- Password, access control, and account management policies.

- Intrusion Detection System (IDS).

- Encryption (secure website transactions wand disk drive(s) containing sensitive information).

- Backups.

- Implementation of a password management system.

- Antivirus (AV) software.

- Manual monitoring, maintenance, and intervention for legacy systems.

- Closed-circuit television (CCTV).

- Locks.

- Locking cabinets (for networking gear).

- Fire detection and prevention systems.

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

## Conclusion <a name="conclusion">
This wraps up my mock security audit write-up. I hope you found it as insightful and useful as I did. If you have any constructive feedback or suggestions for improvement, feel free to share them.

