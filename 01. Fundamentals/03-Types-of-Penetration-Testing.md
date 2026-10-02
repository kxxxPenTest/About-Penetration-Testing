# Types of Penetration Testing
## 1. Overview
Penetration Testing can be categorized in several ways, depending on:
- How much information the tester receives
- Where the tester is positioned
- What type of system is being tested
- What security objective is being evaluated

The most common classification based on the amount of information provided to the tester is:\
- Black Box
- Grey Box
- White Box

Penetration testing can also be classified by the target:
- External Network
- Internal Network
- Web Application
- API
- Mobile Application
- Wireless Network
- Cloud Infrastructure
- Social Engineering
- Physical Security

## 2. Black Box Testing
### Definition
In a Black Box Penetration Test, the tester has little or no prior knowledge about the target:

The tester approaches the target similarly to an external attacker.

Typical information provided may include only:
- Target IP
- Domain
- Application URL

The tester then performs reconnaissance and discovers information independently.

#### Example
Suppose a company gives the tester:

https://example.com

No source code, credentials, architecture diagrams, or internal documentation are provided.

The tester must discover:
- Subdomains
- Open ports
- Services
- Technologies
- Directories
- Applications
- Potential vulnerabilities

The process may look like:\
Target -> Reconnaissance -> Scanning -> Enumeration -> Vulnerability Discovery -> Exploitation

#### Advantages
Black Box testing can provide a realistic view of an external attack because the tester starts with limited information.

It can help evaluate:
- External attack surface
- Publicly exposed services
- Information disclosure
- External application security
- Perimeter security

#### Limitations
Because the tester has limited information, some vulnerabilities may remain undiscovered.

For example:\
Internal Application -> Not publicly accessible -> Black Box tester cannot reach it

The test may therefore provide less coverage of internal functionality.

## 3. White Box Testing
### Definition
In a White Box Penetration Testing, the tester receives extensive information about the target environment.

Depending on the engagement, this may include:
- Source code
- Network diagrams
- Credentials
- Architecture documentation
- API documentation
- Database information
- Application documentation

The tester can use this information to perform a deeper assessment.

### Example
A company provides:
- Application source code
- API documentation
- Test credentials
- Database architecture
- Network diagram

The tester can then examine the application from both an external and internal perspective.

For example:\
Source Code -> Identify Input Handling -> Identify Authentication Logic -> Identify Authorization Issues -> Test Application -> Validate Findings

### Advantages
White Box testing can provide:
- Greater visibility
- Deeper code-level analysis
- Better coverage
- Ability to identify vulnerabilities that may not be visible externally

It can be especially useful for complex applications where understanding the internal architecture is important.

### Limitations
The test may not represent the exact experience of an external attacker because the tester has significantly more information.

## 4. Grey Box Testing
### Definition
Grey Box testing is between Black Box and White Box testing.\
The tester receives some information about the target but does not have complete knowledge of the environment.

For example:
- Username
- Password
- Basic application documentation
- Limited network information

The tester then performs the assessment with this limited internal knowledge.

### Example
A company provides:
- Application URL
- Normal user account
- Basic API documentation

The tester does not receive:
- Source code
- Administrator credentials
- Complete network architecture
- Database credentials

The tester can therefore evaluate the application from the perspective of an authenticated user.

### Advantages
Grey Box testing can provide a balance between:\
Realistic attack simulation + Greater testing coverage

It can be useful for testing:
- Authentication
- Authorization
- Privilege escalation
- Application functionality
- API security
- Role-based access control

## 5. Black Box vs Grey Box vs White Box
|Characteristic|Black Box|Grey Box|White Box|
|:--|:--|:--|:--|
|Information provided|Very limited|Partial|Extensive|
|Source code|Usually no|Usually no|Often yes|
|Credentials|Usually no|Often provided|Often provided|
|Tester knowledge|Low|Medium|High|
|External attacker simulation|Stronger|Moderate|Lower|
|Internal visibility|Limited|Moderate|High|
|Potential coverage|Lower|Moderate|Higher|
|Testing depth|Lower|Moderate|Higher|
|Time required for reconnaissance|Usually higher|Moderate|Usually lower|

The exact characteristics depend on the engagement and its scope.

## 6. External Penetration Testing
External penetration testing evaluates systems that are accessible from outside an organization's network.

Typical targets include:
- Public IP addresses
- Web applications
- VPN gateways
- Mail servers
- DNS servers
- Public APIs
- Remote access services

The tester may begin with:\
Internet -> Reconnaissance -> Attack Surface Discovery -> Scanning -> Enumeration -> Testing

The objective is to understand what an external attacker could discover and potentially exploit.

## 7. Internal Penetration Testing
Internal penetration testing evaluates systems from within an organization's network.

The tester may be given:
- Internal network access
or may begin with a limited internal foothold.

Typical targets include:
- Active Directory
- File servers
- Internal web applications
- Database servers
- Network devices
- Workstations
- Internal services

