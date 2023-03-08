# Command-line Interface (CLI)

## Shells

* Linux/Unix Terminal
  * Shell (sh)
  * Bourne-Again SHell (bash)
  * fish
  * zsh
* Windows Command Prompt (cmd)
  * Successor of the DOS Prompt
* Windows Powershell (powershell)
  * Microsoft's response to the utility of Bash

## Prompt

* A statement that the computer is ready for your next instruction
* Generally some useful information
  * Working directory
  * Current user
  * Computer name

## Syntax and Switches

Commands executed in a command-line interface are very sensitive to syntax

* mv this that
* mv that this
* Switches, or options are the way we specify arguments with many utilities
  * dir /?           show help for dir (in Windows)
  * ls -a            show hidden and non-hidden files (in Linux)
  * In Linux, switches can often be ls -alh (show all files, show additional details, and make the size human-readable)

## Linux basics

* Root directory is /
* Paths use slashes between filenames
  * /etc/fstab
  * /home/jeff/Desktop
* Typical user's directory are located at /home/<username>/, represented by ~
* Linux file structure: https://www.linux.com/training-tutorials/linux-file-structure/
* Display current path with: pwd
* Case sensitive

## Command Prompt and Powershell basics

* Letter drives are top level. The typical first hard drive is C:\
* Paths use backslashes between filenames
  * C:\Windows\System32\notepad.exe
  * C:\Users\Jeffrey.Arends\Desktop\testfile.txt
* Typical user's directories are located at C:\Users\\<username>\\, represented by %
  * %SYSTEMDRIVE% - C:\\
  * %SystemRoot% - C:\\Windows\\
  * %USERPROFILE% - C:\\Users\\{username}
  * %APPDATA% - C:\\Users\\{username}\\AppData\\Roaming
* Windows system files in C:\Windows
* On a 64-bit system
  * 64-bit program files are in C:\Program Files\
  * 32-bit programs files are in C:\Program Files(x86)\
* Not case sensitive
* Powershell "commmandlets" are of the form verb-noun, such as Get-ChildItem

## CLI General Tips

Piping - Take the output of one command and give it to another command as input (works on Bash and Powershell)

* ls /usr/bin | less
 
Redirection - Take the output of one command and write it to a new file (or append to a file)
 
 * ls > myfile # Write output to a new file
 * ls >> myfile # Append output to existing file (or create new one if none exists)
 * cat < myfile # Read file contents as standard input to the command
 * grep .txt < myfile > filteredfiles # Both reading and writing

Tab completion - both Windows and Linux, pressing tab will cause the shell to attempt to predict and complete the command

Press the Up/down arrows to pull up previous commands, move cursor with left/right

The current directory is represented by .
 
 * cp Downloads\myfile.txt .

The parent of your current directory is ..		
 
 * cd ..

## Commands

### Linux - basic

List files and subfolders: ls

Change Directory: cd

Make directory: mkdir

Remove directory: rmdir

Running programs:

* Typical utilities - just type in the name of the utility

* Everything else - ./<program name>

Remove files:

* rm myfile.txt
* rm *.txt
* rm -r dirWithStuff

Copy

- Files - cp notes.txt ~/Documents

* Directories - cp -r Documents Documents_Backup

Move Files/Directories - mv myfile.txt ~/Documents

Rename Files/Directories - mv mv notes.txt oldnotes.txt

Help

* Manual - man ls
* Common help switch - ls -h, or ls --help

Switches/Options often come in short and long varieties

* Long versions usually have two dashes
  * ls -l --all --human-readable
* Shortened versions usually have one dash and can frequently be combined
  * ls -lah

Elevate privileges - su/sudo
 
