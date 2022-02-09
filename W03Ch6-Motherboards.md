# Motherboards

## Form factor

Describes the size of the board and general location of components

### AT

* Invented in the early 1980
* Big and a variety of sizes, around 12"x13"

* No external ports except a keyboard

### ATX

* Most common
* Full real panel for necessary ports
* 12"x9.6"
* CPU and RAM are positioned to provide easier access
* Long expansion cards won't collide with the CPU or northbridge
* The RAM is closer to the CPU

### microATX

* Smaller than an ATX: 9.6"x9.6" (usually)
* Sometimes referred to with the Greek letter micro: μATX
* FlexATX (not in use any more) was a smaller version of microATX

### ITX

* Didn't see widespread use

### Mini-ITX

* 6.7"x6.7" - quite small

### Proprietary Form Factors

* Non-standard
* Some make use of riser cards (aka daughter boards)

## Chipset

Defines the type of processor and RAM the motherboard requires

Defines the built-in devices that the motherboard supports

Generally either Intel or AMD

Classically, there was a Northbridge and a Southbridge, named for their usual location on the motherboard

### Northbridge

* Connects directly to CPU
* RAM
* Expansion devices (PCIe)
* Needed additional cooling, usually a fanless heat-sink

### Southbridge

* Does not connect directly to CPU
* USB
* PCI
* SATA
* IDE

### Super I/O chip

* Non-standard, used for some of the southbridge functions

### Platform Controller Hub (PCH)

* Intel's single chip chipset that takes the place of the northbridge/southbridge

## Standard Components

* CPU
* RAM
* Mass storage

## Additional Components

* USB
* Sound
* Networking
* Video
* RAID
* Case Fan

# Expansion Bus

The wires and accompanying support chips to add additional components

## PCI

* Not in use any more
* Originally 32 bits wide, at 33 MHz
* Devices are self-configuring
* There was also a Mini-PCI for laptops

## PCI Express

Uses a point-to-point serial connection, rather than a shared parallel connection. Why would serial be faster than parallel?

* Each devices has a certain number of dedicated lanes (a single wire for each direction of communication)
* Lane speeds vary by PCIe version
  * 1.x: 2.5 gigatransfers per second (GTps)
  * 2.x: 5 GTps
  * 3.x: 8 GTps
  * 4.x: 16 GTps
  * 5.0: 32 GTps
  * 6.0: 64 GTps (spec released 11 Jan, 2022)
* Smaller cards can fit in larger slots

# Choosing a Motherboard

Considerations

* The motherboard must fit the case - most support ATX, but some may be smaller
* Correct chipset
* Enough RAM slots
* Manufacturer: ASUS, BIOSTAR, GIGABYTE, Intel, and MSI are popular

Motherboards are installed on standoffs - specialized screws to keep the motherboards off the case

Front panel connections - be sure to refer to the manual

* Switches work either way
* LEDs only work one way

# Troubleshooting

* Catastrophic failure - if a capacitor pops, or a short fries a component

* Burn-in failure - (Rare) If a system was working and fails for seemingly no reason in the first 30 days
* Component failure - May be a number of factors
  * Faulty component
  * Buggy device driver
  * Buggy application software
  * Problems with OS
  * Power supply problems

## Techniques

Requires patience and a methodical approach, document actions and findings to discover patterns

* Check
* Replace
* Verify good components