Important areas may include:
- Credential security
- Privilege escalation
- Lateral movement
- Access control
- Network segmentation
- Active Directory security

## Web Application Penetration Testing
Web application penetration testing focuses on the security of web applications.

Common areas include:
- Authentication
- Authorization
- Session Management
- Input Validation
- File Upload
- Access Control
- Business Logic
- API Security
- Information Disclosure

Common vulnerability classes include:
- SQL Injection
- Cross-Site Scripting (XSS)
- Server-Side Template Injection (SSTI)
- Command Injection
- File Upload vulnerabilities
- Broken Access Control

A typical workflow is:\
Recon -> Application Mapping -> Authentication Testing -> Authorization Testing -> Input Testing -> Business Logic Testing -> Vulnerability Validation -> Reporting

## 9. API Penetration Testing
API testing focuses on application programming interfaces.

Typical areas include:
- Authentication
- Authorization
- Input Validation
- Rate Limiting
- Data Exposure
- Object-Level Authorization
- API Configuration

For example:\
GET /api/users/123

A tester may investigate whether changing:\
123 -> 124

allows a user to access another user's data.

This type of issue may indicate an authorization weakness.

## 10. Mobile Application Penetration Testing
Mobile application testing evaluates applications running on platforms such as:
- Android
- iOS

Testing may include:
- Application Storage
- Authentication
- Authorization
- API Communication
- Cryptography
- Certificate Validation
- Sensitive Data Exposure
- Reverse Engineering

The tester may examine both:\
Mobile Application + Backend/API\
because mobile applications often depend heavily on backend services.

## 11. Wireless Network Penetration Testing
Wireless penetration testing evaluates the security of wireless networks.

Areas may include:
- Wi-Fi configuration
- Authentication
- Encryption
- Access Points
- Guest Networks
- Network Segmentation
- Rogue Access Points

Testing must be explicitly authorized because wireless testing can affect networks and devices outside the intended scope.

## 12. Cloud Penetration Testing
Cloud penetration testing evaluates cloud-hosted infrastructure and services.

Potential targets include:
- Virtual Machines
- Storage
- Cloud APIs
- Identify and Access Management
- Containers
- Serverless Applications
- Network Configuration

Testing must take into account:
- Cloud Provider Rules
- Customer Authorization
- Services Restrictions
- Testing Scope

Cloud environments may also involve shared infrastructure, so testing rules can differ from traditional infrastructure testing.

## 13. Social Engineering Testing
Social engineering assessments test whether people and organizational processes can resist specific authorized attack scenarios.

Example include:
- Phishing Simulations
- Pretexting
- Security Awareness Testing
- Physical Security Assessments

These assessments require clearly defined authorization and rules because they directly involve employees or physical locations.

## 14. Physical Security Testing
Physical penetration testing evaluates physical controls designed to protect systems and facilities.

Example include:
- Access Control
- Badge Systems
- Locks
- Restricted Areas
- Server Rooms
- Security Procedures

The goal is to determine whether unauthorized physical access could lead to security impact.

## 15. Choosing a Testing Type
Different testing types answer different questions.\
\
**External Test**\
Question: "What can an external attacker discover or potentially access?"


**Internal Test**\
Question: "What can an attacker do after gaining internal network access?"


**Web Application Test**\
Question: "Can weaknesses in the application be exploited?"


**API Test**\
Question: "Can API functionality or authorization controls be abused?"


**Mobile Test**\
Question: "Can weaknesses in the mobile application or its backend be exploited?"


**Cloud Test**\
Question: "Are cloud resources and identities securely configured?"

## 16. Combining Testing Types
A real penetration testing engagement may combine multiple approaches.\

For example:\
External Pentest -> Web Application Pentest -> Initial Access -> Internal Network -> Privilege Escalation -> Lateral Movement -> Impact Assessment

This can provide a broader understanding of an organization's security posture.

## 17. Key Concepts to Remember
The three major knowledge-based testing approaches are:\
Black Box -> Little information\
Grey Box -> Some information\
White Box -> Extensive information

The major target-based categories include:
- External
- Internal
- Web Application
- API
- Mobile
- Wireless
- Cloud
- Social Engineering
- Physical

These categories are not mutually exclusive.\
A single engagement can combine several testing types.

## 18. Summary
Penetration testing can be classified based on both the information available to the tester and the target being assessed.

Based on tester knowledge:
- Black Box -> Limited information
- Grey Box -> Partial Information
- White Box -> Extensive information

Based on target:
- External Network
- Internal Network
- Web Application
- API
- Mobile Application
- Wireless Network
- Cloud Infrastructure
- Social Engineering
- Physical Security

Understanding these classifications is important because the testing approach, scope, methodology, tools, and expected results can differ significantly between engagements.

Before performing any penetration test, the tester should understand:
1. What am I testing?
2. What am I allowed to test?
3. What information do I have?
4. What techniques are permitted?
5. What are the testing limitations?

This leads directly to the next fundamental topic:\
**Rules of Engagement (RoE)**
