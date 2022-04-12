# Mobile Computing Devices

## Mobile Variants

### Smartphones

* Digital Assistant PDA - one of the earliest types of mobile device
* Smartphone - introduced by iPhone
* Tablets - similar to smartphones, but usually without cellular radio
* E-Readers - E-paper screens
* Wearables - (from the A+) smart watches, fitness monitors, and VR/AR headsets
  * Smart Watches - display notifications, time, messages, weather, music playback, etc
  * Fitness monitors - count steps, monitor heartrate, or maybe include a GPS
  * VR/AR headsets
    * Virtual Reality (VR) - take you into a simulated 3d space, immersive
    * Alternate reality (AR) - overlay onto existing world
      * Google Glass
      * Meta (Facebook) is developing something

## Mobile Hardware Features

### Screen Technologies

* Commonly some form of LCD
  * Twisted Nematics (TN) for inexpensive devices
  * In-Plane switching (IPS) for richer colors, like in iPad
  * Organic light-emitting diode (OLED) - mostly on smaller devices
    * Falling prices mean they are getting larger

### Cameras

* High dynamic range (HDR) - Keep the details in the dark shadows, even in a high contrast scene - very good for landscape photography
* Many phones now have dedicated cameras for different circumstances
  * Facing the user
  * Zoom/macro
  * Fisheye
  * Low light

### Microphones

* Commonly have more than one microphone to enable noise-canceling

### Digitizers

The 'touch' part of the touchscreen

* Transforms analog signals into digital ones
* Technically even digital cameras are examples of digitizers, but the A+ has this grouped with touchscreens

### Global Positioning System

* Uses GPS satellites to determine location
* Typically enabled with 'location' services, though this usually uses other facts also

# Mobile Operating Systems

## Developing for a Mobile OS

### Closed source

* Proprietary, or vendor-specific
* Usually protected via obfuscation and legal means

### Open Source

* Vendor shares how it is made (typically source code)
* Some people argue this makes devices more secure

### Software Development Kits (SDK)

* Used when creating new apps for the operating system
  * iOS SDK is Xcode
    * Have to pay a yearly fee and develop on their software
    * More rigid constraints on distributing through their App store
  * Android has Android Development Kit, among others
    * Google allows anyone to create Android apps
    * Adding apps to the Google play store is relatively easy

## Apple iOS

* Apple's mobile operating system, not to be confused with MacOS

* Apps are installed via the App Store, with few exceptions
* Proprietary
* Few models - more standardized
* Longer length of support (security updates)

## Google Android

* Open-source
* Based on Linux
* Many stores exist, such as the Google Play store, Samsung Store, F-Droid
* Apps can be installed from .apk file directly (called sideloading)
* Customizable Launchers
* Many different models - some features required to install certain versions of the OS
* Length of support (security updates) dependent on manufacturer, not Google

## Mobile OS Features

* Gestures - swipe between screens, pinch to zoom, etc
* Accelerometer - detect jarring motion
* Gyroscope - detect rotations
* Wi-Fi calling - sending information over non-cellular network
* Virtual Assistant - Voice-based control
* Emergency capabilities
  * Emergency notification - Amber alert, or disaster notification
  * Enhanced 911 (E911) - Uses GPS and cellular signal to triangulate the location of the phone - Geotracking
* Mobile Payment Service
  * Typically uses Near Field Communication (NFC)
* Airplane mode - turn off wireless radios (cellular, wifi, and bluetooth)
* Preferred Roaming List (PRL) - a priority-ordered list of carrier networks to connect to
* Product Release Instruction (PRI) - necessary if the network is changing or the device is moved to a new network
* Identifiers for your phone
  * International Mobile Equipment Identity (IMEI) - 15-digit number used to uniquely identify a mobile device
  * International Mobile Subscriber Indentity (IMSI) - Represents the account the phone will connect to
* Mobile Device Management (MDM)
  * Enterprise management of mobile devices, such as setting required security options, or performing a remote wipe when an employee no longer works for them
* VPN - Virtual Private network
  * Encrypt all communication to an endpoint

## Mobile Device Communication and Ports

### Micro-USB/Mini-USB

* Most Android devices made before 2017

### Lightning Connector

* Apple's Proprietary 8-pin connector
* Not keyed, so can be inserted upside-down

### USB Type-C

* Most common Android devices today
* Not keyed, so can be inserted upside-down
* Does not specify a speed of USB - it's merely the form factor (It can be USB 2.0)

### Bluetooth

### NFC

* Typically used for payment, but sometimes file transfer as well

### Magnetic Readers and Chip Readers

* Attach a card reader to a phone and have a very portable POS terminal

### Infrared

* Old, formerly used for data transfer
* Requires line of sight

### Hotspots and Tethering

* Hotspots - share cellular access via WiFi
* Tethering - share cellular access via cable (USB usually)