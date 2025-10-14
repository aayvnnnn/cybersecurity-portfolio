# Access Controls 

## Table of contents 
1. [Intro](#intro) 
2. [Scenario](#scenario) 
3. [Worksheet](#worksheet) 

## Introduction <a name="intro"> 

This report analyzes a realistic access-control incident at a commercial bank. It focuses on identifying weaknesses in account lifecycle management, determining contributing factors to unauthorized access, and providing actionable recommendations.  
*(Originally completed as part of the Google Cybersecurity Professional Certificate.)*

## Scenario <a name="scenario"> 

Recently, a deposit was made from the business to an unknown bank account. The finance manager stated they hadn’t made a mistake. Fortunately, they were able to stop the payment in time. The owner requested an investigation to determine the cause and prevent future incidents.

An analysis of the access logs was conducted to understand how the incident occurred. During the process, key findings were documented, weaknesses in access controls were identified, and actionable recommendations were developed to strengthen the organization’s defenses and prevent recurrence.

## Worksheet <a name="worksheet">

| Category | Note(s) | Issue(s) | Recommendation(s)
| :--- | :--- | :--- | :--- | 
| Authentication & Authorization | On October 3, 2023, the user "Legal/Administrator" logged in from IP address 152.207.255.255. | Former administrator Robert Taylor Jr. accessed the payroll system in 2023, despite his contract ending in 2019. | Implement automatic deactivation of accounts upon contract termination or role change, conduct periodic reviews of user access, and enforce multi-factor authentication (MFA). |

## Summary 

The incident occurred due to a failure in the account deprovisioning process, which allowed a former administrator to retain active access credentials after their contract was terminated. This highlights gaps in identity lifecycle management and administrative management.

| Root Cause | Impact | Mitigation | 
| :--------- | :----- | :--------- |
| Inactive accounts not removed post-termination. | Unauthorized access to payroll systems. | Automate user offboarding, enforce MFA, and schedule regular access reviews for privileged accounts.



