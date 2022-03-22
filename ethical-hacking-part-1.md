# Security Testing and Cyber-Security: Use Case Simulated Man in The Middle Attack and Prevention

## Author:
- Truc Huynh
- Mohammed Alswairki
- [Link to Research Paper-Word File](https://ind657-my.sharepoint.com/:w:/g/personal/huyntl02_pfw_edu/EREQ8HZ5ZnpEmlgh66AqLR0Bc5Aj6R21wPnLuFMnwC4k5g?e=LA2CBC)

## Keywords:

- Software Testing: 
- Software Testing Life Cycle(STLC): Software Testing Life Cycle (STLC) is a sequence of specific activities conducted during the testing 
process to ensure software quality goals are met. STLC involves both verification and validation activities. There are 6 steps of STLC:
Requirement Analysis, Test Planning, Test Cases Designing, Test Enviroment Setup, Test Execution.
- Software Quality: Computer programs, procedures, and possibly associated documentation and data pertaining to the operations of the system (IEEE).
Four component that need to assure the quality of the software development: code, procedures, documentation, data to operating the software system (from [2])
- Secure Software Testing: testing methods that determine software products protects data and maintains security specification as given.
- Secure Programing Practice: is the practice of developing computer software in such a way that guards against the accidental introduction of security vulnerabilities
- Security Breaches: A security breach happen when a system fail in its security processes and cause unauthorized party access to the system. A security breach can happen by software problems (error, fault, failures), outdated security technology, ransomware, malware ...

## Abstract:
- The paper introduce security testing principles. 
- The paper also discuss about types of security testing.
- The relationship between STLC, SDLC, and security testing
- A Use case of simulating Man-In-The-Middle Attack on a system, and the tools that can be used in an Man-In-The-Middle Attack (Python, Kali Linux, Web Application Security Testing)
- Overview of Penetration Testing Methods(Pen Testing) and its related work

## Introduction:
### A. Software Security Testing:
- Security Testing or Software Testing Security determines that software protects data and maintains security specification as given. 
Another word to say: "security testing uncovers vulnerabilities of the system and determines that the data and resources of the system are well protected".
It ensures that the software system and application are free from any threats or risks that can cause a loss.
- To understand and implement good security test plans we must understand what is software quality, software development framework (SDLC)
software testing lifecycle (STLC), and software requirements.
- We also need to understand major issues that cause security breaches.
- Security-related bugs can differ from traditional bugs in a number of ways:
  - Security testing is often fundamentally different from traditional testing because it emphasizes what an application 
  should not do rather than what it should do, as pointed out in [9],
  - Malicious attackers do intelligently search for vulnerabilities. If they succeed, they cause problems for other users, 
  who may be adversely affected. Compounding the problem, malicious hackers are known to script successful attacks and distribute them.[9]
  - Since most developers are not currently trained in secure programming practices, security analysts carry a greater 
  burden in verifying that secure programming practices are adhered to.[9]
  - Many security requirements can be neither refined nor dropped even if they are untestable. e.g. 
  ”an attacker should never be able to take control of the application,” would be regarded as untestable in a traditional software development setting [9]
- The result is that secure software development is intrinsically harder than traditional software development.
Therefore, testing also has an expanded role. Software testing also has other strengths that can be leveraged during secure software development
  - Testing can help confirm that the developers did not overlook some insecure programming practices.
  - A vulnerability is usually taken more seriously if there is a known exploit for it, but developing exploits is the domain of penetration testing 
  - Testing can be used to help identify and mitigate risks from third-party components, where development artifacts like source code and architecture diagrams are unavailable.
  - Testing can be used to provide metrics of software insecurity and help raise the alarm when software is seriously flawed from the security standpoint.
  - Every design artifact views the software system at a certain level of abstraction. Attackers like to find the abstractions used by developers and work their way around them. 
  No person or group can view a software system at all possible levels of abstraction, but testing can help by perhaps finding (at least some) flaws that are not visible in the design artifacts.[9]
- It is often said that security testing is only a small part of secure programming [10]. In fact,  it is very difficult to find all security related problems in a software system.
Thus, no effective mitigation strategy should be overlooked.

### A. Software Security Testing Goal
- To identify the threats in the system.
- To measure the potential vulnerabilities of the system.
- To help in detecting every possible security risk in the system.
- To help developers in fixing the security problems through coding.

### B. Software Security Testing Principle
- Confidentiality
- Integrity
- Authentication
- Authorization
- Availability
- Non-repudiation

### C. Major Focus Areas in Security Testing
- Network Security
- Web Application Testing (Client-side and Server-side)
- System Security

## Test Case Designing for Security Testing:
- Test if users can directly access bookmarked web page without login.
- Test if system restrict users to download the file without log in.
- Test if previous accessed pages should not accessible after log out (i.e. Sign out and then press the Back button to access the page accessed before).
- Test if the industry standard username & password rules is enforced.
- Test if sensitive information ( passwords, ID numbers, credit card numbers, etc.) are stored as plain text. They should be encrypted and in asterix format.
- Test if bookmarking is disabled on secure pages by default.
- Test if source code is invisible to users.
- Test if older version web browsers can access the app (older version web browsers does not support SSL).
- Test if multiple attempt is being blocked.
- Test if system completely log out current user after time out.
- Test if users connection are stable and secure.
- Verify that relevant information (upload, download, activities) are written to the log files and that information should be traceable.
- Test if the SSL encryption is done correctly and verify the integrity of the information.
- Prevent same username to log in at the same time.
- Check if important credential update immediately.
- Test if error messages doesn't contain important information.

## Related Work:
### A. Types of Security Testing:
There are seven types of Security Testing:
- Vulnerability Scanning: Vulnerability scanning is performed with the help of automated software to scan a system to detect the known vulnerability patterns.
- Security Scanning: Security scanning is the identification of network and system weaknesses. Later on, it provides solutions for reducing these defects or risks. Security scanning can be carried out in both manual and automated ways.
- Penetration Testing: Penetration testing is the simulation of the attack from a malicious hacker. It includes an analysis of a particular system to examine for potential vulnerabilities from a malicious hacker that attempts to hack the system.
- Risk Assessment: In risk assessment testing security risks observed in the organization are analyzed. Risks are classified into three categories (low, medium, and high). This testing endorses controls and measures to minimize the risk.
- Security Auditing: Security auditing is an internal inspection of applications and operating systems for security defects. An audit can also be carried out via line-by-line checking of code.
- Ethical Hacking: Ethical hacking is different from malicious hacking. The purpose of ethical hacking is to expose security flaws in the organization’s system.
- Posture Assessment: It combines security scanning, ethical hacking, and risk assessments to provide an overall security posture of an organization.

### B. Penetration Testing Pre-Requirement:
- Python Scapy Package: Scapy is a powerful Python-based interactive packet manipulation program and library. It is able to forge or decode packets of a wide number of protocols, send them on the wire, capture them, store or read them using pcap files, match requests and replies, and much more. It is designed to allow fast packet prototyping by using default values that work.
- Kali Linux: is an open-source, Debian-based Linux distribution geared towards various information security tasks, such as Penetration Testing, Security Research, Computer Forensics and Reverse Engineering [11].
- Cyber Security principles: Applied Cyber Security Principle to find weakness in the system (by pass filter if using same MAC address)
- Networking Principles (MAC Address)
- OSI Model and TCP/IP Model: Understand Layers Architecture
- Web Aplication Structures (Client Server Model)
- Python Programming: String Manipulation, Parsing HTML, Sending & receiving HTTP requests, Netfilterqueue, Socket Programming, Data Structures, 

### C. Penetration Testing Methods:
- 


## Problem:

In this use case I will demonstrate how to implement man in the middle attack on a system (that we are not allowed to get access).

## Reference:
- IEEE: [Advance Technology for Humanity](https://www.ieee.org/) [1]
- ISO 9000-3: [Quality management and quality assurance standards](https://www.iso.org/standard/26364.html) [2]
- SWEBOK V3.0: [Guide to the Software Engineering Body of Knowledge](https://ieeecs-media.computer.org/media/education/swebok/swebok-v3.pdf) [3]
- [Tutorial Point: STLC Tutorial](https://www.tutorialspoint.com/stlc/index.htm) [4]
- [Software Testing | Security Testing](https://www.geeksforgeeks.org/software-testing-security-testing/?ref=lbp) [5]
- [Security Testing: Types, Tools, and Best Practices](https://www.neuralegion.com/blog/security-testing/) [6]
- [API Security: The Complete Guide](https://www.neuralegion.com/blog/api-security/) [7]
- [STLC (Software Testing Life Cycle) Phases, Entry, Exit Criteria (guru99.com)](https://www.guru99.com/software-testing-life-cycle.html) [8]
- Fink, G. & Bishop, M. "Property-Based Testing: A New Approach to Testing for Assurance." ACM SIGSOFT Software Engineering Notes 22, 4 (July 1997): 74-80.[9]
- McGraw, Gary & Potter, Bruce. "Software Security Testing." IEEE Security and Privacy 2, 5 (Sept.-Oct. 2004): 81-85. [10a]
- McGraw, Gary. "Application Security Testing Tools: Worth the Money?" Network Magazine, November 1, 2004.  (2004). [10b]
- https://www.kali.org/?msclkid=ccbd3c3faa2511ecbe541363c15a4582 [11]
- https://pypi.org/project/scapy/?msclkid=33343ba2aa2611eca8b9c3abfd8b35c1 [12]
