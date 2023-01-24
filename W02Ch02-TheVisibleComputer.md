# The Computing Process

## Personal Computer (PC)

Typically runs Microsoft Windows (historically)

Stereotypical computers, wifi picture frames, modern refrigerators, and even mall lighting systems

### The computing parts

* Hardware
  * Physical stuff you can touch, the case, keyboard, etc
* Operating system (OS)
  * Controls hardware and provides some sort of user interface (UI), typically a GUI
* Applications
  * Compose a document
  * Browse the internet

### The computing process

* Input
  * Clicking the mouse or touching a touchscreen
* Processing
  * Many different transistors working together to do something with the input
* Output
  * Show something on the display
  * Play a song
* Data storage
  * Save a permanent copy of your work
* Network connection
  * Talk to another computer

### Why the Process Matters

The more you understand about the process, the better you can troubleshoot when something goes wrong

# Computing Hardware

Give a tour of a physical machine

* Rear connection panel
  * Video
  * Audio
* Motherboard
  * PCIe slots
  * Power cable
  * Heat-sink above CPU
  * RAM
* Expansion cards
* Power supply
* Hard drive bays
* CD-ROM bays

# Computing Software

### Windows 7

* Dated and unsupported, but still in use sometimes
* GUI looks quite similar to Windows 10
* Added blurred background (Aero, or Aero Glass)
* Has a start button, pinned applications on the taskbar, with a notification area (aka the system tray)
* Right click in most areas gives you a **context menu**

### Windows 8/8.1

* The interface, code-named **Metro UI** was designed for touch-enabled devices with its tiles
* Microsoft faced backlash over defaulting to touchscreen style, originally trying to get rid of the start button
* With 8.1, Microsoft brought back features such as the start button, easy access to the close icon for apps, and the ability to boot directly to the desktop.
* 8.1 looks very similar to Windows 7
* Introduced the Charms bar
  * Place cursor in top- or bottom-right corner of the screen

### Windows 10

* Improved functionality of search, though still not perfect
* Tries to modernize the Windows 7 by combining some features of Metro

### Windows In General

* Uses File explorer/Explorer to navigate directories graphically

### macOS

* Frequenty used applications can be accessed from the **Dock**, on the bottom (similar to the Windows taskbar)
* You can switch between applications by using **Mission Control**
* Allows multiple desktops with **Spaces**

### Linux

* Too many distributions (distros) to describe
* Popular distributions like Ubuntu and Mint provide all the features that are offered by Mac and Windows

## File structures and paths

### Windows

The file system acts as a bunch of trees, with each drive letter being the root of each tree.

* Directories (folders) are separated with backslashes
* Not case sensitive
* File types are indicated by their extension
* File associations specify what file extensions go with what applications
* C:\Program Files - Default directory for applications that are installed in Windows
* C:\Program Files (x86) - The location for 32-bit program files when installed in a 64-bit system
* Personal Documents
  * C:\Users\Jeffrey.Arends\Desktop
  * Documents
  * Downloads

### macOS/Linux

The file system has a global root, /

* Directories are separated with slashes (not backslashes)
* Case sensitive
* File extensions are still used to indicate file type
* User documents are typically in /home/jeffrey.arends/ for Linux, /Users/jeffrey.arends for mac

## Tech Tools

### Windows 7

* The Control panel contains many applets
* System Tools also contains many tools
* The Command-line interface (CLI) provides a lot of power if you can use it (more about this later)

### Windows 8/8.1

* The control panel
* Administrative Tools
* The command-line

### Windows 10 & 11

* The control panel
* Settings
* Administrative tools (Renamed Windows Tools in Windows 11)
* The command-line

### macOS

* System preferences (Click on the Apple icon in the top-left and select system preferences)
  * Contains almost all settings you will need
* Utilities Folder, located in the Applications folder
* Mission Control (CTRL + Up) - switch between open applications

### Linux

* Some GUIs have preferences, but the CLI is the most common and versitile
