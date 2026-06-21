# AMS_SpoolEdit
AMS SpoolEdit - Intelligentes Filamentmanagement für das Bambu AMS mit NFC Funktionalität
Das AMS SpoolEdit ist ein eigenständiges ESP32-S3 Touch-Display zur komfortablen Verwaltung von Filamentspulen für das Bambu Lab AMS.

Es ermöglicht eine einfache Verwaltung des Restgewichts, die Bearbeitung von Spulendaten, die Synchronisation zwischen mehreren Geräten und sogar das Speichern der Spulendaten direkt auf NFC-Tags.

Keine Cloud, keine Abonnements und keine zusätzliche Software erforderlich.

Funktionen
✅ Verwaltung von bis zu 32 Filamentspulen

✅ 4- oder 8-AMS-Modus

✅ Verwaltung des verbleibenden Filamentgewichts

✅ Speicherung von Material, Typ, Farbe, Hersteller und Artikelnummer

✅ Bearbeitung der Spulendaten direkt am Display

✅ Moderne Weboberfläche für Smartphone, Tablet und PC

✅ Import und Export aller Spulendaten als JSON-Datei

✅ MQTT-Unterstützung

✅ HTTP-Fallback (funktioniert auch ohne MQTT)

✅ Unterstützung für den optionalen AMS Dial

✅ NFC-Tag-Synchronisation

✅ Automatische Konfliktlösung über Zeitstempel

✅ Deutsch- und Englisch-Unterstützung

✅ Umschaltbare Displayrotation (USB-Anschluss oben oder unten)

✅ AP-Setup-Modus zur einfachen WLAN-Konfiguration

 
NFC-Synchronisation
Das Display kann komplette Spulendaten direkt auf einem NFC-Tag speichern.

Gespeicherte Daten:

Spulennummer
Restgewicht
Material
Typ
Farbe
Hersteller
Artikelnummer
Leer-Status
Zeitstempel der letzten Änderung
Beim erneuten Einlegen einer Spule vergleicht das Display automatisch die Zeitstempel:

NFC-Daten sind neuer → Daten vom Tag werden importiert.
Display-Daten sind neuer → Der NFC-Tag wird automatisch aktualisiert.
Beide Datenstände sind identisch → Es erfolgt keine Änderung.
Dadurch können Spulen problemlos zwischen mehreren Druckern oder sogar zwischen verschiedenen Nutzern ausgetauscht werden, ohne dass Informationen verloren gehen.

 
Weboberfläche
Die integrierte Weboberfläche ermöglicht:

Anzeige aller Spulen
Bearbeitung der Spulendaten
Ändern des Restgewichts
Tauschen von Spulen
Import und Export von Daten
Konfiguration der WLAN-Einstellungen
Die Weboberfläche funktioniert auf:

Smartphone
Tablet
Desktop-PC
 
AMS Dial Unterstützung
Der optionale AMS Dial ermöglicht:

Auswahl einer Spule
Abziehen des verbrauchten Filaments
Tauschen von Spulen
Die Kommunikation erfolgt über MQTT oder automatisch per HTTP, wenn kein MQTT-Server vorhanden ist.

 
Einfache Einrichtung
Beim ersten Start startet das Display automatisch im AP-Setup-Modus.

Mit folgendem WLAN verbinden:

SSID: AMS-Setup

Passwort: 12345678

Anschließend im Browser öffnen:

http://192.168.4.1

und die eigenen WLAN-Daten eingeben.

 
Hardware
ESP32-S3 Touch Display
Optionaler PN532 NFC Reader (I²C)
Optionaler AMS Dial
 
Dieses Projekt wurde entwickelt, um das Filamentmanagement einfach, zuverlässig und unabhängig vom Drucker selbst zu machen.