![sudo make me a sandwich](https://imgs.xkcd.com/comics/sandwich.png)

### Windows

List files and subfolders - dir

Change Directory - cd

Moving between drives letters - d: or c:

* If a partition is mounted as a folder, just cd to it

Making directories - md

Removing directories - rd

Running programs

* For most programs, just use the filename, mmc

* Powershell - also uses dot slash notation to run scripts

Deleting files - del reportdraft1.docx

Move - move

Copy

* copy notes.txt e:      (works only on one directory at a time)
* xcopy                        (can be used with /s switch to recursively copy directories)
* robocopy                  (robust file copy, more options)

Rename - rename

Help

* Old-style cmd - help dir
* Individual programs - dir /?
* Powershell specific - get-help get-childitem

Elevate privileges - look for "Administrator" in the title bar

* When opening, right click and "Run as administrator"
* If using the run dialog, hold ctrl and shift when pressing 'OK'

### Additional Windows Commands

chkdsk - scans, detects, and repairs file system issues and errors

* /f to fix file system-related errors
* /r to attempt to locate and repair bad sectors

format - format volumes

hostname - display the name of the computer

gpupdate - Fetch the latest group policies, such as password complexity, logon attempts, and permissions

gpresult - Gives an overview of security policies

sfc - (System File Checker) scans, detects, and restores important Windows system files

shutdown - shutdown local or remote computer

net

* view - see connected resources
* share - manage shared network resources
* use - use shared resources
* users - view users
* user - manage user accounts
  * net user bob * /add (if you type in asterisk it will prompt you for password)
* localgroup - manage local groups
  * net localgroup administrators bob /delete

### Additional Linux Commands

ifconfig - Show information about or configure network interfaces

* Deprecated, but on the A+ - use ip command instead

iwconfig - similar to ifconfig but specific to wireless devices

cat - output contents of file

grep - filter text

* ls /bin | grep zip - would show all binaries in /bin that have filenames that contain the 'zip'
* cat myfile.txt | grep -i school - would show all the lines of myfile.txt that contain 'school', regardless of capitaization

ps - show processes

* Typically we would use the aux options to show all processes, regardless of the user or the mode it's run in

apt-get/apt - used to install packages

* install/remove

nano - editor (use this one)

vi/vim - editor (not as user friendly)

* insert mode
* command mode

dd - disk duplicator (or is it destroyer?), bytewise copy of file/device

* dd if=/dev/sda of=mydrive.iso
  * This would copy everything exactly - the partition table, file system, unwritten space
  * Copying a 1TB drive create a 1TB file, regardless of how much is actually stored
* dd if=/dev/urandom of=/dev/sdb - write random bits to a drive (wipe it)

shutdown <options> <time> - shut down the system

* shutdown -r now - reboot now

passwd - change password

# Pros/Cons of the Command-Line Interface (vs GUI)

### Disadvantages 

* Takes longer to learn/more difficult to get started
* Not as user-friendly

### Advantages

Doesn't change as often

* GUI changes happen constantly - keeping track of multiple versions of Windows/Linux is a losing battle
* wmic will be disabled by default soon, but changes are very slow
* GUI tends to be less stable for me (more crashing)

Can easily be run remotely - remotely administer computers (even while they're in use)

* Powershell makes administering a command to many computer simultaneously possible

More customizable

Bash and Powershell are Modular

* You don't have to rely on the GUI being created specifically for the thing you want
* Pipe output between utilities to do just what you want

It is scriptable

* Allows consistency between multiple devices/employees/times
* Enables automation

## Scripting

Text files can be interpreted to string together commands, which are run in succession

* Bash script (.sh)

* Batch file (.bat)

* Powershell script (.ps1)
* Others
  * Python (.py)
  * JavaScript (.js)
  * Visual Basic (.vbs)

Data types

* String
* Integer

Variables

* Giving a name to some data, target_ip="10.10.123.52"

Execution sequence - generally, the first line, then second, and so on

* Conditional - only execute these commands if something is true
* Loops - execute these commands repeatedly

Comments - These are not interpreted by the computer, they're there for readability typically

## Environment Variables

### Windows

Path Variable - When you try to run a program that isn't in your current directory, the computer will search through the directories in your path variable

* For example, if you install Python, you can run it from anywhere if you check the little "add to environment variables" checkbox, otherwise you have to be in the directory

You can use the %<Variable>% notation to tell Windows to use these variables

* If you ever see %TEMP%, this may be replaced with C:\Users\Jeff\AppData\Local\Temp - this is defined by an environment variable
* cd %APPDATA%

To view/edit

* Control Panel -> System -> Advanced System Settings -> Environment Variables
* If you show the control panel by categories, you have to select "System and Security" before System
* path, or echo %TEMP% to see them

### Linux

Path variable - similar to Windows

You can use $<Variable> to use these variables

* echo PATH

Other environment variables

* env

