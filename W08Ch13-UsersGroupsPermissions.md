# Fundamental Security Concept - AAA

Authentication, Authorization, and Accounting

## Authentication

Being identified as a specific person

* Typically makes use of an Identity and Access Management (IAM) tool
* Verified by one or more factors
  * Something you know
  * Something you are
  * Something you have

### Users

* Windows stores user accounts as an encrypted database of user names and passwords
  * Local user account - exists only on that computer
  * Global user account - exists on that computer and on Microsoft server
    * synchronizes some of your files between devices
* NIST guidlines for passwords: (1 minute video) https://www.nist.gov/video/password-guidance-nist-0
  * In my opinion, the biggest problems are password reuse, and easy to guess passwords
    * http://haveibeenpwned.com
      * credential stuffing - use username/password pairs against many different services
    * rockyou.txt - 14 million most common passwords
      * dictionary attack
        * Account is locked after a certain number of failed attempts
      * password spraying
* Windows password policies
  * Complexity requirements
  * Password expiration

### Groups

A collection of users so that access can be more easily controlled

Default Windows Groups:

* Administrators - any account in this group has complete administrator control
* Power Users - Almost as powerful as administrators, but can't install new devices or access other users' files
* Users - cannot edit registry or access critical system files
  * Called standard users
* Guests - previous versions of windows, used for temporary access
  * Usually disabled

### Temporarily elevate privileges

Right-click and use the "Run as administrator" option, if you have the privileges

## Authorization

Being allowed access to specific content

NTFS permissions types

* Ownership - Owners can do anything they want to the files and folders they own
* Take Ownership permission - Ability to seize control of the file/folder
  * Administrators can take ownership of any file
* Change permission - ability to give or take away permissions
* Folder permissions
  * Full control - enables you to do anything you want
  * Modify - Enables you to read, write, and delete both files and subfolders
  * Read & Execute - Enables you to see the contents of the folder and any subfolders as well as run any executable programs or associates in that folder
  * List Folder Contents
  * Read - View folder contents and ready any file in the folder
  * Write - Enables you to write to files and create new files and folders
* File permissions
  * Full control
  * Modify - read, write, and delete the file
  * Read & Execute
  * Read
  * Write - open and write to file
* Inheritance 
  * new folders permissions are inherited from their parent folder
  * Enabled by default
* Permission propagation - when copying/moving, how new permissions are assigned
  * on the same NTFS-based volume
    * copying - the copy inherits permissions from the new location
      * permissions might differ from original
    * moving
      * The permissions are unchanged
  * Between two NTFS-based volumes
    * permissions are inherited from the new location (for both copying and moving)

## Accounting

Keep track of what and when content has been accessed by whom, typically log files

* It is important to not share accounts

# Permissions in Linux and macOS

On the Linux command-line, type ls -l

drwxrwxr-x 2 mikemeyers    mi6   4096 Oct   2  18:35 agent_bios

\-rw-rw-r--  1   mikemeyers    mi6   34405 Oct 2 18:39 datafile

-rwxr--r-- 1    mikemeyers     mi6    299  Oct 2 18:31  launch.sh

The first character tells you what type of file

* d - directory
* \- normal file
* l - link

The next 9 characters come in groups of 3

* Owner
* Group
* Everyone

Within each of these groupings, the following information is conveyed (in this order)

* read - read the contents
* write - write or modify a file or folder
* execute - execute a file or list the folder contents

## chown Command

change owner (requires superuser privileges)

chown <new owner> filename

## chmod Command

change permissions

* Numeric values:

  * r: 4

  * w: 2

  * x: 1

  * chmod 754 launch    # would change the permissions of launch to rwxr-xr--

* Setting with letters

  * You can add/remove specific permissions +r, -r, +w, -w, +x, -x
    * chmod +x launch     # would give execute permission to everyone
  * You can specify who it applies to (u for owner, g for group, o for other, a for all)
    * chmod u-x launch    # would remove the owner's permission to launch

# Protecting data with encryption

Encrypting File System (EFS) - feature of Windows professional