# Registry

A huge database where Windows stores information for installed programs

## Access

Registry is stored in several files, called hives

* Details about hives: https://docs.microsoft.com/en-us/windows/win32/sysinfo/registry-hives

GUI access with Registry Editor (regedit)

In Powershell, cd HKLM:, cd HKCU:

In the Command Prompt,

* reg - full registry edititing tool. check out reg /?
* regsvr32 - used to register dlls

## Registry Components

Consists of Root keys, subkeys, and values

Root Keys: 

* HKEY_CLASSES_ROOT
  * Define file extension associations
  * Combination of HKCU\Software\Classes and HKLM\Software\Classes
* HKEY_CURRENT_USER and HKEY_USERS
  * Personalization settings for users
  * HKCU is just the current user, while HKU is all users
* HKEY_LOCAL_MACHINE
  * Non-user-specific configurations
* HKEY_CURRENT_CONFIG
  * Current configurations of options in HKLM

Subkeys are used for organization, like folders and can have values

Values are of defined data types

* String - Assortment of characters
* Binary - a bunch of 1s and 0s
* DWORD - 4 bytes, 32 bits
* QWORD - 8 bytes, 64 bits

## Editing the Registry

You should back up the registry before making edits

* Export either the entire registry, and entire root key, or just a subkey
* File | Export

Autorun programs

* \HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
* Also in HKCU with the same path
* Both of those, but also RunOnce (by default these values are deleted when they run)
  * RunOnce is not run when the computer starts in Safe Mode

# The Boot Process

Windows uses a file called bootmgr (boot manager)

### BIOS-based

* Boot order determines which drives get scanned, looking for an active partition
* An active partition would have information in its boot sector that points to bootmgr, a file used by Windows

### UEFI-based

* bootmgr is run directly

### bootmgr

* Reads data from Boot Configuration Data (BCD) file about operating systems and how to load them. Will run any operating system, so long as its Windows (in my experience)
* contains instructions for how to load them (bootstrap)
* Calls a program called winload.exe
  * Gets ready to load the operating system
  * Loads the hardware abstration layer
  * Load Registry
  * Load drivers for boot devices
  * Loads the operating system kernel (ntoskrnl.exe)

# Managing Processes

Process - A program that is loaded into RAM

* Are assigned a process id (PID)

Applications - Process that has a window associate with it (or is fullscreen)

Services - Process that doesn't require a window - provide background functionality

## Task Manager

CTRL+SHIFT+ESCAPE, or CTRL+ALT+DELET and select it, or taskmgr

Differs across different versions of Windows

* Windows 7
  * Applications, Processes, Services, Performance, Network, Users
* Windows 8-10
  * Processes, Performance, App history, Startup, Users, Details, Services
  * Some things moved, like startup (which used to be in msconfig)

Can force quit in context menus (right click)

## Command-line

* tasklist
  * tasklist /fi "imagename eq iexplore.exe"    # applies a filter based on 'image' (filename)
* taskkill
  * taskkill /pid 4684     # add the /f to force
* stop-process
  * Powershell
  * Has an alias of kill


## Performance Monitor (perfmon)

* Object - a system component with a set of characteristics
* Counter - tracking the information of an object
* Data Collector Sets (Groups of counters) - track data long term and make reports

## Resource Monitor (perfmon /res)

Monitor CPU, Memory, Disk, and Network Usage

I've used to to discover that slowness was caused by an antivirus scan (spiked disk usage)

# Tools for Programmers

## Component Services

Give programmers the ability to share data about objects between applications

Unless you are building Windows programs, you won't need to use this

## Data Sources

Open Database Connectivity (ODBC) - enables programmers to write databases that are OS agnostic

ODBC Data Source Administrator - Microsoft's tools to configure ODBC