AMS SpoolEdit – Smart Filament Management for Bambu AMS with NFC funktionality.
English Documentation
The AMS SpoolEdit is a standalone ESP32-S3 touch display designed for convenient filament spool management for the Bambu Lab AMS.

The project allows you to manage remaining filament weight, edit spool information, synchronize data between devices and even store spool information directly on NFC tags.

The system is completely standalone and does not require any cloud services or additional software.

 
Features
✅ Manage up to 32 filament spools

✅ 4 or 8 AMS mode

✅ Remaining filament weight management

✅ Material, type, color, manufacturer and article information

✅ Edit spool data directly on the display

✅ Modern web interface for smartphone, tablet and PC

✅ JSON import / export

✅ WiFi configuration via the web interface

✅ MQTT support

✅ HTTP fallback mode (works completely without MQTT)

✅ Optional AMS Dial support

✅ NFC synchronization

✅ Automatic timestamp-based conflict resolution

✅ German and English language support

✅ Switchable display rotation

✅ AP setup mode

✅ Factory reset

 
Hardware
Supported Hardware
Main Device
ESP32-S3 Touch Display (240x320)
Optional
PN532 NFC Reader (I²C)
AMS Dial
MQTT Server
 
Spool Management
Each spool stores:

Spool number
Remaining weight
Material
Type
Color
Manufacturer
Article number
Empty status
Timestamp of the last modification
All data is permanently stored in LittleFS.

 
Display Functions
Subtract Used Filament
Used filament can be directly subtracted from the selected spool using the touchscreen.

Swap Spools
Spools can be swapped directly on the display.

All spool data is transferred automatically.

Edit Spools
The following information can be modified:

Material
Type
Color
Manufacturer
Article number
Empty status
 
Web Interface
The integrated web interface allows:

View all spools
Edit spool information
Change remaining weight
Swap spools
JSON import / export
WiFi configuration
The web interface works on:

Smartphone
Tablet
Desktop PC
 
WiFi Setup
On first startup the display automatically enters AP mode.

Connection Information
SSID:

AMS-Setup
Password:

12345678
Open in your browser:

http://192.168.4.1
After saving the WiFi credentials, the device automatically reboots.

 
MQTT (Optional)
MQTT is completely optional.

If no MQTT server is available, the display automatically switches to HTTP mode.

Examples of supported integrations:

Home Assistant
Node-RED
Custom MQTT systems
 
HTTP Fallback
All display functions can be used completely without MQTT.

Communication is then automatically handled via HTTP.

 
AMS Dial (Optional)
The optional AMS Dial allows:

Selecting a spool
Changing remaining filament weight
Swapping spools
Communication automatically works via:

MQTT
or HTTP
 
NFC Support
The display supports NFC tags in combination with a PN532 reader.

Stored Data
Spool number
Remaining weight
Material
Type
Color
Manufacturer
Article number
Empty status
Timestamp
 
NFC Synchronization
When an NFC tag is read, timestamps are automatically compared.

NFC is newer
The data is imported into the display.

Display is newer
The NFC tag is automatically updated.

Both are identical
No action is taken.

This makes it easy to synchronize filament spools between multiple printers or even different users.

 
Languages
Supported languages:

German
English
The selected language is permanently stored.

 
Display Rotation
Supported installation orientations:

USB port on top
USB port on bottom
Display and touch orientation are adjusted automatically.

The setting is permanently stored.

 
Import / Export
All spool data can be exported as a JSON file.

The file can be used:

as a backup
to transfer data to another display
after a factory reset
 
Factory Reset
The web interface allows deleting:

WiFi credentials
Display IP address
MQTT IP address
After reboot the device automatically starts in AP mode again.

 
Project Status
This project is under active development.

New features and suggestions are always welcome.

 
Support
For questions, issues or feature requests:

Use GitHub Issues
Pull Requests are welcome
Feedback is highly appreciated
 
❤️ Enjoy managing your filament spools!
