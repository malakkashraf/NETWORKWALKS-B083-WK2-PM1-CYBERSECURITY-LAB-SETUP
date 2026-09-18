# NETWORKWALKS-B083-WK2-PM1-CYBERSECURITY-LAB-SETUP


**Track:** Cybersecurity Fundamentals  
**Environment:** Kali Linux  
**Target:** `networkwalks.com`  
**Exercise:** Authorized Reconnaissance

## Overview

This lab focused on using reconnaissance tools in Kali Linux to collect publicly available information about an assigned web domain. The exercise covered domain registration, web technology identification, DNS resolution, HTTP headers, WAF detection, DNS enumeration, and open-source information gathering.

## Authorization & Responsible Testing

All activities documented in this repository were performed as part of an authorized cybersecurity exercise. The tools were used for information gathering and reconnaissance only.

No exploitation, unauthorized access, or attempts to compromise the target were performed.

Reconnaissance commands should only be used against systems and domains where appropriate permission has been provided.

## Purpose of the Exercise

The information-gathering stage is an important part of a security assessment. Before investigating potential vulnerabilities, security professionals first need to understand what information is publicly visible about a target.

This exercise provided hands-on practice with several tools that can be used to build an initial picture of a web domain and its publicly exposed infrastructure.

## Reconnaissance Method

**Target:** `networkwalks.com`

| Step | Tool | Purpose |
|------|------|---------|
| 1 | WHOIS | Retrieve domain registration information |
| 2 | WhatWeb | Identify web technologies |
| 3 | NSLookup | Resolve the domain to an IP address |
| 4 | cURL | Inspect HTTP response headers |
| 5 | Wafw00f | Check for a detectable WAF |
| 6 | DNSRecon | Enumerate DNS records |
| 7 | theHarvester | Gather publicly available information |

## Step 1 — WHOIS

The WHOIS command was used to examine publicly available registration information associated with the target domain.

**Command:** `whois networkwalks.com`

![Step 1](1-Step-one.png)

## Step 2 — WhatWeb

WhatWeb was used to fingerprint the website and identify technologies that could be detected from the target.

**Command:** `whatweb networkwalks.com`

![Step 2](2-Step-two.png)

## Step 3 — DNS Resolution

NSLookup was used to determine the IP address associated with the target domain.

**Command:** `nslookup networkwalks.com`

**Result:** `192.232.216.135`

![Step 3](3-Step-three.png)

## Step 4 — HTTP Headers

cURL was used to inspect the HTTP response headers returned by the target website.

**Command:** `curl -I https://networkwalks.com`

![Step 4](4-Step-four.png)

## Step 5 — WAF Detection

Wafw00f was used to determine whether a Web Application Firewall could be detected protecting the website.

**Command:** `wafw00f networkwalks.com`

![Step 5](5-Step-five.png)

## Step 6 — DNS Enumeration

DNSRecon was used to gather publicly available DNS records and information associated with the domain.

**Command:** `dnsrecon -d networkwalks.com`

![Step 6](6-Step-six.png)

## Step 7 — Open-Source Reconnaissance

theHarvester was used to gather publicly available information related to the target domain from open sources.

![Step 7](7-Step-seven.png)

## Findings Summary

The seven reconnaissance activities provided different types of information about the target:

- **WHOIS:** Domain registration information
- **WhatWeb:** Detectable web technologies
- **NSLookup:** Domain-to-IP resolution
- **cURL:** HTTP response information
- **Wafw00f:** WAF detection results
- **DNSRecon:** Public DNS records
- **theHarvester:** Publicly available domain-related information

The DNS resolution step successfully identified `192.232.216.135` as the IP address returned for `networkwalks.com`.

## Security Perspective

Reconnaissance can reveal information about a target's technology stack, DNS infrastructure, web configuration, and publicly accessible data.

However, discovering information does not automatically mean that a security vulnerability exists. Further authorized assessment would be required to determine whether any finding represents an actual security weakness.

## Key Takeaways

This exercise helped develop practical experience with:

- Linux-based reconnaissance tools
- Domain and DNS enumeration
- Web technology fingerprinting
- HTTP header analysis
- WAF identification
- Open-source intelligence gathering
- Documenting technical results with evidence

The lab demonstrated how multiple reconnaissance techniques can be combined to create an initial overview of a target's publicly visible infrastructure.

## Tools & Skills

`Kali Linux` `Cybersecurity` `Network Reconnaissance` `Web Reconnaissance` `DNS Enumeration` `OSINT` `WHOIS` `WhatWeb` `NSLookup` `cURL` `Wafw00f` `DNSRecon` `theHarvester`

## Author

**Author:** [Your Name]

**Field:** Cybersecurity / Information Security

**Environment:** Kali Linux
