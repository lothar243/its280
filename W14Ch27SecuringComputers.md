# Protecting Your Data

## Non-skilled attacks

Dumpster diving

Shoulder surfing

## Social Engineering

Often, the most insecure face of a company is its people

* Impersonation - gain entrance by use a disguise

* Tailgating - following someone else in

  Securing against tailgating:

  * Mantrap - small room with two doors. Outer door must be closed before inner will open (like an airlock)

  * Security Guard
  * Entry control roster

* Telephone scams

* Phishing - trying to get usernames/password via email, usually low effort
  * Spear phishing - more targeted (Like the frequent "Are you available?" emails posing as Tom Gallagher or Seth Bodnar)

## Denial of Service (DoS)

* Causing a service to become available

* Distributed Denial of Service (DDoS) - Many devices simultaneously attacking a single system

* Destruction of Data

* System Crash/Hardware Failure
* Physical Theft
* Malware

## Environmental Threats

* Power loss
* Dirty Air
* Temperature and Humidity

# Security Concepts and Technologies

## Access Control 

### Secure Physical Area

* Require ID Badges, with RFID tags or smart cards (RFID is easily cloned)
* Locked doors, gates, fences
* Cable Locks
* USB Locks to prevent plugging in unauthorized USB devices (Like the USB Rubber Ducky)
* RJ-45 locks or similar access control
* Server locks to limit access to ports, or locking rack doors

* MAC address Filtering - can be overcome, but adds a barrier

### Authentication

* Proper passwords
* Multifactor authentication - require something from two different categories
  * Something you have: smart card, hardware token, software token
  * Something you are: fingerprint, iris scan, facial scan
  * Something you know: PIN, password, passphrase

* Principle of least privilege - Accounts should have permissions only to resources they need and no more
* Beware of default user accounts and groups

### Security Policies

* Group policies Management - Activities that are allowed
  * Prevent Registry Edits
  * Prevent Access to the Command Prompt
  * Log On Locally
  * Many others


* Organizational Units (OUs) are used like folders to help organize users and devices, and apply group policies

### Data Classification

* Personally Identifiable Information (PII)
* Protected Health Information (PHI)

### Compliance Groups

* Payment Card Industry (PCI)
* General Data Protection Regulation (GDPR)
* California Consumer Privacy Act (CCPA) (not in the A+)

## Incident Response

### First Response

* Secure area
* Determine scope
* Explore seriousness and impact on the company

### Identify and Report

* Have Auditing Enabled - create an entry in the Security Log when certain events happen
* Use Event Viewer to read through logs (Logs are stored in %SystemRoot%\System32\Config)

### Incident Reporting

* Provide record of work
* Provide information that might help to reveal bigger patterns

### Evidence Handling and Chain of Custody

* Ignore personal information around a person's computer
* Your company should have an Acceptable Use Policy (AUP) that defines what actions an employee may or may not perform with company resources
* Report through proper channels - perhaps your incident response leader
* Secure the chain of custody - a list of who has had possession of the evidence
  * Isolate the system - shut it down and store it in a place where no one else has access
  * Document when you took control and the actions you took (like shutting it down)
  * Document the transfer of custody

# Malware

Types of Malware

* Virus - software that replicates and activates
* Worm - automatically spreads across a network - no user interaction is required usually
* Trojan - malware that appears to be one thing but does something else
* Keylogger - Keeps a log of keys pressed
* Rootkit - A virus that gains low-level access to a system, accessing the kernel memory - very difficult to extinguish
* Spyware - usually installed without your knowledge
* Ransomware - encrypt valuable files, usually asking for bitcoin to get the decryption key
* Botnet - The program will perform attacks on behalf of someone that controls it, among many other infected devices
  * Often insecure routers or IOT devices
  * The attacks can be DDoS, spam, or just acting as a node to hide traffic


Attack Vector - The route the malware takes to infect the system

Types of attacks

* On path attack (Formerly Man-in-the-Middle) - The attacker intercepts communication and has the ability to alter it before forwarding it to the destination
* Session Highjacking - Getting ahold of a valid cookie and putting it forward as your own (possibly through XSS)
* Drive-by Downloads - downloading a file without user intervention
* Popups - unwanted popups that can cause the user to click on something they didn't want to click
  * Claim to be a popup from your operating system warning that your system is infected, and you "need to download and run this software"
* Spam/Phishing - Email that attempts to get you to download something or steal your credentials

Zero-Day Vulnerabilities - vulnerabilities with no fixes, depending on who you ask, this definition may require "in the wild" exploitation

Password Guessing

* Brute force - trying all possible values
* Dictionary attack - using a list of common passwords
  * /usr/share/wordlists/rockyou.txt on Kali (you have to unzip it first)
* Rainbow tables - A list of pre-hashed passwords to save time. Most passwords are salted to prevent this

### Dealing with malware

* Anti-malware programs such as an antivirus

  * Virus signatures are usually either pattern recognition or behavior recognition

  * Polymorphic viruses alter themselves to avoid detection - often choosing random install locations, or using random strings in the program
  * This will catch most garden variety viruses - Windows defender is enough for most people's purposes in my opinion. Running multiple antivirus programs can cause performance problems

* Verify good downloads

  * Checksum (for example, a hash) - A value generated by an algorithm that will be drastically different if any bit is changed in the file

* Removal of viruses can be difficult

  * Many different forms of persistence - autorun locations, hiding among other applications
  * Viruses often come in multiple layers, even if you eliminate one part, the other part may still reinfect you

  Best practices for removal (according to the A+ 1002 exam objectives)

  1. Identify and research malware symptoms
  2. Quarantine the infected systems
  3. Disable System Restore (in Windows)
  4. Remediate the infected systems
     1. update the anti-malware software
     2. Scan and use the removal techniques, possibly using safe mode or the preinstallation environment
  5. Schedule scans and run updates
  6. Enable system restore and create a restore point (in Windows)
  7. Educate the end user

  Alternatively, restoring from a known good backup (which is the preferred method if possible)

* Secure Boot to prevent boot sector viruses
* Network firewalls, with stateful packet inspection (SPI)
  * Port forwarding causes incoming port's traffic to be directed to a specific computer within your network
  * A DMZ is a portion of the network that is exposed to the internet - typically dedicated web servers

# Internet Appliances

* Intrusion detection system (IDS) - Send an alert when specific type of traffic is detected (like an attempt at logging in)
* Intrusion prevention system (IPS) - Sits in the flow of network traffic and can stop unwanted traffic when detected
* Unified threat management (UTM) - Bundle the traditional firewall, an IPS, VPN, maybe a load balancer and antivirus all into the same appliance

# Encryption

* IPsec - includes protocols for mutual authentication and negotiation of cryptographic keys
* VPN - an encrypted tunnel for all communication, often to add a device to a remote network, or connect two networks
* Secure Socket Layer (SSL) and Transport Layer Security (TLS) - The encryption method used for HTTPS
* Digital certificates - a verification from a Certificate Authority (CA) that some is who they claim to be
  * Trusted Root CAs - CAs that are built in to your browser
  * Certificates can be revoked, but not all software recognizes revocation properly - http://revoked.grc.com
  * Expired certificate: https://expired-rsa-dv.ssl.com/
