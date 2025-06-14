# OS Hardening

## Table of contents

1. [Introduction](#intro)
2. [Scenario](#scenario)
3. [Identification](#identification)
4. [Documentation](#documentation)

## Introduction <a name="intro">

An investigation conducted for a fictional IT company. Completed as a part of my cybersecurity portfolio and as a part of the <a href='https://www.coursera.org/learn/networks-and-network-security?specialization=cybersecurity-certificate'>Connect and Protect: Networks and Network Security</a> course in Google's <a href='https://www.coursera.org/google-certificates/cybersecurity-certificate'>Cybersecurity Professional Certificate</a> on <a href='https://www.coursera.org/'>Coursera</a>..

The goal is to analyze a recent incident that resulted in various problems and showed malicious intervention in the company's website, identify the one protocol that was exploited during this event, recommend a remediation and mitigation strategy, and aggregate a report that explains the matter in a clear and structured format. 

## Scenario <a name="intro">

You are a cybersecurity analyst for yummyrecipesforme.com, a website that sells recipes and cookbooks. A former employee has decided to lure users to a fake website with malware. 

The former employee/ hacker executed a brute force attack to gain access to the web host. They repeatedly entered several known default passwords for the administrative account until they correctly guessed the right one. After they obtained the login credentials, they were able to access the admin panel and change the website’s source code. They embedded a javascript function in the source code that prompted visitors to download and run a file upon visiting the website. After embedding the malware, the hacker changed the password to the administrative account. When customers download the file, they are redirected to a fake version of the website that contains the malware. 

Several hours after the attack, multiple customers emailed yummyrecipesforme’s helpdesk. They complained that the company’s website had prompted them to download a file to access free recipes. The customers claimed that, after running the file, the address of the website changed and their personal computers began running more slowly. 

In response to this incident, the website owner tries to log in to the admin panel but is unable to, so they reach out to the website hosting provider. You and other cybersecurity analysts are tasked with investigating this security event.

To address the incident, you create a sandbox environment to observe the suspicious website behavior. You run the network protocol analyzer tcpdump, then type in the URL for the website, yummyrecipesforme.com. As soon as the website loads, you are prompted to download an executable file to update your browser. You accept the download and allow the file to run. You then observe that your browser redirects you to a different URL, greatrecipesforme.com, which contains the malware.  

The logs show the following process:

- The browser initiates a DNS request: It requests the IP address of the yummyrecipesforme.com URL from the DNS server.

- The DNS replies with the correct IP address. 

- The browser initiates an HTTP request: It requests the yummyrecipesforme.com webpage using the IP address sent by the DNS server.

- The browser initiates the download of the malware.

- The browser initiates a DNS request for greatrecipesforme.com.

- The DNS server responds with the IP address for greatrecipesforme.com.

- The browser initiates an HTTP request to the IP address for greatrecipesforme.com.

A senior analyst confirms that the website was compromised. The analyst checks the source code for the website. They notice that javascript code had been added to prompt website visitors to download an executable file. Analysis of the downloaded file found a script that redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com. 

The cybersecurity team reports that the web server was impacted by a brute force attack. The disgruntled hacker was able to guess the password easily because the admin password was still set to the default password. Additionally, there were no controls in place to prevent a brute force attack. 

Your job is to document the incident in detail, including identifying the network protocols used to establish the connection between the user and the website.  You should also recommend a security action to take to prevent brute force attacks in the future.

## Identification <a name="identification">

The HyperText Transfer Protocol (HTTP) was exploited during the incident. This can be deduced, as the issue was with accessing the web server for yummyrecipesforme.com, and we know that requests to web servers for web pages involve HTTP traffic.

Another observation supporting this conclusion, would be that when we ran "tcpdump" and visited the "yummyrecipesforme.com" website, the log file showed the usage of the HTTP protocol when contacting the webpage, which resulted in a malicious file being downloaded (at the application layer) and a redirection occurring. 

## Documentation <a name="analysis">

The incident came to notice when several customers began contacting the company's helpdesk, and notified them about a file being downloaded (misrepresented to be a file containing new recipes) when they attempted to visit the website. The users' computers have been operating slowly since. The website owner tried logging into the administrator portal, but noticed their account was locked out.

The cybersecurity analyst used a sandbox environment to open the website in an isolated environment (so that it does not affect the company's network). Then, the analyst utilized "tcpdump" to capture the network traffic produced by visiting the website. The analyst was prompted to download a file that claimed it contained new recipes. The analyst then accepted the download and ran the file. The browser than redirected the analyst to a fake website, "greatrecipesforme.com"
The analyst was prompted to download a file claiming it would provide access to free recipes, accepted the download and ran it. The browser then redirected the analyst to a fake website (greatrecipesforme.com).
