# The Internet

Tiers

* Tier 1 - Long distance, high speed fiber optic connections known as backbones
  * Can reach every other network via settlement-free interconnections (settlement-free peering)
* Tier 2 - Smaller, regional networks
  * Peer for free with some networks
  * Pay for peering to reach at least some portion of the internet
* Tier 3
  * Networks who solely purchase IP transit from other networks to reach the internet

Internet Service Provider (ISP) - Lease connections from Tier 1 and Tier 2 for their customers

### DNS (More emphasis in the A+ 1101)

DNS records are identified by type

* A - IPv4 address
* AAAA - IPv6 address
* TXT - text
* MX - Mail exchanger
  * Sender Policy Framework (SPF) - Prevent spoofing by defining which IP addresses are allowed to send mail for a particular domain
  * DomainKeys Identified Mail (DKIM) - Provides encryption key and digital signature that verifies the email was not faked or altered
  * Domain-based Message Authentication, Reporting, and Conformance (DMARC) - Declare what should happen to email that fails SPF or DKIM (Usually marked as spam or bounce)

### Dial-up networking (DUN) (Not in A+ 1101)

* Modems - MOdulate/DEModulate - convert signals from digital to/from analog
  * Used to convert ethernet to something that can travel over cable or phone
  * Phone line modems had speeds based on a baud (1 cycle per second)
    * Phone line modems can have a max rate of 2400 baud, but modems pack multiple bits of data per baud. 14 bits per baud would have a speed of 33.6 Kbps
  * Dial-up networking - connecting over a phone land-line
    * Point-to-Point Protocol (PPP) - streaming protocol for dial-up internet
    * Point-to-Point Protocol over Ethernet (PPPoE) - Encapsulate PPP frames inside ethernet. Not to be confused with PoE.

### ISDN (Not in A+ 1101)

Integrated Services Digital Network

* Must be close enough to the central office
* Runs over the pre-existing copper phone lines
* Two channels: Bearer (B) and Delta (D)
  * Bearer carried voice and data at 64 Kbps
  * Delta carried configuration at 16 Kbps
* Much faster to form initial connection than traditional modem over analog

### Optical network terminal (ONT)/Fiber

Convert Fiber to Ethernet

* Consumer speeds up to 5Gbps
* Symmetrical speeds
* More limited availability

### DSL

Digital Subscriber Line

* Must be close enough to the central office
* Connect to ISP over standard telephone line
* Always-on internet
* DSL filter must be placed before phones  to get rid of high pitched screech, but there's no need for an additional line
* Typically asymmetric (faster download speeds than upload) called ADSL

### Cable

* Uses RG-6 or RG-59 coaxial cable

### Cellular

* 2G and 3G
  * Global System for Mobile Communications (GSM) or Code division Multiple Access (CDMA) networks
    * GSM evolved into GPRS and EDGE
    * CDMA introduced EV-DO
  * Fragmented technologies made switching carriers difficult
* 4G LTE (Long Term Evolution)
  * An open interoperable standard used by virtually all carriers
* 5G
  * Relies on cell towers that are closer together (shorter distance than 4G)
* Mobile hotspot - turn your device into a WAP to share your cellular connection
* Tethering - Sharing the cellular connection over a wire, such as over USB

### Satellite

* Satellite latency - usually unnoticeable for Internet browsing, but not good for gaming or voice
* More availability with options like Starlink

## Network Address Translation (NAT)

Routing traffic all to the same IP address to the correct device

1. When a device requests a website from the internet, this goes to the default gateway (your router)
2. The router, which has an external IP address sends this request from high numbered port
3. The webpage is sent back to that same port
4. The router remembers the internal IP of the device that sent the request, and forwards it on

## Internet Applications

HTTP/HTTPS - HyperText Transfer protocol

* Primarily uses GET or POST requests to retrieve web pages
  * Error codes
    * 100-199 Informational responses
    * 200-299 Success
      * 200 OK
    * 300-399 Redirection
    * 400-499 Client error
      * 404 File not found
      * 418 I'm a teapot - actually in the standard (introduced on April 1 1998, 2014)
        * google.com/teapot
    * 500-599 Server error

SMTP/POP3/IMAP - Email

* SMTP is used for sending email between mail servers
* POP3 and IMAP are used to retrieve email from your mail server
* Encryption
  * Not encrypted by default
  * Pretty Good Privacy (PGP) or Gnu Privacy Guard (GPG)
  * Secure/Multipurpose Internet Mail Extensions (S/MIME)


File Transfer Protocol - FTP

Telnet - Remote shell, unencrypted login

SSH - Secure Shell

SFTP - Transferring files over ssh

Voice over IP (VoIP)

* VoIP phones

Remote Desktop Protocol (RDP) - Graphical control over remote computer

## Virtual Private Networks (VPNs)

Form an encrypted network connection between hosts over which other traffic can be tunneled

* Connect to your office from your home, allow access to local resources
* VPN service - (Like NordVPN, etc) - your ISP can't see the specific traffic, but the VPN provider can

## Internet Utility Protocols

Lightweight Directory Access Protocol (LDAP) - Transmit directory information (what an who are on the network)

Simple Network Management Protocol (SNMP) - Remote query and config of network appliances

Server Message Block (SMB) - Window's network file and print sharing protocol

Apple Filing Protocol (AFP)  - Apple's network file and print sharing

Network File System (NFS) - Unix and Linux network file sharing

Service Location Protocol (SLP) - Advertises available services

## The Internet of Things (IoT)

Digital assistants - Alexa, Siri, Bixby, Ok Google

* Voice-based interface

Home Automation

* Thermostats
* Lights

Protocols

* Z-Wave
  * Proprietary (devices must be certified)
  * More expensive
  * Devices tend to work together better
* Zigbee
  * Open
  * Less expensive
  * Each company tends to require their own gateway (or hub)

# Internet Troubleshooting

No Connectivity

* Disconnected NIC or inability to connect to a resource
* Can you ping out? ping google.com
* Check DNS, maybe flush current DNS with ipconfig /flushdns
  * Google's DNS server is at 8.8.8.8 and 8.8.4.4, Cloudflare is at 1.1.1.1 and 1.0.0.1

Limited connectivity

* Check ipconfig - if your address is in the 169.254 range, then you probably don't have a DHCP server

Local Connectivity

* Can you ping your default gateway?
* Do other devices on the network have connectivity?

Slow Transfer Speeds

* netstat shows current connections
  * Is QoS limiting your download speed?

