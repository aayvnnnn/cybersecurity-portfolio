# NIST Incident Report

## Table of contents

1. [Intro](#intro)
2. [Scenario](#scenario)
3. [Summary](#summary)
4. [Analysis](#analysis)
## Introduction <a name="intro">

An incident report for a fictional multimedia company. Completed as a part of my cybersecurity portfolio and as a part of the <a href='https://www.coursera.org/learn/networks-and-network-security?specialization=cybersecurity-certificate'>Connect and Protect: Networks and Network Security</a> course in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>..

The goal is to suggest security improvements for a multimedia organization based on the NIST CSF to strengthen its security posture and reduce the risk of future incidents after a recent DDoS attack.

## Scenario <a name="intro">

You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack. 

To address this security event, the network security team implemented: 

- A new firewall rule to limit the rate of incoming ICMP packets

- Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets

- Network monitoring software to detect abnormal traffic patterns

- An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics

As a cybersecurity analyst, you are tasked with using this security event to create a plan to improve your company’s network security, following the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF). You will use the CSF to help you navigate through the different steps of analyzing this cybersecurity event and integrate your analysis into a general security strategy. We have broken the analysis into different parts in the template below. You can explore them here:

- Identify security risks through regular audits of internal networks, systems, devices, and access privileges to identify potential gaps in security. 

- Protect internal assets through the implementation of policies, procedures, training and tools that help mitigate cybersecurity threats. 

- Detect potential security incidents and improve monitoring capabilities to increase the speed and efficiency of detections. 

- Respond to contain, neutralize, and analyze security incidents; implement improvements to the security process. 

- Recover affected systems to normal operation and restore systems data and/or assets that have been affected by an incident. 

## Summary <a name="summary">

The organization faced a DDoS attack that exploited an unconfigured firewall. The team successfully defended against the attack by implementing network monitoring software, reviewing firewall rules, and deploying an IDS/IPS system. To ensure business continuity, only critical services were restored, while non-critical services were temporarily suspended.

## Analysis <a name="analysis">

- Identify: The organization faced a DDoS attack, specifically an ICMP flood attack that disturbed the internal network, resulting in a situation where no legitimate traffic could access any network resources. The attack infiltrated the network through an unconfigured firewall.

- Protect: The incident management team responded by adding a new firewall rule to limit the rate of incoming ICMP packets.

- Detect: The network security team implemented an IDS/IPS system to filter out ICMP traffic based on specific suspicious characteristics.

- Respond: They implemented network monitoring software, along with source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets. 

- Recover: The incident management team stopped all non-critical network services, restoring only critical ones.
