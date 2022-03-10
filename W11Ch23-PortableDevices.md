# Portable Devices (Ch 23)

There are many different types of devices, with non-standard vocabulary. We will focus on the following for this chapter:

* Laptops

* Tablets

* Convertibles - convert into a tablet, some have removable screens

* Hybrid - Tablet that is designed to integrate with a detachable keyboard

### Input Devices

Keyboard Quirks - Often use the Function key to give more uses to fewer keys (Often hiding F1-F12)

Pointing Devices

* touchpad
  * multitouch - sensing multiple touches simultaneously, enabling gestures 
    * Three-fingered swipe to switch desktops
    * pinch to zoom
* TrackPoint - a joystick the size of a pencil eraser to move mouse cursor

Dedicated switches for some components

* Webcam
* WiFi
* Touchpad

### Display Types

Usually widescreen aspect ratio

Common Technologies

* LED
  * May perform better in brightly lit environment
  * Backlit, with liquid crystals to block light where it's not wanted

* Organic LED (OLED) - Low energy usage
  * Extremely flexible, thin and rollable
  * Each pixel has its own power and luminance
    * Deeper blacks
  * Greater viewing angles

### Extending Portable Computers

Single-function ports

* Dedicated 3.5mm audio jack
* HDMI
* Smart Card Reader (not really a port)

Storage Card slots, for SD or microSD cards

Portable-Specific Expansion slots

* Personal Computer Memory Card International Association (PCMCIA)
* PC card - obsolete
* Replaced with ExpressCard - uses USB 2.0 or PCIe

Multi-function ports

* More common
* Docking station
  * Older docks used proprietary connectins
  * Modern docks make use of USB 3.x, thunderbolt, or lightning connections
  * A single USB-C or lightning port where you can plug a dock in when necessary
* Dongles (aka port replicators)

## Managing and Maintaining Portable Computers

### Batteries

Older battery technologies: Nickel-Cadmium (Ni-Cd), Nickel-Metal Hydride (Ni-MH)

Litium-Ion (Li-Ion)

* Lightweight
* High energy density
* Lithium is explosively reactive to water (even the water that's present in the air)

Caring for your batteries

1. Store in a cool place (batteries are a chemical process, which is slowed when cool)
2. Keep the battery charged to at least 70-80 percent
3. Never drain the battery all the way down unless necessary
4. Beware of ruptured or broken batteries
5. Recycle old batteries - search for electronics recycling

### Power Management

Low-power mode

* Sleep (also called standby or suspend)
  * RAM keeps power, but general functioning is suspended
  * Restoring is very fast
* Hibernate
  * Save contents of RAM to a drive
  * Restoring takes a little while

How power management is achieved

* Advanced Power Management (APM)
  * Introduced in 1992
  * Intel and Microsoft

* Advanced Configuration and Power Interface (ACPI)
  * Introduced in 1996
  * Successor to APM
  * More companies involved

Reduce usage

* Reduce screen brightness
* Reduce network connectivity - transfer files when on AC power
* Set power-saving options to reduce performance (use more efficiency cores if you have them)

### Heat

Laptops can have problems if operated on your lap - they need to breathe

### Security

In addition to network security, a laptop/phone is much more likely to be stolen in its entirety

* Fill drive encryption with password or multifactor login
  * Wipe the drive after too many failed login attempts
  * TPM
* Cable lock
* LoJack for retrieval

## Upgrading and Repairing Laptops

There is no standardization inside laptops and phones

If available, refer to manufacturer resources

www.ifixit.com has many breakdown videos

* https://www.ifixit.com/Teardown/Samsung+Galaxy+S7+Teardown/56686

RAM

* In Laptops, RAM is usually SO-DIMM with one or two slots
* In phones, the RAM is not replacable

Mass Storage

* Older laptops may have a 2.5" form factor drive
* Newer laptops probably just have an NVME M.2 Drive

Batteries

* May require soldering, or may even be glued in place (BE CAREFUL if you try to remove!)

Video Card

* Most laptops do not have a discrete removable/replaceable video card, thus this would involve replacing the entire motherboard and/or CPU

Glue - why is it used?

* Reduce the chance of the part working its way loose (causing rattling)
* Improve waterproofing
* Makes assembly easy, but makes disassembly very difficult

WiFi antenna - usually around screen behind bezel

* Can come loose, causing intermittent/no WiFi signal

**Warning - the following portion touches on politics**

Some manufacturers are hostile to attempts to repair their hardware

* Legal implications for obtaining replacement parts
  * Claim their brand will be tarnished if non-standard parts are allowed
  * Claim it is dangerous to make replacements
* Disabling functionality if not the original part
* When you purchase a device, who owns the device?

Right-to-repair movement

* Many people want to reduce e-waste or just reduce costs
* Want to require manufacturers to allow replacement parts

Option: Framework Laptop https://frame.work/
