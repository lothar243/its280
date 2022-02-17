# Custom PCs

Thick client - modern operating system, all the usual components (your typical 'PC'). Requirements vary based on your need

* CPU

* Memory

* Hard drive

* Graphics

* Network

Thin client - designed to outsource most of its work, Virtual Desktop Infrastructure (VDI) access, or POS terminals

* Typically no hard drive

* Stores basic applications

* Needs a network connection

* Typically just meets minimum hardware requirements

Virtualization workstation - for running multiple OSs

* Need a large amount of RAM

* Needs a fast CPU, with many cores

Gaming PC

* Multicore processor

* Good cooling

* High-end GPU

* For the A+ (Sound card) - they aren't common anymore

Graphics/CAD/CAM Design workstation

* Multicore processor

* High end GPU

* Lots of RAM

* Robust storage

Audio/Video Editing workstation

* Specialized audio/video cards

* Large, fast storage

* Lots of RAM

* Dual monitors (or more)

Network attached storage (NAS)

* Redundant storage, and lots of it (RAID?)

* Fast Network Connection

* Decent processor if transcoding

# Installing an operating system

Clean installation - completely replacing the operating system

Upgrade installation - installing the OS on top of the existing system

Multiboot installation - Multiple operating systems, you choose which starts at boot

* If you're installing both Windows and Linux, install Windows first, then Linux

Installation methods

* Unattended installation - uses a pre-defined answer file

* Network installation - installation media can be retrieved over the network

  * Image deployment - Create a standard system image, and use that for  fresh installs. Can contain pre-configured or preinstalled applications. This would be made available typically on a Windows server.  Alternately, you can use TFTP

 * Preboot execution environment (PXE) - no thumb drive or installation media is required - enable in BIOS

 * Netboot is the MacOS solution

Windows installation keys

* allows a 30 day trial, after which you can no longer customize things like the desktop or use some tools

* Typically tied to your specific hardware (replacing a motherboard counts as installing the OS on a new system)

  * If a computer comes with an OEM copy, you often don't need to specify the key when reinstalling (it is burnt into the system)

Post-installation tasks

* Apply patches, service packs, and updates

* Update Drivers

* Restore user data files, if necessary

* Install essential software

Migration - moving old data to the new system

* Windows Easy Transfer - Migrate data and personalization settings easily

* User State Migration Tool (USMT) - must be run in an Active Directory environment, typically for migrating many users

Retiring an old system

* Data destruction - remember that data remains after the file is deleted
  * Destroy the physical device

  * Wipe the data

* Recycle
* Donate