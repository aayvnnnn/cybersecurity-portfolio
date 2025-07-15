# Network Hardening

## Table of contents

1. [Intro](#intro)
2. [Scenario](#scenario)
3. [Tools & Methods](#tools-methods)
4. [Explanation](#explanation)

## Introduction <a name="intro">

A network intrusion attack report for a fictional IT company. Completed as a part of my cybersecurity portfolio and as a part of the <a href='https://www.coursera.org/learn/networks-and-network-security?specialization=cybersecurity-certificate'>Connect and Protect: Networks and Network Security</a> course in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>..

The goal is to suggest security improvements for a social media organization to strengthen its defenses and reduce the risk of future data breaches after a recent attack.

## Scenario <a name="intro">

You are a security analyst working for a social media organization. The organization recently experienced a major data breach, which compromised the safety of their customers’ personal information, such as names and addresses. Your organization wants to implement strong network hardening practices that can be performed consistently to prevent attacks and breaches in the future. 

After inspecting the organization’s network, you discover four major vulnerabilities. The four vulnerabilities are as follows:

- The organization’s employees' share passwords.

- The admin password for the database is set to the default.

- The firewalls do not have rules in place to filter traffic coming in and out of the network.

- Multifactor authentication (MFA) is not used. 

If no action is taken to address these vulnerabilities, the organization is at risk of experiencing another data breach or other attacks in the future. 

In this activity, you will write a security risk assessment to analyze the incident and explain what methods can be used to further secure the network.

## Tools & Methods <a name="tools-methods">

- Implement Multi-Factor Authentication (MFA) to reduce reliance on passwords and add an extra layer of account security.
- Create & enforce strong password policies, requiring complex, unique passwords and regular updates.
- Maintain and regularly update firewalls to prevent unauthorized access and monitor incoming/outgoing traffic.
 
## Explanation <a name="explanation">

Enforcing Multi-Factor Authentication (MFA) significantly strengthens account security by requiring authentication through multiple factors, such as a password and a one-time code or biometric verification. It reduces the risk of password sharing, makes passwords less valuable to attackers, and helps prevent attacks such as brute force, credential stuffing, and unauthorized access.

Setting and enforcing a strict password policy within the organization will make it increasingly challenging for attackers to access the network. Policies like suspending an account after a specific number of logins can prevent brute force attacks. Requiring complex passwords, regular updates and disallowing reuse of passwords can also help discourage malicious actors from infiltrating the network.

Firewall maintenance should be performed regularly. Network administrators must ensure that firewall rules are kept up to date and align with the latest standards for allowed and denied traffic. Traffic originating from suspicious or unknown sources should be blocked or added to a deny list. Firewalls should also be promptly updated following any security incident, particularly those involving the network. This proactive approach helps defend against various threats, including Denial of Service (DoS) and Distributed Denial of Service (DDoS) attacks.
