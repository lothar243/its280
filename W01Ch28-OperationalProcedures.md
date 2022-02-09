# Documentation Best Practices

## Network Documentation

Provides a roadmap for current and future techs that need to make changes or repairs over time.

### A Network Topology Diagram

includes switches, routers, WAPs, servers, and workstations

### Knowledge base/Company Articles

Documents that specify which equipment is used, and any relevant links to manufacturer sites and information

### Incident Documentation

Helps track specific problems. For example, this printer keeps jamming when this paper is used

## Company Policies

### Regulatory Compliance

Generally government regulations that specify things to maintain a healthy workforce

OSHA, FERPA, PCI-DSS

### Acceptable Use Policy (AUP)

A document that specifies what an employee can and cannot do with company property

### Password Policy

How long and complex passwords should be

Password storage

Password change frequency

## Inventory Management

### Barcodes

Read only

### Asset tags

RFID - passively powered, can be read from a short distance

# Change Management

The process that enables organizations to implement changes to IT infrastructure in a safe and cost-effective manner.

Best Practices

* Consult documented business processes

* Determine the purpose of the change
  * Why should we update to Windows 11?

* Analyze the scope of the change
  * Number of people involved
  * How long the change will take
  * Cost of the change
* Analyze risk involved in making (or not making) the change
  * Will the most recent Windows patch break the ability to print? What is the risk in not applying the update?
* Plan for the change
  * What needs to be done first?
  * Where will the old equipment go?
  * During what time period will this change take place?
* Educate end users about the need, benefit, and cost of the change
  * Multi-factor authentication just became required? Why?

* Have a dedicated team to manage the change
  * Change board - a group of techs and representatives that review the documentation and approve or deny the change

* Have a backout plan in case the change creates negative consequences
  * Swap back to original hard drive in case the Windows 11 install doesn't take
  * Keep the old equipment in the original configuration for a month
* Document everything thoroughly
  * The previous steps
  * Receipts
  * Overtiem records
  * Inventory of changed systems

# Disaster Prevention and Recovery

## Power Protection

* Uninterruptible power supply (UPS), or battery backup

## Backup and Recovery Procedures

* Lots of copies keep data safe. It also costs more and increases the odds of data leak
* Diversify backups to reduce the risk of any one thing causing failure
* Storing backups off-site
* Automatic backups

The 3-2-1 rule. At least 3 copies on at least 2 different types of media, with at least one offline

### File-level backups

A simple way to keep files, copy the user files

All major operating systems have automated options (File History in Windows, Time Machine in macOS, the Backup Tool in Linux Mint)

### Critical Applications

* License Keys
* How to reinstall
* Any essential installation options
* Account information or credentials

### Image-level backup

Backing up the complete volume - including the OS, boot files all installed applications and all the data

* Images are big, but restoring from an image can be fast

### Cloud Storage vs Local Storage

* Cloud storage is convenient, but may be size-limited
* Local storage is potentially safer from compromise, but will be destroyed by some disasters

### Backup Testing

Verifying a backup - it's no good if you can't restore from it

* Not easy to verify, but worth the time

In Spring 2021, during the Colonial Pipeline hack, they had backups but it was taking too long to restore, so they paid the ransom anyway

## Account Recovery

A common helpdesk task - resetting passwords. Be sure to verify identity

The operating system may have tools, like Windows "Create a password reset disk"
