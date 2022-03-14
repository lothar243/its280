### Problems with specific Apps

* Force stop - In Android, using the application manager to stop the app and any background processes
  * Beware that this can cause a loss of data

* Apps can typically be uninstalled in the device's application manager
  * Often they can be uninstalled via the App store also
* Apps not loading
  * May be hardware requirement (RAM, storage, processor)
  * Check the logs for errors (may require third-party tools)

* Soft Reset - restarting the device, whether from within the OS or by hardware button

* Reset to Factory Default, or factory reset

### Touchscreen and Display issues

* Dim display
  * Brightness control
  * Auto-brightness
* Touchscreen responsiveness
  * Accidental Touch
    * Hold the device in such a way as to not touch it
    * Moisture on the screen can sometimes cause this
  * Dirty Screen
  * Performance problems
  * Screen protector poorly installed
  * Calibration and Diagnostics
    * May be hidden, consult documentation to learn how to access
  * Physical damage
    * Immersion in water - Liquid Contact Indicator (LCI) stickers change color when they get wet

### Overheating

* External factors (temperature, sun)
* Charging while in use
* Processor-intensive activities
* Device may shut down to protect it

### Slow Performance

* Low RAM
  * Check background apps
* Low storage space
  * Removable storage like microSD

### Battery Life

* Worn out battery
* Frequently used radios (cellular and WiFi)
* Location - GPS and other radios
* Excessive processing
  * The phone may show what app is using your battery
* External power pack - external battery
* Reducing display settings - power-saving modes

### Swollen Battery

* Usually caused by overcharging and/or overheating
* Dangerous - stop using it
* http://reddit.com/r/spicypillows

## Mobile Security

### Unauthorized access

* Authentication factors
  * Something you know (passcode, PIN)
  * Something you are (Fingerprint, face scan) - Biometric
  * Something you have (smart card, OTP app)
* Screen Lock
* Install verification
* System lockout or Wipe device if too many failed attempts
* Full Device Encryption
* Remote wipe

### Bring Your Own Device (BYOD)

Employees use personal devices on a employer's network and for work

IT has much less control over their network

* Mobile Device Management (MDM) - Regain some control by IT over devices used for work

### Malware

iOS - Doesn't allow sideloading and is much more strict about their store

* They may be required to allow third-party stores soon

Android - Be careful what you download

* Anti-malware isn't very good at spotting original malware
* Permissions required for functionality
* Malware can be introduced after the initial download (during an update)

Symptoms/Clues

* Unexpected Resource Use
* Power Drain and High Resource Utilization
* Slow Data Speeds
* Data Transmission Over Limit

### Network-based attacks

* Open Networking packet sniffing
* Evil Twin - Exploiting automatic SSID-based connection
  * Wi-Fi analyzer app can be used to find these
  * Can also be done with cellular (tower spoofing/Stingray)

### Unauthorized Root Access

* Jailbreaking - Allowing users to side-load apps to iOS devices
* Rooting - Gaining root-level access to an Android