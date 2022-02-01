# Display Technologies

## LCD Monitors - Liquid crystal display

### How LCDs work

* Backlight
* Polarizing Filter
* Polarizing agent & Thin-Film Transistor (TFT) matrix, or active matrix
* A translucent sheet give the ability to have RGB subpixels, even though it starts out white
* 2nd Polarizing filter 90 degrees to the first

### LCD Components

* LCD panel
* Backlight
* Inverter (in older models)

### LCD Panel Technologies

* Twisted nematics (TN) - most common
  * Cheapest
  * High refresh rates
  * Poor color reproduction
  * Most restricted viewing angle
* In-plane switching (IPS) - 2nd most common
  * Best color
  * Widest viewing angle
  * Most expensive
* Vertical alignment (VA)
  * Better response than IPS, but better color than TN

## LCD Variations

### Backlights

* Light-emitting diode (LED)
  * Uses DC
  * Edge LED backlighting - edges may be brighter than the middle
  * Direct LED backlighting - better uniformity of brightness
* Previous generations used CCFL - (Cold Cathode Fluorescent Lamp)
  * Requires an inverter because they need high frequency AC
  * Noticeably thicker than LED styles

### Resolution

* Designed to run at a single **native resolution**
  * At lower resolutions, uses interpolation to soften the jagged corners of pixes that don't line up perfectly
* The number of pixels arranged on the screen define the aspect ratio of the picture, such as 16:9 or 21:9

### Brightness

* Measured in nits
  * Varies from 100 nits to 1000 or more nits. On average around 300 nits

### Other considerations

* Viewing Angle
* Response Rate - amount of time for all sub-pixels to change from one state to another
* Refresh Rate - How often the screen change change or update completely
* Contrast Ratio - The difference between the darkest and lightest spots
* Color Depth - The amount of colors the panel can display

# Projectors

Projectors generate an image in one device and then use light to throw it onto some other object

Vocabulary

* Lumens - the amount of light given off by a light source
  * 1 lumen = amount of light reflected off of a 1 square meter area that is one meter from a one candela light source
  * 1 nit = one candela per square meter
  * A quick and dirty conversion: Multiply nits by 3.426 to get lumens
* Throw - The distance the projector must have to project a 100-inch diagonal screen
  * A typical projector must be 11 to 12 feet away
  * A short-throw projector must be 4 feet away
* Lamps - Generate the light
  * Three common varieties
    * metal halide
      * Very bright
      * Fans take up a lot of space
      * Average lifespan of 3000 hours
    * LED
      * Dimmer
      * Smaller overall
      * Lifespans of 20,000+ hours
    * Laser
      * more expensive
      * good, high-contrast images
      * 30,000+ hours lifespan

# Common connectors

* VGA - video graphics adapter

  * 15-pin, 3-row D-type connector
  * Usually blue
  * Video only, oldest and least capable connection type

* DVI - Digital visual interface

  Several different connections (https://components101.com/connectors/dvi-connector)

  * DVI-A - Analog, compatible with VGA
  * DVI-D - Digital, compatible with HDMI
  * DVI-I - Integrated
    * Single Link
    * Dual Link - Double the throughput

* HDMI - High Definition Multimedia Interface

  * Carries both Video and audio signals
  * Mini-HDMI connections exist also

* DisplayPort

  * Similar to HDMI
  * mini-Displayport (mDP)

* HDBaseT

  * Uncompressed HD video and audio over Cat 5a or Cat 6 network cables

# Display Adapters

## Motherboard slots

* PCI - Peripheral Component Interconnect
* AGP - Accelerated Graphics Port
* PCIe
* Onboard

## GPU

MSI GeForce GTX 1080ti 11-GB 384-bit GDDR5X PCI Express 3.0

* GeForce GTX 1080ti is the graphics processor
* 11-GB 384-bit GDDR5X describe the video RAM and the connection to the graphics processor
* PCI express 3.0 describes the expansion slot

* Larger bus means better access to VRAM

## Integrated GPUs

* Not very good for intensive gaming
* AMD has an APU - Accelerated Processing Unit that has two to four CPU cores, a memory controller, and a GPU
* Lower power consumption - good for portable computers like laptops and phones

# Software

* Display Settings; Start | Settings | System | Display Settings
  * Multiple displays
    * Extend
    * Duplicate
* DirectX
  * API that provides the ability for the programmer to talk directly with the hardware
  * DirectX Diagnostic Tool (dxdiag) allows you to see the current version of DirectX installed

# Troubleshooting Video

Incompatible drivers or incorrect settings

* SVGA mode
* blank monitor
* lock up
* display a garbled screen with weird patterns
* incorrect color patterns
* distorted image
* oversized images

Overheating graphics card or bad video RAM

* bizarre screen outputs followed by screen lockup
* Usually Windows keeps running

Because of high-voltage and the difficulty of repair, it is not recommended to open a monitor without specialized training

