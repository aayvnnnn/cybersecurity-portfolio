# Access Controls 

## Table of contents 
1. [Intro](#intro) 
2. [Scenario](#scenario) 
3. [Worksheet](#worksheet) 

## Introduction <a name="intro"> 
An access control worksheet made for a commercial bank. Completed as part of my cybersecurity portfolio and as part of the <a href='https://www.coursera.org/learn/assets-threats-and-vulnerabilities?specialization=cybersecurity-certificate'> Assets, Threats, and Vulnerabilities</a>  course in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>. 

The goal is to identify, list, evaluate, and prioritize risks to help the organization focus on securing the most vulnerable ones. 

## Scenario <a name="scenario"> 

Review the scenario below. Then complete the step-by-step instructions.

You’re the first cybersecurity professional hired by a growing business.

Recently, a deposit was made from the business to an unknown bank account. The finance manager says they didn’t make a mistake. Fortunately, they were able to stop the payment. The owner has asked you to investigate what happened to prevent any future incidents.

To do this, you’ll need to do some accounting on the incident to better understand what happened. First, you will review the access log of the incident. Next, you will take notes that can help you identify a possible threat actor. Then, you will spot issues with the access controls that were exploited by the user. Finally, you will recommend mitigations that can improve the business' access controls and reduce the likelihood that this incident reoccurs.

## Worksheet <a name="worksheet">

| | Note(s) | Issue(s) | Recommendation(s)
| :--- | :--- | :--- | :--- | 
| Authentication/Authorization | <ul><li>The event took place on 10/03/23.</li><li>The user is Legal/Administrator.</li><li>The IP address of the computer used to login is 152.207.255.255.</li></ul> | <ul><li>Robert Taylor Jr. is an administrator.</li><li>He accessed payroll systems in 2023, after his contract ended in 2019.</li></ul> | <ul><li>User accounts should expire after they are not utilized or applicable (if the user has changed roles, their contract has ended, etc).</li><li>User access should be checked regularly.</li><li>MFA should be implemented.</li></ul> |
