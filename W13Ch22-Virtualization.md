# Virtualization

A single host computer can run multiple operating systems

A virtual machine (VM) or guest runs on hypervisor software

## Benefits of Virtualization

* Power savings - fewer physical machines running
* Hardware consolidation
  * Virtual Desktop Infrastructure (VDI) allows thin clients to be used as workstations
* System management and security
  * Easier to make standardized installations
  * Physical security is easier because the servers can be smaller
  * You can take snapshots or checkpoints of the machine state
* Research
  * Learning environments (like this class)
  * Software can be developed for a system before it physically exists

## Implementing Virtualization

### Client-Side Virtualization

Requires the use of software called a Hypervisor

* Windows Hyper-V
* Virtualbox
* VMware
* Linux Kernel Virtual Machine (KVM), not to be confused with a KVM switch

The hypervisor manages the hardware interactions between the guest OS and the host OS

Virtualization is not emulation

* Emulation allows a computer to act as if the hardware is different (a desktop PC pretending to be a SNES console)

### Hardware Requirements

* Requires hardware virtualization support to be enabled in the BIOS

* RAM requirements
  * 4GB for the host OS
  * 1 GB for Windows 7
  * 512 MB for Ubuntu
  * 2.5 GB for Windows 10
* VM Storage
  * Space for VM files (which can be quite large)
  * Performance

### Networking Options

* Internal Networking - Virtual machines not present on physical network
  * Makes use of virtual switches
* Bridged Networking - Virtual machine appears as its own host on the physical network
* NAT Forwarding - Virtual machine makes use of ports on host
* No Networking

## Server-Side Virtualization

Bare-metal hypervisor (Type-1) vs application hypervisor (Type-2)

* Lower overhead
* VMware's ESX/ ESXi
* Small enough that it can be entirely located on a flash drive, allowing other storage media to be used for virtual machines

### On the Cloud

Many different ways it is done

Cloud-based services

* Infrastructure as a Service (IaaS)
  * Client is provided not much more than access to a virtual machine (like a base operating system)
  * Lot of flexibility, but you're responsible for configuring and maintaining the OS
  * Examples: Linode, Digital Ocean, Rackspace
* Platform as a Service (PaaS)
  * A framework rather than an finished product. The client can choose components to snap together
  * Client does not need to be aware of underlying OS
  * Examples: Google App Engine, Salesforce Lightning, IBM Cloud Foundry
* Software as a service (SaaS)
  * Provider does all the maintenance, minimal configuration
  * Often implemented as a web application
  * Examples: Office365, Google Suite, Slack, Dropbox

Some cloud providers span several types of service

* Microsoft Azure, Amazon AWS 

### Cloud Models

* Private Cloud - Services are hosted on servers owned by business
* Public Cloud - Services are hosted on servers from a public company (Like Amazon, Google, or Microsoft)
* Community Cloud - Servers are run by a group of organizations with similar goals or needs
* Hybrid Cloud - Connecting some combination of private, public and/or community clouds
* Consider the security implications of each of these before choosing a model

### Benefits of the Cloud

"The Cloud" is just someone else's computer - why is this desirable?

* Avoiding the large capital expenditure (capex) in favor of an operational expenditure (opex) - easier budgeting
* Rapid Elasticity - Fire up more services as they are needed, or shut them down to save money
* Measured or Metered Services - you only pay for what you use
* Cloud-based applications - Available from anywhere without installation
  * Makes the transition to/from work-at-home easier
* Cloud-based Virtual Desktops - Enables use of thin clients
