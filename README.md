# SAVOOD Firmware-Ablage

Dieses Repository enthaelt NUR Firmware-Update-Pakete des SAVOOD-Displays
(ESP32-P4). Kein Quelltext.

Jedes Release enthaelt:
- `savood_display.bin` — das Firmware-Abbild
- `manifest.json` — Version, Groesse, SHA256, Abholadresse

**Veroeffentlichen nur ueber `tools/ota_veroeffentlichen.py`.** Das Werkzeug prueft
vorher hart, dass im Abbild KEINE WLAN-Zugangsdaten stehen (Byte-Suche), und
bricht sonst mit Exit 3 ab. Ein oeffentlich abrufbares Abbild mit Passwort waere
ein Leck mit jedem Update.

Abholen (Beispiel):
```
https://github.com/janbleile09-lab/savood-firmware/releases/latest/download/manifest.json
https://github.com/janbleile09-lab/savood-firmware/releases/download/<tag>/savood_display.bin
```
