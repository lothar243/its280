# Maintenance

## Patch Management

### Windows

* Windows releases patches every month - patch Tuesday, several other companies have started imitating this
* It is not always wise to apply patches immediately
  * Functionality may be broken - test and weigh your options
* Windows 7&8 patches are divided into three types: Important, Recommended, and Optional
  * Many patches would be lumped into "Service packs"

* Windows 10/11 - individual users can delay updates for up to 35 days, but can't hide or skip them
  * Quality updates - standard patches, cumulative by default
  * Feature updates - whole new versions of Windows
    * https://docs.microsoft.com/en-us/windows/release-health/release-information
    * Start > Settings > System > About
    * Released twice per year
    * https://learn.microsoft.com/en-us/windows/release-health/release-information
    * Examples names: 1903, 1909, 2004, 20H2, 21H1, 21H2, 22H1, 22H2


### macOS and Linux

App Store - macOS 10

package managers - Linux (sudo apt update && sudo apt upgrade)

## Disc Maintenance

Right click drive > Properties

* Disk Cleanup - Temporary Files
* Disc Defrag/Optimize SSD
* Error Checking - chkdsk
* WinDirStat (3rd party, not on A+)

## Windows Registry

* No real maintenance required, despite the presence of third-party registry cleaners

## Scheduling Maintenance

* Task Scheduler - Windows
* launchd - macOS
* cron - Linux

## Autostarting Software

* Windows 7 had startup utilities set in the msconfig utility
* Windows 8 and 10 has startup utilities in the Task Manager

## Windows Tools

### System Configuration

* General - Startup selection type
* Boot - Advanced boot features
  * Which versions of Windows you have installed
  * Safe mode
  * No GUI boot, etc
* Services - Similar to services tab in task manager
* Startup - not used in Windows 8/10
* Tools - Links to many system tools

### Task Manager (CTRL+SHIFT+ESCAPE), click more details

* Processes - both foreground and background
* Performance - CPU, Memory, and Disk usage
* App history
* Startup
* Users
* Details
* Services

### System Information (msinfo32)

* View information about hardware resources, components, and the software environment

### Microsoft Management Console (MMC)

Starts out blank and you add snap-ins

* Event Viewer
* Disk Management
* Task Scheduler
* Device Manager
* Certificate Manager
* Local Users and Groups
* Performance Monitor
* Group Policy Editor

### Performance Options

Right-click "My Computer" or "This PC" | Properties | Advanced system settings | Advanced tab | Performance - Settings Button

* Set Visual Effects
* Set Virtual Memory Size

# Backups

### Backup and Restore

* Windows 7
* In the Control Panel

### File History

* Windows 8/8.1/10

* Requires a second drive
* Not enabled by default
* Can be used to backup your Libraries, Desktop, Contacts, and Favorites (or other files)

### Time Machine

* macOS
* backups are called "local snapshots"

### System Protection / System Restore

* Windows
* Create restore points for the operating system
* Can be used to restore previous configuration (only settings and programs are changed)
* Volume Shadow Copy Service (VSS) allows recovery of old versions of files, provided a system restore point is created
