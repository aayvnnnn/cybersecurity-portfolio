# Network Incident Report

## Table of contents

1. [Intro](#intro)
2. [Scenario](#scenario)
3. [Summary](#summary)
4. [Analysis](#analysis)

## Introduction <a name="intro">

An incident report (of a specific network log) for a fictional IT company. Completed as a part of my cybersecurity portfolio and as a part of the <a href='https://www.coursera.org/learn/networks-and-network-security?specialization=cybersecurity-certificate'>Connect and Protect: Networks and Network Security</a> course in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>..

The goal is to analyze a tcpdump log that contains information regarding a recent incident that prompted problems in the client company's website, determine the protocol that was affected during this event, and aggregate a report that explains the matter in a clear and structured format. 

## Scenario <a name="intro">

You are a cybersecurity analyst working at a company that specializes in providing IT services for clients. Several customers of clients reported that they were not able to access the client company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you attempt to visit the website and you also receive the error “destination port unreachable.”. To troubleshoot the issue, you load your network analyzer tool, tcpdump, and attempt to load the webpage again. To load the webpage, your browser sends a query to a DNS server via the UDP protocol to retrieve the IP address for the website's domain name; this is part of the DNS protocol. Your browser then uses this IP address as the destination IP for sending an HTTPS request to the web server to display the webpage. The analyzer shows that when you send UDP packets to the DNS server, you receive ICMP packets containing the error message: “udp port 53 unreachable.” 

![tcpdump log](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/LKXsnNIhT0e1mAz5AEvxog_d363c94e0a4f4a8b90b0be403f6ee1f1_mMBaLWLyXG2omYBcSdjuR8y5_S59zow1ZEPYdjNyJzA1B0r55nI9KmDosI8QHXcEwE51NxM3N5gNtMgSOyVDHyJVLZvZA7_jJtkzUKfxuqFUJPHs57vVVES-LbG5teR8eir4idaqsxFaYJhhVJZn-a_S-txb7zQNIZq07XESgSkqDHuzfvALfYk3lipGVBY?expiry=1749254400000&hmac=X89HG-KjNHkfPlwHIBUSwj4e1wsNeAYlV9gemxyow0o)

## Summary <a name="summary">

The UDP protocol cannot reach port 53, and the ICMP echo reply returns the error: "UDP port 53 unreachable". Since port 53 is typically used by DNS servers, this indicates that the DNS service is not responding.

## Analysis <a name="analysis">

The incident occured at around 1:24PM, as customers notified the IT team about how they were consistently recieving the error, "destination port unreachable", when they attempted to visit the website; the network team is currently looking into the issue to ensure the restoration of the website. In our investigation, we conducted packet sniffing using the tool, "tcpdump". The resulting log files showed that the DNS port 53 was unreachable. There could be various causes responsible for this incident, such as a misconfiguration, traffic being blocked, or a malicious attack such as a DoS/DDoS attack. 
