# Supporting Common Ports

## Serial Ports

* Not often used for modems, printers, mice, or networking, but they used to be

* Commonly used as a console port, for device configuration

### DB-9

* https://en.wikipedia.org/wiki/D-subminiature
* 9 Pins. Technically a DE-9, but nobody calls it that
* Part of the RS-232 standard
* D-subminiature is named for the D-shaped metal shield

## USB Ports

The core of USB is the USB host controller, an integrated circuit normally built into the chipset

* A single host controller can support 127 USB devices
* Connected to the host controller is a USB root hub, which splits to the various USB ports

* Additional hubs can be added to give more devices

### USB Standards

* USB 1.1
  * Low-speed USB, max speed of 1.5 Mbps
  * Full-speed USB, up to 12 Mbps
* USB 2.0
  * Hi-speed USB running at 480 Mbps
* USB 3.0
  * Marketed as Superspeed USB, or USB 3.1 Gen 1
  * Speeds up to 5 Gbps
* USB 3.1
  * Marketed as Superspeed USB 10 Gbps or USB 3.1 Gen 2
  * Speeds up to 10 Gbps

USB is fully backward compatible

The standard is usually indicated by the color of the connector, but not always

* USB 1.1 White
* USB 2.0 Black
* USB 3.0 Blue
* USB 3.1 Teal

### Cables and Connectors

https://usbcafe.com/what-is-the-difference-between-usb-type-a-and-usb-type-b/

Originally, there were two types of connectors, USB a and USB B

* USB A were upstream (toward the host)
* USB B were downstream (toward the USB device)

More downstream connection types were introduced

* USB Mini
* USB Micro

USB type C

* Can act as either upstream or downstream (the devices negotiate)
* Plug can be reversed

## Firewire

* Also known as IEEE 1394
* Has many of the same features as USB
* Not in common use any more

## Thunderbolt

* Taps directly into the PCI Express bus (security implications)
* Thunderbolt 1 and 2 use Mini DisplayPort (mDP) connector
* Thunderbolt 3 Uses the USB Type C connection, but marked with a thunderbolt instead of USB symbol, though not electrically compatible
* Thunderbolt 1 Runs full duplex at 10 Gbps
* Thunderbolt 2 - 20 Gbps
* Thunderbolt 3 - 40 Gpbs

# Common Peripherals

* Keyboards
* Pointing devices, like a mouse or touchpad
* Biometric devices
  * Fingerprint scanner
  * Face scanner
* Smart card readers
  * Scan a chip in a card to verify identity
* Barcode/QR scanners
* Touch Screens
* KVM Switches
* Game Controllers and Joysticks
* Digitizers
  * Wacom pen tablet
  * Signature Pad
* Multimedia devices and formats
  * Digital Cameras
  * Webcams
  * Sound Components
  * Microphones
  * Headsets

# Storage Devices

### Flash memory

* Thumb drives
* Flash cards
  * CompactFlash (CF) - oldest and largest
  * Secure Digital (SD)
    * About the size of a postage stamp
    * SD Mini
    * SD Micro - This is what I have in my phone
    * Standard SD store from 4MB to 4GB
    * SDHC store from 4GB to 32GB
    * SDXC store from 32GB to 2TB
    * There were standards for speeds, but we're not covering that in this class
  * xD - Extreme Digital
    * Formerly used in Olympus and Fujifilm digital cameras
    * You'll only see them on a CompTIA exam

### Optical Media

* CD-Media; 74min of uncompressed stereo digital audio or 650 MB of data
  * CD-ROM - read only
  * CD-R - Recordable (Write once)
  * CD-RW - rewritable
* DVD-Media; 4.37GB - 15.9 GB, 2-8 hours of video
  * DVD-ROM - Read only
  * DVD-RW
  * DVD-RW DL (Dual layer)
* Blu-Ray; 25GB - 100GB
  * BD-ROM; read-only
  * BD-R; recordable
  * BD-RE; rewritable
