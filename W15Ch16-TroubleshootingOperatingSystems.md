# Troubleshooting

## Failure to boot

### Hardware configuration

* Everything is plugged in - does the display show anything?
* No boot device
  * the BIOS is pointing to the wrong location (or a thumb drive is plugged in)
  * the drive is not connected (or nothing has been installed yet)

### Failure to Boot: Windows

* Windows Preinstallation Environment (WinPE)
  * A limited-function graphical OS that contains troubleshooting and diagnostic tools, and the installation process
  * Windows Recovery Environment (WinRE)
    * A set of tools that run within WinPE
    * Win7
      * Startup Repair
        * Repair corrupted Registry by accessing the backup copy
        * Restore critical boot files
        * Restore critical system and driver files
        * Rolls back any non-working drivers
        * Rolls back updates
        * Runs chkdsk
        * Runs a memory test to check your RAM
      * System Restore
        * Apply a restore point
      * System Image Recovery
        * Apply a system image (.wim file)
      * Windows Memory Diagnostic
      * Command Prompt
        * Many tools, like we saw in the lab
        * bootrec /fixboot # rebuild the boot sector for the active system partition
        * bootrec /fixmbr # rebuilts the mbr for the system partition
        * bootrec /scanos # looks for Windows installations not in BCD, no changes made
        * bootrec /rebuildmbr # looks for Windows installations not in BCD, gives option to add to BCD
        * bcdedit /export <filename> # exports a copy of the BCD store to a file
        * bcdedit /import <filename> # imports a copy of the BCD from a file
        * bcdedit /set {current} path \BackupWindows\system32\winload.exe # changes path of the {current} identifier to point to an alternative winload.exe
        * diskpart - set up mounting locations for volumes
          * format - create formatting information for newly created volume
          * clean - wipe all partition and volume information from currently selected disk
    * Win 8/8.1/10
      * "Refresh your pc" - Attempts an in-place reinstall without removing user files (removes all applications)
      * "Reset your PC" - Fresh install, removing all previous data
      * System Restore
      * Uninstall Updates
      * System Image Recovery
      * Startup Repair
      * Command Prompt
      * UEFI Firmware settings

* Safe Mode - Either through advanced startup options or via msconfig | Boot tab
  * Loads only very basic, non-vendor-specific drivers
  * Allows access to Device manager, where you can fix driver issues
  * ... with Networking
  * ... with Command Prompt
  * Enable boot logging - saves log info to %SystemRoot%\ntbtlog.txt
  * Last Known Good Configuration
  * Directory Services Restore Mode (Domain Controllers only)
  * others...

# Troubleshooting Tools

* Event Viewer - Many Windows logs are saved and viewable in Event Viewer
* Troubleshooting - In the control panel - offers common solutions
* System File Checker (sfc) - compares hash of file to known-good hash
* Security and Maintenance (Win 10), or the Action Center (Win 7/8/8.1) - In the Control Panel
  * Compiles information from other utilities
  * UAC settings
  * Backup and Restore
  * Windows Update
  * Troubleshooting Wizard
  * System Restore
  * Recovery

# Application Problems

* Reinstall, be sure all requirements are met
* Use compatibility mode for backward compatibility with older applications
  * Windows can pretend to be an older version
  * Reduced color mode
  * Lower resolution
  * etc
* Missing file or incorrect file version
  * DLLs are shared between multiple programs
* Many other possible problems, not covered here
