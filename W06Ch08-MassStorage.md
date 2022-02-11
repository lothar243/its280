# Mass storage - Ch 8

## Magnetic Hard Drives

* Hard Disk Drive (HDD)

* Data is stored magnetically on several spinning disks

  * Can be damaged by vibration/shock (not a good choice for laptops)

  ![harddrive](images/harddrive.webp)

* Actuator arm moves a read/write head (this is the source of the clicking noise)

Spindle Speed

* 3600, 5400, 7200 RPM
* Faster speed generally means faster read/write
  * Require more energy
  * Creates more heat

Form Factors

* 2.5-inch or 3.5-inch

## Solid-State Drives (SSD)

Uses nonvolatile flash memory such as NAND ROM

No moving parts

Form Factors

* 2.5-inch
* mSATA
* M2 drives connected over NVMe (Non-volatile memory express), connecting directly to PCIe
  * Key B, Key M, or Keys B+M support mass storage
  * Key A and Key E are used in wireless networking devices


![m2ssd](images/m2ssd.jpg)

## Comparing: Spinning vs Solid

SSDs cost more, though not as bad as it used to be

Sequential read/write

* Measured in throughput (MBps)- transferring large files. Most drives read a little faster than they write
* Typical speeds:
  * 200 MBps for HDD
  * 600 MBps for SSD attached via SATA
  * 2500 MBps or faster for NVMe attached SSD

Random Read/Write

* Measured in input/output operations per second (IOPS). Many small transfers - more representative of normal use
* Typical speeds:
  * 150 IOPS for a traditional HDD
  * Hundreds of thousands of IOPS for a NVMe SSD

Latency

* How quickly it responds to a single request, usually expressed in milliseconds (ms) or microseconds (μs)
  * Hard drives are typically under 20 ms
  * SSDs are typically under 1 ms

## The best of both worlds?

Hybrid Hard Drives (HHDs)

* Combine flash memory as a cache for speed with spinning platters for capacity
* In reality, they're not very popular

# Connecting Mass Storage


* Advanced Technology Attachment (ATA)
* Parallel ATA (PATA)

  * Large ribbon cables, sometimes referred to as IDE cables (impede airflow)
  * Can't be hot-swapped
  * Up to two drives per cable, but they must be arranged as master/slave
  * 40 wires normally, with an 80 wire variant
  * Generally not in use
* Serial ATA (SATA)

  * Fewer wires, longer maximum wire length
  * One drive per port
  * Faster than PATA - 1.5Gbps, 3Gbps, and 6Gpbs varieties
* SATA 2.5
* Magnetic hard drives (and their RPM)
* sizes (2.5, 3.5)
* hybrid drives
* flash (ch 10)
  * sd card
  * compactflash
  * micro-sd
  * mini-sd
  * xD

RAID types (ch 8)

Hot swappable(ch 8)

# Hard drive cables

SATA

SCSI

SCSI

eSATA

Molex

Windows

* disk management (ch 9)

SSD vs hybrid vs magnetic disk - Ch 23, p890

# Mass Storage Maintenance and End-of-life

S.M.A.R.T. (Self-Monitoring, Analysis, and Reporting Technology)

* An internal drive program that tracks errors and error conditions within the drive

Physical destruction

Recycling/repurposing

* Low-level vs standard format

* overwrite

* drive wipe

