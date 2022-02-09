# Understanding Electricy

## How we measure electricity

The pressure of the electrons in the wire is called **voltage**, measured in Volts (V)

The amount of electrons moving past a certain point in the wire is called **current**, or amperage and is measured in Amps (A)

The total amount of power being delivered is the **wattage**, and is measured in Watts (W). It can be calculated by: W = V * A

* Total usage over an amount of time (technically called work) is usually measured in Kilowatt-hours (# of kilowatts * # of hours)
* 1 horsepower is approximately 746 W, or 6.2A delivered at 120V

The tendency for wires to prevent the flow of electricity is called **resistance** and is measured in Ohms (Ω)

* Larger diameter wires have lower resistance than smaller diameter wires
* Resistance tends to increase as the conductive material gets hotter
* Energy dissipated because of resistance is usually lost as heat

## How electricity flows

Direct current - electrons flow consistently in one direction

* Batteries
* Used in most electronics
* LED bulbs
* Circuits are formed by connecting two different voltage levels (ground = 0V)

Alternating current - the direction of flow is constantly changing (60Hz in US, 50Hz elsewhere)

* Whenever power is delivered over long distances (much less power lost over distance)
* Microwaves
* Incandescent lights
* Circuits are formed by connecting a hot wire to a neutral. Grounds are present for safety

## Powering your device

### Power Supply Units (PSU)

* One of the Field Replaceable Units (FRU) - PSU, RAM, and a hard drive
* Most PSUs are Dual-voltage
  * The US uses 110-120V
  * Most of the rest of the world uses 220-240V
* Converts from wall power to the various levels of DC that are needed: 12V, 5V, 3.3V, etc
* Good ones come with active power factor correction (active PFC) to prevent harmonics in the power supply
* Some are modular, allowing you to unplug unused cables to tidy up the inside of the computer

### Power Adapter

Converts from wall power to a single level of DC power, example: 5V

## Tools

### Multimeters

You can use a multimeter to measure parts of an electric circuit

* AC voltage
* DC voltage
* Resistance
* Continuity test
* Voltages on a PSU can vary by +- 10%
* Can be used to test wall power, or power inside the computer

### Circuit Tester

Checks to see if polarity is reverse, ground is present

### Surge Suppressors

Prevent spikes in voltage from damaging your equipment

* Spikes are usually from powering other devices on/off (not lightning)

Rated in joules - how much energy it can suppress before it fail. They wear out over time and need to be replaced

### Power Conditioning

Cleans up the transmission to filter out EMI and RFI

### Uninterruptible Power Supply (UPS)

Battery backup

* Measured in Watts (W) and Volt-Amps (VA)
  * VA is the amount of power the UPS could supply if the devices took power from the UPS in the perfect way
* Should give time @ power usage
* With line-interactive UPS, the inverter is always active

# Supplying DC power

## Motherboard

Usually 20- or 24-pin P1 power connector

Some motherboards require a supplemental 4-, 6-, or 8- pin connectors

## Peripherals

### Molex

* Supplies 5- and 12-V current
* Fans and older drives

### Mini Connector (Berg)

* Supplies 5- and 12-V current
* Floppy disks and occasional other devices

### Sata Power

* 15-pin
* 3.3- 5- and 12-V
* hot swappable
* L-shaped connector

### Splitters and Adapters

* Beware that you're not drawing too much

## ATX

* 20-pin P1 motherboard power
* 5V always on
* Soft power to turn on power supply, controlled by software

  * Allows system to sleep and wake
  * Prevents the user from cutting power without shutting down

  * Allows power over LAN

### ATX 12V 1.3

* P4 power connector
* More 12V power to assist the 20/24 pin connector
* 6-pin AUX connector - 3.3V and 5V to motherboard

### EPS12V

* More power for servers
* Introduced rails

### Rails

* Single-rail has one over-current protection (OCP)
* Multi-rail has multiple OCP, allowing more voltage where it's needed while still protecting elsewhere

### ATX12V 2.0

* 20/24 pin motherboard connector (usually convertible)
* Dropped AUX requirement
* Requires two 12V rails for any rating higher than 230W
* Usually have 8-pin CPU power connector (referred to as EPS12V, EATX12V, or ATX12V 2x4)

### Niche-Market Power Supply Form Factors

* Mini-ITX and microATX
* TFX12V
* SFX12V

## PSU Ratings

### Wattage

Total wattage that can be delivered

* Hard drives may take 15W, while a processor takes 151W
* Not enough power usually means the computer does nothing

### Efficiency

* Some of the energy is lost when converting AC to DC
* Efficiency can vary from 70% (min for ATX) to 94%
* Bronze: 85%, Gold: 90%, Titanium: 94%
* Efficiency ratings are gathered at with a wattage load, lower efficiency outside of that
* Allow room for upgrades
* https://outervision.com/power-supply-calculator

# Safety

Don't open up a power supply without further training - the capacitors inside can retain a charge even with unplugged

In case of fire, use an appropriate fire extinguisher

* Class A - Ordinary free-burning combustible, such as wood or paper
* Class B - Flammable liquids, such as gasoline, solvents, or paint
* Class C - Live electrical equipment
* Class D - Combustible metals such as titanium or magnesium
* Class K - Cooking oils, trans-fats, or fats
* Class ABC is common, though it can leave residue on computing equipment

# Troubleshooting

Voltages out-of-spec (beyond 10%)

No power

* The motherboard could be the problem
  * Short green to any black to see if power supply turns on
* Power supply switch (on/off) on back

Slow failure

* Computer requires a few boots to get going
* Computer locks up after an hour or two
* New devices aren't recognized immediately

