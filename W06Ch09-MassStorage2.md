Magnetic disk drives are preset with millions (or hundreds of millions) of sectors.

* Older drives had 512-byte sectors
* Modern drives use 4096-byte sectors

Solid-state drives have 4096-byte pages

* A group of pages is a block (typically 128 pages)

Your OS uses (logical block addressing) LBA to retrieve data

* It is presented to the user as files and folders

# Partition Tables - Dividing up a drive

## Master Boot Record (MBR)

The first sector contains information about how the drive is organized

* Partition Table
  * Up to 4 primary partitions or 3 Primary partitions and an extended partition
    * Only one primary partition can be booted from (referred to as the 'active' partition)
    * One method of a multiboot setup is to use GRUB (Grand Unified Bootloader) or Partition Commander by Avanquest Software
      * During the boot process, the software prompts the user for which OS to load
      * If you want to dual boot for Windows and Linux, install Windows first, then Linux
    * Extended partitions can contain multiple logical drives (each getting a drive letter)
* Max partition size of 2.2 TB

## Dynamic Disks

* Windows calls a drive structure a 'volume'
  * Simple
  * Spanned - risky
  * Striped - risky
  * Mirrored
  * RAID 5 (not available on Windows 7-10)

## GUID Partition Table (GPT)

GUID stands for Global Unique Identifier - a reference number that is unlikely to be duplicated

* Similar to MBR, but arranged by LBA instead of sectors

* Almost unlimited partitions (MicroSoft limits this to 128)
* Max size measured in zettabytes... (big)
* The first sector is used to identify the drive as GPT (Protective MBR)
* GPT headers are duplicated - one at beginning and one at end of drive
  * Variable size - includes information about arrangement of partitions
* Windows installed on GPT requires UEFI

## Other partition types

* Hidden partitions - used by some PC makers to hide a backup install for OS
* Swap Partition - Used by Linux and Unix for virtual memory

## Tools for setting up partitions

Windows

* FDISK - Command-line
* Disk Management - Graphical
  * 'volumes' vs 'partitions' is unclear in the program

* diskpart - command-line

Linux

* fdisk - command-line
* disks in Mint, or GParted in Ubuntu

# Formatting - Organizing the partition

## File system types

* FAT32
  * Extension of FAT, FAT16, Originally used with DOS
  * Uses a File Allocation Table (FAT) to keep track of directory structure
  * Data is stored in clusters of size 4096 bytes, or larger to support larger drives
    * If a file is smaller, there is unused space
    * For larger files, multiple blocks are used, and are chained together - they don't need to be contiguous
    * Larger clusters mean less efficient storage
  * Bad blocks are marked and not used
  * Lots of non-contiguous files make the drive fragmented
    * Spinning disks might require use of the disk defragmenter
    * SSD doesn't care about fragmentation, in fact defragging an SSD could shorten its life
  * Partition size limited to 2TB, file size limited to 4GB
* NTFS - (New Technology File System)
  * Default FS for Windows
  * Offers several new features: redundancy, security, compression, encryption, disk quotas, and cluster sizing
  * Uses an enhanced file allocation table called the Master File Table (MFT)
    * Keeps a backup copy in the middle of the disk

  * Security - Enables use of an Access Control List (ACL)
  * Compression - fit more onto the hard drive, at the cost of speed
  * Encryption - Encrypt a files or folders - (Encrypting File System, EFS)
  * Disk Quotas - Limit users from monopolizing the drive
  * Supports 16TB on a dynamic disk, 2TB on a basic disk
  * Cluster Sizes vary - by changing this, you can support partitions up to 16 exabytes

* ExFAT
  * Typically used for Thumb Drives
  * Supports files up to 15 EB (exabytes), with a theoretical partition size of 64 ZB (zettabytes)
  * Lacks all the cool features of NTFS
* Apple
  * HFS+ (Hierarchical File System Plus) - Classic Apple file system
  * More commonly Apple File System (APFS)
* Linux
  * Ext4 (Fourth Extended File System)
    * Supports partitionls of 1 EB, with files of 16 TB
    * Backwards compatible with ext2 and ext3

  * ZFS
  * BTRFS (Butter FS)
* CDFS
  * Optimized for CDs
* NFS (Network File System)
  * For file sharing between different operating systems


## Formatting a disk

High-level formats initialize portions of the drive

* Defines a partition as FAT32, sets up the File Allocation Table, etc

Low-level format (or physical formatting) divides the disk into sectors and tracks. This is done before you get the drive

* Cannot be done natively from your operating system

* Not something you typically need to do