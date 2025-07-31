# Network Intrusion Attack Report

## Table of contents

1. [Intro](#intro)
2. [Scenario](#scenario)
3. [Identification](#identification)
4. [Explanation](#explanation)

## Introduction <a name="intro">

A network intrusion attack report for a fictional IT company. Completed as a part of my cybersecurity portfolio and as a part of the <a href='https://www.coursera.org/learn/networks-and-network-security?specialization=cybersecurity-certificate'>Connect and Protect: Networks and Network Security</a> course in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>..

The goal is to analyze and investigate a recent network attack, determine its type, and aggregate a report that explains it in a clear and structured format. 

## Scenario <a name="intro">

You work as a security analyst for a travel agency that advertises sales and promotions on the company’s website. The employees of the company regularly access the company’s sales webpage to search for vacation packages their customers might like. 

One afternoon, you receive an automated alert from your monitoring system indicating a problem with the web server. You attempt to visit the company’s website, but you receive a connection timeout error message in your browser.

You use a packet sniffer to capture data packets in transit to and from the web server. You notice a large number of TCP SYN requests coming from an unfamiliar IP address. The web server appears to be overwhelmed by the volume of incoming traffic and is losing its ability to respond to the abnormally large number of SYN requests. You suspect the server is under attack by a malicious actor. 

You take the server offline temporarily so that the machine can recover and return to a normal operating status. You also configure the company’s firewall to block the IP address that was sending the abnormal number of SYN requests. You know that your IP blocking solution won’t last long, as an attacker can spoof other IP addresses to get around this block. You need to alert your manager about this problem quickly and discuss the next steps to stop this attacker and prevent this problem from happening again. You will need to be prepared to tell your boss about the type of attack you discovered and how it was affecting the web server and employees.

## Identification <a name="identification">

One potential cause of the website's connection timeout errors is a Denial of Service (DoS) attack. The log file indicates that the server stopped responding after being swamped by SYN packets, which is known as a SYN flood attack.

## Explanation <a name="explanation">

When the users try to establish a connection with the web server, a three-way handshake occurs:

`
Firstly, a SYN (Synchronize) packet is sent from the client to the web server.
Then, the web server responds with a SYN/ACK (Synchronize/Acknowledge) packet, demonstrating that it has successfully received the packet and wants to establish a connection.
The client will lastly respond with an ACK (Acknowledge) packet to show that it recognizes the server's permission to connect.
`

In the event of a SYN flood attack, a malicious actor sends a large volume of SYN packets to a web server in rapid succession, causing it to initiate numerous half-open TCP connections. This overwhelms the server's resources, potentially crashing it or preventing it from responding to legitimate client requests.

The logs reveal that the web server is overwhelmed and unable to process incoming SYN requests. As a result, it cannot establish new connections, causing visitors to experience connection timeouts.
