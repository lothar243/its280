# Local Area Networking

TCP/IP - Transmission Control Protocol/Internet Protocol

* The primary protocol of most modern networks, including the internet

## IPv4

* IP address - Four 8-bit numbers (between 0 and 255), separated by decimals
* Made up of Two parts - Network ID and Host ID
  * Network ID can be read by applying a subnet mask
    * Subnet mask
      * 255.255.255.0
      * Alternatively, Classless Inter-Domain Routing (CIDR) notation is used to denote the number of bits used for the network ID, /24
    * Classes - not used any more, but still referenced
      * Class C - 255.255.255.0, or /24 
        * By far the most common of classes
        * Could have up to 2^8 - 2 = 254 hosts
      * Class B - 255.255.0.0, or /16
        * Could have up to 2^16 - 2 = 65534 hosts
      * Class A - technically 255.0.0.0 or /8
        * Could have up to 2^24 - 2 hosts
  * Host ID
    * all 0s may be reserved
    * all 1s means broadcast to hosts in subnet

## Interconnecting networks

* PAN - Personal Area Network - IE devices on your person
* LAN - Usually withing a couple-hundred meters
* MAN - Metropolitan area network - citywide network
* WAN - Wide area network - usually Hundreds of kilometers
* SAN - Storage area network - high-speed network that provides block-level access to storage

Routers - redirect traffic based on IP address, they generally have a 'LAN' side and a 'WAN' side

* LAN side - traffic within the defined subnet
* WAN side - the 'default gateway', or where any traffic outside of your LAN is sent

## Domain Name Service (DNS)

Serves IP address of easy-to-remember names like google.com

* When you type in google.com, a DNS server is first queried to find out what is the IP address of google.com

Top-level domains (.com, .org, .mil, .edu, etc)

## Obtaining an IP

In order to get an IP address, you need the following

* IP address
* Subnet mask
* Default gateway
* DNS server

### DHCP

Dynamic Host Control Protocol (DHCP) is an automatic way of configuring this information

* The DHCP server sends the information

Configuring this information manually is one way to get a static IP address

### Automatic configuration without DHCP

Windows has a feature called Automatic Prived IP Addressing (APIPA), other operating systems call this feature zeroconf

* Automatically assigns a random IP address in the 169.254/16 range

This process is completed by your home router as well, getting information from your Internet Service Provider (ISP)

TCP vs UDP

* TCP is a connection-oriented protocol, where communication goes between both hosts
  * Packets are verified and resent if there are problems
  * Used when information loss is bad
  * Examples
    * HTTP - hypertext transfer protocol (sending web pages)
    * SSH - secure shell (logging on to a computer remotely)
    * many others
* UDP is a connectionless protocol
  * A best-effort attempt is made to send the information, but it may be lost
  * "Fire and forget"
  * Used when time is "of the essence"
  * Examples
    * VOIP - Voice over IP
    * RTSP - Real-time streaming protocol

## Networking Tools

* ping - determine if there is a route to/from a particular address
* ipconfig (Windows)/ifconfig (Linux)
  * ipconfig /release - give up current IP address
  * ipconfig /renew - get a new IP address from the DHCP server
* nslookup (Both Windows and Linux)- learn information about address from DNS server
  * can open a new prompt - type exit when done
* tracert (Windows)/traceroute (Linux) - determine path from your host to another address
  * uses a sequence of pings, changing the number of hops that they're willing to go
  * Routes may vary while running traceroute

## Configuring TCP/IP - Windows GUI

Control Panel -> Network and Sharing -> Change Adapter Settings 

Select your interface -> Properties -> Internet Protocol Version 4 (TCP/IPv4) and click Properties

Now you can change your IPv4 settings, either using DHCP (configure automatically) or manually specifying the IP address

## IPv6

32-bit IPv4 addresses can only address 2^32 or approximately 4 billion addresses

* Many of these addresses are reserved
  * Inefficient use of the addresses: 
    * 127/8 - 2^24 addresses for loopback?
    * Some companies have very large IP blocks
  * Multiple possible local networks
    * 10.0.0.0
    * 172.16.0.0
    * 192.168.0.0
* The address space is exhausted

IPv6 addresses are a much larger address space

* 128 bits, so 2^128 possible addresses (around the magnitude of the number of grains of sand on earth)
* Fewer reserved addresses
  * no private IP should be necessary
* Format of address
  * 8 words, each separated with colons
  * The largest group of all zeros can be omitted, and denoted ::
  * 2001:0:34f1:8072:303d:16ce:f5fe:8a81
  * fe80::18ed:901d:70db:a01c
  * ::1 - loopback
* Link-local address
  * Similar to APIPA
  * Starts with fe80:0000:0000:0000
  * The remaining bits identify the interface

### IPv6 Address Breakdown

The first 64 bits are used for the prefix

* The five Regional Internet Registries (RIR) pass out /48 prefixes (Generally to big ISPs)
* The remaining 16 bits of the prefix are used by the ISP for subnetting

The remaining 64 bits are used for end users

# Wired Network Concepts

Full-duplex mode

* Able to send and receive data simultaneously
* All modern NICs will use this

Half-duplex mode

* Cannot send and receive at the same time
* Usually caused by using the same medium for sending and receiving

Link Lights

* Off means no connection
* Flickering or blinking indicates problem

Activity Light

* On when network traffic is detected (so it flickers)
* There is no standard on colors, but colors usually indicate link speed

Wake-on-LAN

* If enabled, you can turn the computer on over the network
* Requires a special pattern or a 'magic packet'

QoS

* Allows busy networks to prioritize traffic
  * Give priority to VOIP to reduce jitter
  * Slow down bittorrent downloads

Switches

* Unmanaged
  * Automatic device with no configuration
* Managed
  * Has the ability to be configured (usually through a web interface)

Power over Ethernet (PoE)

* Ability to power your device and send data over the same ethernet cable
* The device must be capable of accepting the power, and it must be injected either by a standalone device or by the switch itself
* Handy for devices like security cameras

### Network Shares

* Resources that are made available over the network (Folders or printers, for example)
* In Windows, there are multiple levels of permissions, network permissions and NTFS permissions
  * Network (share) permissions and NTFS permissions are separate
  * You can give everyone 'full control' via network settings, and use NTFS for more precise control

## Workgroups

* You must have the same Workgroup name on the network in order to share resources
  * Default: WORKGROUP
* All hosts in the workgroup are equals
* Works well for small networks (<30 computers)
* Each computer manages their own user accounts (potentially different passwords for the same username)

## Domains

* A computer running Windows Server is configured as a domain controller
  * Stores domain accounts - allows users to use the same credentials across the network
* Activie Directory - A Windows Server in the domain that keeps track of directory information
  * Printer information
  * Computer Names
  * Location information, etc

* Domain Administrator - an account that can configure the domain controller, and anything under it
* Roaming profiles
  * Information that is transferred onto a computer when the user logs in
* Organizational Units (OUs)
  * A method to organize users and computers by function, location, permission, etc

## Homegroups

Middle ground - Workgroups provide almost no security, and domains require too much configuration for the average user

* Introduced in Windows 7
* Share libraries with a password