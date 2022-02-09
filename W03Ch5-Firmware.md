# Talking to the hardware

Each keypress on a keyboard sends a series of pulses (1s and 0s) that are interpreted by the computer

## System BIOS

The basic input/output service (BIOS) is the support programming that enables the CPU to talk to devices

Hundreds of these little services are collectively called the system BIOS

## ROM

Read-only memory

Non-volatile memory that stores the system BIOS

Usually flash ROM, so that it can be updated

Typically, software stored on ROM is referred to as **firmware**

## UEFI

Unified Extensible Firmware Interface (UEFI)

Compared to a traditional system BIOS, there are several improvements

* Supports booting to larger partitions
* Native 32-bit or 64-bit
* Handles boot-loading duties
* Portable to other chip types
* Enables 'Secure Boot'

## CMOS and RTC

Complemantary metal-oxide semiconductor (CMOS) - a tiny bit of RAM powered by the internal battery that stores BIOS settings

* Incorporated into the chipset
* Many motherboards have a 'reset' feature that clears the CMOS

Real-time clock (RTC) powered by the internal battery

## System Setup

Different manufacturers setup utilities look different, but have the same basic features

* Administrator password - required to get into the system setup utility
* User Password - required when the computer boots

## Other BIOS security settings

* Chassis intrusion detect/notifiction
* LoJack
* Trusted Platform Module (TPM)
  * Stores cryptographic keys
  * Formerly a separate module, but now incorporated into the CPU
  * TPM 2.0 required for Windows 11

# Option ROM and Device Drivers

How does the CPU talk with a device that didn't even exist when the CPU was made?

## Option ROM

The device has its own BIOS

Example: Video Cards

## Device Drivers

Files stored on the PCs hard drive that contain the commands necessary to talk to a device

Basics are preloaded into operating systems and online tools, but sometimes you have to download specific drivers

# Power-On Self Test (POST)

A self-diagnostic run by the computer every time it boots

## Beep Codes

Most systems have only two beep codes

* Bad or missing video (two or three short beeps)
* Bad or missing RAM (continual beeping)

Many systems beep once or twice after the POST to indicate everything is good

Consult your motherboard manual

## Text Errors

There are generally self-explanitory

* No keyboard detected

* No operating system detected

## POST Cards

Expansion card that displays POST code - some motherboards have them built in

## The Boot Process

* Power supply sends signal down the **power good** wire to awaken the CPU

### Older systems:

* POST passes control to the bootstrap loader (find the OS and by considering the boot sequence)
  * Boot Sequence specifies the order to consider devices: USB drives, then CD-ROM, then Hard drive, for instance

* Once a bootable disk (aka system disk) is found, the bootstrap loader locates the boot sector and passes control there

### UEFI systems:

* POST hands control to the Boot manager, which loads the system boot loader directly (no scanning for boot sector)

### Preboot execution environment (PXE)

Enables the PC to boot without any local storage by retrieving an OS over a network, keeping it entirely in RAM

# Care and Feeding of BIOS/UEFI and CMOS

Be careful about changing the settings of your computer - don't tinker with a computer unless you can afford it to go down

## Return to defaults

Load default settings - sets everything back to default in the UI, or connect CLRTC pins on the motherboard (in a lab)

## Losing the CMOS RTC Settings

If your CMOS battery is dead or missing, your system clock will reset whenever you lose power

Possible errors when the battery is dead or dying

* CMOS configuration mismatch
* CMOS date/time not set
* BIOS time and settings reset
* No Boot device available
* CMOS battery state low

## Flashing the ROM

Motherboards are usually only supported for a few years, but may receive additional updates

New updates may fix bugs, or unlock new features

Typically installed via thumb-drive, but they can be risky

If it isn't broke, don't fix it
