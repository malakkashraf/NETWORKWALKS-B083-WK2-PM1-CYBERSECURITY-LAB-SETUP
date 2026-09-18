# NETWORKWALKS-B083-WK2-PM1-CYBERSECURITY-LAB-SETUP
This repository shows all the steps of setting up my foot printing & reconnaissance attacks using Kali Tools.
**Track:** Cybersecurity Fundamentals  
**Environment:** Kali Linux  
**Target:** `networkwalks.com`

## Overview

This lab focused on reconnaissance and information gathering using common Kali Linux tools. The goal was to collect publicly available information about the assigned domain and document the results.

## Step 1 — WHOIS Domain Information

Used `whois` to retrieve publicly available domain registration details.

**Command:** `whois networkwalks.com`

![Step 1](1-Step-one.png)

## Step 2 — Web Technology Fingerprinting

Used WhatWeb to identify technologies and services associated with the website.

**Command:** `whatweb networkwalks.com`

![Step 2](2-Step-two.png)

## Step 3 — DNS Resolution

Used NSLookup to resolve the domain to its IP address.

**Command:** `nslookup networkwalks.com`

**Result:** `192.232.216.135`

![Step 3](3-Step-three.png)

## Step 4 — HTTP Header Analysis

Used cURL to inspect the HTTP response headers.

**Command:** `curl -I https://networkwalks.com`

![Step 4](4-Step-four.png)

## Step 5 — WAF Detection

Used Wafw00f to check whether a Web Application Firewall was detected.

**Command:** `wafw00f networkwalks.com`

![Step 5](5-Step-five.png)

## Step 6 — DNS Enumeration

Used DNSRecon to enumerate publicly available DNS records.

**Command:** `dnsrecon -d networkwalks.com`

![Step 6](6-Step-six.png)

## Step 7 — Open-Source Information Gathering

Used theHarvester to gather publicly available information related to the target.

**Command:** `theHarvester`

![Step 7](7-Step-seven.png)

## Tools Used

- WHOIS — Domain information
- WhatWeb — Technology fingerprinting
- NSLookup — DNS resolution
- cURL — HTTP header analysis
- Wafw00f — WAF detection
- DNSRecon — DNS enumeration
- theHarvester — Open-source information gathering

## Key Takeaway

This exercise provided practical experience with reconnaissance techniques and demonstrated how different tools can be used together to understand a target's publicly visible infrastructure.

## Ethical Consideration

All activities documented in this repository were performed as part of an authorized cybersecurity exercise. No exploitation or unauthorized access was performed.

## Author

**Author:** [Your Name]
