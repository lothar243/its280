# Roles

Hosts - any computer that connected to a network

Server - a computer that listens for a request, when it gets a request it responds

Client - a computer that initiates a request

Types of servers

* Web server
* Print server
* File server

Resources - anything that might be shared over a network

# Networking Technologies

### Network Interface Controller/Card (NIC)

* Labels the machine on the network
* Works as an interface between network communication and internal communication
* Has a built-in identifier called a media access control (MAC) address
  * 48 bits long - 12 hexadecimal characters

### Frames

* Contains to and from MAC addresses
* Contains some other data, variable size
* Contains a cyclic redundancy check (CRC)

### Ethernet

The series of standards that define how a NIC communicates

Typical speeds vary

* 10BaseT
* 100BaseT - Fast ethernet
* 1000BaseT - Gigabit

* 10GBaseT - 10 Gigabit ethernet

#### Ethernet topology

* Star - each host connects to a central box
* Mesh - each host connects to many other hosts
* Ring - connections form a cycle - not common
* Others

LAN - Local area network

* Typically within a few hundred meters
* One broadcast domain

#### Network infrastructure

Hub

* Sometimes called a repeater, because it just repeats all incoming signals to all outputs
* All traffic goes everywhere - leads to more congestion

Switch

* Attempts to only send frames where they are needed (based on MAC address)
* Traffic only goes where it's needed

Network segment

* Connection between a computer and a switch
* Limited to 100m

Bridge

* connect dissimilar network technologies that transmit the same signal

# Cables

### Twisted Pair cabling

* Shielding
  * Unshielded twisted pair (UTP)
    * Twisting the wires together cancels out most interference
    * Higher frequencies require tighter twisting
  * Shielded twisted pair (STP)
    * Only really needed in areas of excessive electronic noise



* Categories
  * Cat 5 - Designed for 100-Mbps networks
  * Cat 5e - Enhanced to handle 1000-Mbps networks
  * Cat 6 - Supports 1000-Mbps at 100-meter segments, 10-Gbps up to 55-meter segments

* Covering
  * Plenum - used in plenum spaces (like drop-down ceilings)
    * Coated with fire-resistant materials, usually teflon

  * Other - typically PVC - puts off a lot of nasty smoke when on fire

* RJ-11 Connector - used for telephone line
  * Either 2 or 4 conductors


* RJ-45 Connectors - T568A and T568B

  * Alternate stripe/solid

  * Blue and brown are in the same spots __ __ __ B BW __ Br BrW

  * The green and orange order is dependent on A (alphabetical) or B (backward)

  * GW G BW __ __ B __ __    vs    BW B GW __ __ G __ __


### Fiber Optic

* Connectors
  * ST - round with bayonet mount
  * SC - "Square connector", snap-in
  * LC - Small form factor
  * Others exist, but not needed for the A+
* Mode
  * Multimode - Multiple wavelengths of light
    * Cheaper (uses LEDs for light)
    * Slower - speeds up to 10Gbps
    * Shorter distances (up to ~600m)
  * Single-mode - relatively rare
    * Uses lasers for light source
    * Faster - speeds of 100Tbps in 2011
    * Long distances (over 100 miles)

### Coaxial

Central core surrounded by insullation

* Cables
  * RG-59 - thinner and doesn't carry data as far
  * RG-6
* Connectors
  * BNC - Bayonet Neill-Concelman or British Naval connector
    * quarter-turn twist connector
  * F-Type
    * Screw in for 5 minutes

### Ethernet over Power

Transmit signal over normal power lines

# Equipment racks

* Standardized sizes
  * Equipment heights are measured in U, 1U, 2U, 4U, etc
* Patch panels
  * A box with a row of female connectors in the front and permanent connections in the back
  * Provide a place to transition cables from solid-core to stranded core
  * Commonly a 110 block
    * connections are made in the back with a punchdown tool, which forces the wire into place and trims the excess
* Patch cables - short (typically 2-5 feet) cables used to connect devices in the rack

