<img width="4284" height="5712" alt="image" src="https://github.com/user-attachments/assets/bee71751-cd44-4ed7-8430-dc3fd0e3cff6" />

<img width="3024" height="4032" alt="image" src="https://github.com/user-attachments/assets/e4b4e4cd-57ad-4bbb-9629-a607b5462a06" />

# AMS_SpoolEdit
AMS SpoolEdit - Intelligentes Filamentmanagement für das Bambu AMS mit NFC Funktionalität.

Das AMS SpoolEdit ist ein eigenständiges ESP32-S3 Touch-Display zur komfortablen Verwaltung von Filamentspulen für das Bambu Lab AMS. Es ist ein Weiterentwicklung meines AMS Spool Display.

https://github.com/paulchen67/AMS_Spool_Display

Das Projekt ermöglicht die Verwaltung des Restgewichts, die Bearbeitung von Spulendaten, die Synchronisation zwischen mehreren Geräten und die Speicherung von Spulendaten direkt auf NFC-Tags.

Das AMS SpoolEdit benötigt einen M5 Stack Dial.

Die Firmware für den Dial findet Ihr hier.

https://github.com/paulchen67/AMS_Spool_Display/releases/tag/V1.3Dial

Das AMS SpoolEdit System arbeitet vollständig eigenständig und benötigt weder Cloud-Dienste noch zusätzliche Software.

---
 
# Features

✅ Verwaltung von bis zu 32 Filamentspulen

✅ 4- oder 8-AMS-Modus

✅ Restgewichtsverwaltung

✅ Material-, Typ-, Farb-, Hersteller- und Artikelinformationen

✅ Bearbeitung der Spulendaten direkt am Display

✅ Moderne Weboberfläche für Smartphone, Tablet und PC

✅ JSON Import / Export

✅ WLAN-Konfiguration direkt über die Weboberfläche

✅ MQTT-Unterstützung

✅ HTTP-Fallback (funktioniert vollständig ohne MQTT)

✅ Unterstützung für den optionalen AMS Dial

✅ NFC-Synchronisation

✅ Automatische Konfliktlösung über Zeitstempel

✅ Deutsch- und Englisch-Unterstützung

✅ Umschaltbare Displayrotation

✅ AP-Setup-Modus

✅ Factory Reset

---

# Hardware

Unterstützte Hardware

Hauptgerät
ESP32-S3 Touch Display (240x320)

PN532 NFC Reader(I²C)

AMS Dial

MQTT Server

---
 
# Spulenverwaltung

Jede Spule speichert:

- Spulennummer
- Restgewicht
- Material
- Typ
- Farbe
- Hersteller
- Artikelnummer
- Leer-Status
- Zeitstempel der letzten Änderung

Die Daten werden dauerhaft im LittleFS gespeichert.

---
 
# Display Funktionen

Filamentverbrauch erfassen
Über das Touchdisplay kann verbrauchtes Filament direkt von der jeweiligen Spule abgezogen werden.

Spulen tauschen
Spulen können direkt am Display miteinander getauscht werden.

Alle Daten werden automatisch übernommen.

Spulen bearbeiten
Folgende Informationen können geändert werden:

- Material
- Typ
- Farbe
- Hersteller
- Artikelnummer
- Leer-Status

---
 
# Web Interface
Die integrierte Weboberfläche ermöglicht:

- Anzeige aller Spulen
- Bearbeiten der Spulendaten
- Ändern des Restgewichts
- Spulen tauschen
- JSON Import / Export
- WLAN-Konfiguration

Die Weboberfläche funktioniert auf:

Smartphone

Tablet

Desktop-PC

---

# WLAN Einrichtung

Beim ersten Start startet das Display automatisch im AP-Modus.

Zugangsdaten

SSID: AMS-Setup

Passwort:12345678

Aufruf im Browser: http://192.168.4.1 ==> (PC oder Laptop benutzen, am Smartphone kann evtl. das Speichern nicht funktionieren)

Nach dem Speichern der WLAN-Daten startet das Gerät automatisch neu.

---
 
# MQTT (optional)

MQTT ist vollständig optional.

Ist kein MQTT-Server vorhanden, arbeitet das Display automatisch im HTTP-Modus.

Unterstützt werden beispielsweise:

- Home Assistant
- Node-RED
- Eigene MQTT-Systeme

---
 
# HTTP Fallback

Alle Funktionen des Displays können vollständig ohne MQTT verwendet werden.

Die Kommunikation erfolgt dann automatisch per HTTP.

---
 
# AMS Dial

Der AMS Dial ermöglicht:

- Auswahl einer Spule
- Änderung des Restgewichts
- Tauschen von Spulen
- 
Die Kommunikation erfolgt automatisch über:

MQTT oder HTTP

https://github.com/paulchen67/AMS_Spool_Display/releases/tag/V1.3Dial

---

# NFC Unterstützung

Das Display unterstützt NFC-Tags in Verbindung mit einem PN532 Reader.

Gespeicherte Daten

- Spulennummer
- Restgewicht
- Material
- Typ
- Farbe
- Hersteller
- Artikelnummer
- Leer-Status
- Zeitstempel

---
 
# NFC Synchronisation

Beim Lesen eines NFC-Tags werden die Zeitstempel verglichen.

NFC ist neuer
Die Daten werden in das Display importiert.

Display ist neuer
Der NFC-Tag wird automatisch aktualisiert.

Beide identisch
Es erfolgt keine Änderung.

Dadurch können Spulen problemlos zwischen mehreren Druckern oder sogar verschiedenen Nutzern synchronisiert werden.

---
 
# Sprache

Unterstützte Sprachen:

- Deutsch
- Englisch

Die Spracheinstellung wird dauerhaft gespeichert.

---
 
# Display Rotation

Unterstützte Einbaulagen:

- USB-Anschluss oben
- USB-Anschluss unten
- 
Display und Touchscreen werden automatisch angepasst.

Die Einstellung wird dauerhaft gespeichert.

---
 
# Import / Export

Alle Spulendaten können als JSON-Datei exportiert werden.

Die Datei kann verwendet werden:

- als Backup
- zum Übertragen auf ein anderes Display
- nach einem Factory Reset

---
 
# Factory Reset

Über die Weboberfläche können gelöscht werden:

- WLAN-Daten
- Display-IP
- MQTT-IP

Nach dem Neustart startet das Gerät automatisch wieder im AP-Modus.

---
 
# Projektstatus

Das Projekt befindet sich in aktiver Entwicklung.

Neue Funktionen und Verbesserungsvorschläge sind jederzeit willkommen.

---
 
# Support
Bei Fragen, Problemen oder Verbesserungsvorschlägen:

GitHub Issues verwenden

Pull Requests sind willkommen

Feedback ist ausdrücklich erwünscht

---
 
❤️ Viel Spaß beim Verwalten eurer Filamentspulen!

---

<img width="4812" height="4281" alt="Bild alle Teile ohne 3D Druck" src="https://github.com/user-attachments/assets/47c860bf-ad79-4df1-a7e4-be4ee9cef14c" />


### Stückliste

https://github.com/paulchen67/AMS_SpoolEdit/blob/main/Parts%20List/St%C3%BCckliste.md

---
English Version here

https://github.com/paulchen67/AMS_SpoolEdit/blob/main/README_ENG.md
