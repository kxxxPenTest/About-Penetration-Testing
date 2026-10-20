# Penetration Testing Methodology

## 1. Overview
Penetration Testing Methodology is a structured approach used to perform a penetration test.

A methodology defines:
- What should be tested
- In what order testing should be performed
- What information should be collected
- How vulnerabilities should be validated
- How findings should be documented
- How remediation should be verified

A penetration test should not be performed randomly.\
\
A structured methodology helps testers work systematically and reduces the chance of missing important security issues.

## 2. General Penetration Testing Process
A typical penetration testing process can be represented as:
1. Planning & Scope
2. Reconnaissance
3. Scanning
4. Enumeration
5. Vulnerability Assessment
6. Exploitation
7. Privilege Escalation
8. Post-Exploitation
9. Evidence Collection
10. Reporting
11. Remediation
12. Retesting

The exact process can vary depending on:
- Target
- Scope
- Testing methodology
- Organization
- Rules of Engagement
- Type of penetration test

## 3. Phase 1 -- Planning and Scoping
Before technical testing begins, the tester needs to understand the engagement.

Important questions include:
- What systems are being tested?
- What systems are excluded?
- Who authorized the test?
- When can testing occur?
- What techniques are allowed?
- What techniques are prohibited?
- What should happen if a critical vulnerability is discovered?

#### Important information includes:
- Scope
- Objectives
- Authorization
- Testing Window
- Rules of Engagement
- Emergency Contacts
- Testing Restrictions

## 4. Scope
The scope defined what the penetration tester is authorized to test.\
\
Example:\
In Scope:\
192.168.10.10\
192.168.10.20\
example.com\
api.example.com\

Example of an excluded system:\
192.168.10.50\
\
The tester should not test excluded systems even if they are discovered during reconnaissance.

## 5. Rules of Engagement
Rules of Engagement define how the penetration test should be conducted.\
\
They may specify:
- Allowed testing techniques
- Testing hours
- Source IP addresses
- Allowed targets
- Prohibited actions
- Data handling requirements
- Communication procedures
- Emergency procedures

For example:
#### Allowed:
- Port scanning
- Web application testing
- Authentication testing

#### Not allowed:
- Denial-of-Service testing
- Destructive exploitation
- Deleting production data
- Testing third-party infrastructure

The Rules of Engagement protect both the organization and the penetration tester.

## 6. Phase 2 -- Reconnaissance
Reconnaissance is the process of gathering information about the target.\
\
The objective is to understand the attack surface before deeper testing begins.\
\
Information may include:
- IP addresses
- Domains
- Subdomains
- DNS records
- Technologies
- Employees
- Applications
- Public services
- Network information

#### Reconnaissance can be divided into:
Passive Reconnaissance + Active Reconnaissance

## 7. Passive Reconnaissance
Passive reconnaissance collects information without directly interacting with the target infrastructure in a significant way.\
\
Examples include:
- Search engines
- Public websites
- WHOIS information
- Public DNS information
- Certificate transparency records
- Public documentation
- Public code repositories
- Social media

The objective is to learn about the target  while minimizing direct interaction.

## 8. Active Reconnaissance
Active reconnaissance involves interacting directly with the target.\
Examples include:
- Port scanning
- Service detection
- HTTP requests
- DNS queries
- Directory enumerations
- Network discovery

For example:\
```nmap -sC -sV <target>```
\
Active reconnaissance can generate logs or alerts on the target system, so it should only be performed when authorized.

## 9. Phase 3 -- Scanning
Scanning is used to identify reachable systems, open ports, services, and other technical information.\
A common starting point is port scanning.\
For example:\
```nmap <target>```
\
\
Service Detection:\
```nmap -sV <target>```
\
\
Default scripts:\
```nmap -sC <target>```
\
\
Combined:\
```nmap -sC -sV <target>```
\
\
All TCP ports:\
```nmap -p- <target>```
\
\
The purpose is not simply to run Nmap.\
The tester needs to understand what the results mean.
