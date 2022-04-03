# Printers and Multifunction Devices

## Printer Technologies

### Impact Printers

Printers that create an image on paper by physically striking an ink ribbon - not common any more

Dot-matrix printers

* Can be used for multipart forms with carbon copies
* May still be used in Point-Of-Sale POS terminals
* Use a grid of tiny pins (printwires) to strike the inked ribbon
* The case that holds the printwires is called a printhead

### Inkjet printers

* Ink is ejected through tiny tubes, either with heat or a mechanical method
  * Heat: tiny resistors boil the ink that ejects the droplet
* Ink is stored in ink cartridges
  * Ink colors are commonly cyan, magenta, yellow and black (CMYK)
* Commonly, printers are sold for a loss with charging extra for ink
* Print resolution rates the number of dots per inch (dpi)
* Print speed is measured in pages per minute (ppm)

### Dye-Sublimation Printers

Sublimation is the process of causing something to change from solid directly to vapor (then back in this case)

* Sometimes called thermal dye transfer
* Better detail/color, but more expensive
* Uses heat-sensitive plastic film embedded with page-sized sections of CMYK
* Requires one pass per color
* Not constructed of pixels, so can create 'continuous-tone' images

### Thermal Printers

Two types of thermal printers: Direct thermal and thermal wax transfer

#### Direct Thermal

* Burns does into heat-sensitive thermal paper
* Common for POS terminals (no ink!)

#### Thermal Wax Transfer

* Similar to dye-sublimation, but with colored wax
* Don't require special paper

### Laser Printers

https://www.youtube.com/watch?v=WB0HnXcW8qQ

* Toner cartridge holds a the powder that is used to create images
  * Also often contain parts the parts that tend to wear out or break
* Imaging Drum
  * A photosensitive drum
  * Starts out electrically charged, but when exposed to light that charge drains away
* Erase Lamp
  * Exposes the imaging drum to light, causing the charge to drain away
* Primary Corona/Charge Roller
  * Creates a uniform voltage on imaging drum of between 600 to 1000 volts (negative)
* Laser
  * Exposes the imaging drum to light in a controlled fashion, effectively 'writing' the design to that drum
* Toner
  * Fine powder made up of plastic particles bonded to pigment particles
  * Initially charged to between 200 and 500 volts (negative)
    * Toner will only stick to the imaging drum where it has no charge
* Transfer Corona/Transfer Roller
  * Give a positive charge to the paper, drawing the negatively charged toner to the paper
  * Afterward, a static charge eliminator removes the charge from the paper to prevent it from being attracted to the imaging drum
* Fuser Assembly
  * Usually separate from the toner cartridge
  * Applies heat and pressure to melt the toner onto the paper, which was previously just resting on the paper
* Power Supply
  * Supplies the extremely high voltages necessary
* Additional parts
  * Pickup Roller - grabs the paper
  * Separation pad - uses friction to separate a single sheet from the others
  * Duplexing assembly - reverses the paper for printing on the other side
  * Gearboxes - replaceable parts. Most printers have 2 or 3
  * Ozone filter - remove ozone (O3) created by high voltages
  * Sensors and switches
* System board
  * Main processor
  * ROM - contains firmware that may be able to be upgraded
  * RAM - may be upgradeable
    * Not enough RAM can cause an overflow
  * Possibly multiple actual boards

### 3D Printers

Material

* Usually plastic filament on spools, melting with a head

* Liquid resin that is hardened with a laser
* Powdered metal welded in layers
* Requires specialized software to print

### Virtual Printers

* Print to PDF
* Print to XPS - (XML Paper Specification) - Essentially a Microsoft specific version of PDF
* Print to Image - create BMP, GIF, etc file
* Clout and Remote Printing - printer is accessed via the cloud

### Printer Languages

* American Standard Code for Information Interchange (ASCII) - text-based
* PostScript - Adobe specification - most of the processing is done on the printer
* HP Printer Command Language (PCL) - more advanced than ASCII but still character-based
* Windows GDI and XPS
  * Graphical device interface (GDI) - processing is done by CPU (rather than printer) - raster image
  * XPSj

## Scanners

* Create a digital copy of photos, documents, drawings, etc
  * For example, place a piece of paper on a large flatbed scanner, and a sensor will move across capturing the image

* Technology Without An Interesting Name (TWAIN) - traditional scanner driver
* Manufacturers cite two sets of numbers for quality
  * Optical resolution - the resolution it achieves mechanically
  * Enhanced resolution - a resolution achieved with assistance of software
* Color depth - number of bits of information the scanner uses to describe an individual pixel
  * Also, there is grayscale depth

## Multifunction Devices

A multifunction device (MFD)

* Typically Printer/scanner/copy/fax

* Uses an automatic document feeder (ADF) to grab pages
* Connection
  * Network printer - connected via WiFi or Ethernet, runs a print server
  * USB Connection - printer can still be shared over the network, configure in Windows



# Laser Printing Process

1. Processing
   * Job is sent to print spooler in Windows, allowing job queueing
   * Job is sent from print spooler to printer
     * Raster Image Processor (RIP) converts raster image to pattern for laser
   * Resolution Enhancement Technology (RET) - Insert smaller dots among characters to smooth out appearance
2. Charging
   * The primary corona wire or primary charge wire distribute a uniform negative charge to the imaging drum
3. Exposing
   * A laser is used to create a positive image on the surface of the drum
4. Developing
   * Toner is attracted to drum with relatively positive charge
5. Transferring
   * Toner moves from imaging drum to paper, but just resting in place
6. Fusing
   * Two rollers - a heated roller coated in a nonstick material and a pressure roller melt the toner to the page
7. Cleaning
   * Erase lamps remove remaining charge from imaging drum and a cleaning blade scrapes toner from the drum

# Troubleshooting Printers

### Print job never prints

* Is the printer on, connected, and online?
* Is there an error in the display?
  * Memory full/low memory error
* Does it have paper?
* Is the computer online?
* Can you print directly to the printer? (Skip the spooler)

* Does the printer have a local webpage interface?

### Print job is a strange size

* User mistake?
* Page setup
* Printer driver

### Misaligned or Garbage Prints

CompTIA calls this 'garbled characters'

* Often caused by corrupted or incorrect driver
* Try a reboot of the printer first
* Data cable or power issue?

### Prints in wrong color

* 'Rich black' have other colors mixed in
* Run diagnostic / test
* Calibrate colors
* Maybe the monitor is wrong instead?
* Cartridges are installed incorrectly, or out of one color

### Crashes on Power-up

Since both laser printers and computers require more power during their initial power-up, try starting the printer first and then the computer (instead of both at the same time)

### Display Screen Malfunction

CompTIA calls this 'no image on printer display'

* Try restarting
* Bad screen probably requires a replacement

## More specific printer problems (specific to impact, thermal, laser etc) - see your book

