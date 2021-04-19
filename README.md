# knidos-notices
## Festlegungen
- NMEA = NMEA 2000, NMEA 0183 wird immer explizit genannt

## NMEA 0183 Kabel
- schwarz: OUT (-)
- grün: IN (-)
- gelb: IN (+)
- orange: OUT (+)
- Gibt es korrespondierende Minusleitungen (NMEA OUT / IN -, NMEA Tx / Rx – o.ä.), verbindest Du sie ebenfalls miteinander; fehlen sie, verwendest Du ersatzweise die Masseleitung (auch, wenn sie nur auf einer Seite fehlt).

## Legende Kabelbinder
- gelb: Cortex
    - GPS-Antenne
    - Power
    - Sensors NMEA 0183
    - VHF
- blau: Raymarine
    - RF-Base
    - Niedergang Geräte
    - Autopilot
- rot: Delta M22 Antenne
- rot rot: Delta 900S Antenne

## Legende
- RF-Base: Station für Fernbedingung Autopilot
- Backbone: Ein Backbone ist eine Hauptleitung. Der Backbone ist das sozusagen das Rückgrat (englisch Backbone) eines Netzwerks. Lokale Leitungen verbinden sich mit diesen zentralen Leitungen und speisen ihre Daten ein.
- Spurkabel: Verbindet Seatalk_ng Geräte mit Backbone

## Smart Pilot
- Steuerung des Autopiloten
- Belegte Slots sind
    - [in] Fluxgate: compass inputs
    - [in] Ruder: possition sensors
    - [in/out] Seatalk 1: seatalk 2 seatalk_ng + x?!
    - [in/out] Seatalk 2: unknown
    - [in/out] PWR
    - [out] Antriebsmotor
    - [out] Antriebskupplung
- Sealtalk 2 Seatalk_ng
    - gelb: Seatalk, siehe [in/out] Seatalk
    - blau: Backbone Plotter oder Autopilot?
    - weiß: Spurkabel Strom

## Cortex - System
- NMEA 0183, Orange und Schwarz werden nach hinten in einem grauen Kabel zum Plotter gerootet.
    - mappinng: weiß|weiß, schwarz|grün (gnd)
- Audio Außenlautsprecher rot = plus, scharz = minus
    - Kabel zum Lautsprecher blau = minus und braun = plus [ACHTUNG!]
    - Lautsprecher lässt sich über Handheld steuern
- NMEA 0183 scheint nur Output zu sein, NMEA 2000 input/output
- Sealtalk-NMEA-Interface anschließen: gelb an gelb und grün an grün (an NMEA 0183 Kabel) [NOT_WORKING]

## Navtex
- Multiklemme liefert Daten für Navtex Receiver

## Antenne
- Wir haben die Pacific von rr

## TODOs
- Kabel an Smart Pilot sicher?
- Dokumentation

### Einkaufsliste svb
- 73710: PL-Stecker für RG58U Kabel: Antennenkabel zu Cortex Adapter
- 98564: Seatalk NG Backbone Kabel 9m : Seatalk 2 Sealtalk_ng Bridge zu T-Adapter
- 98571: SeaTalk NG T-Stück : Verbindung Backbonekabel zu Cortex
- 60707: Adapterkabel SeaTalk NG auf NMEA 2000 female : Kabel von T-Stück zu Cortex
- 95507: BNC-BNC Verbindungskabel : Cortex Splitter zu AV-Box
- BNC-Koax Adapter für Radio

## Things
- 3 pending GPS-Kabel eines nach hinten, eines der Pilz vorne?
- Woher kommen welche Sensordaten und wohin fließen sie? -> Siehe Datenflussdiagramm WIP


## Datenflüsse

### Antennennetzwerk
[antenna_network]: datenfluss/antenna_network.png "Antennennetzwerk"
![antenna_network]

### Datenfluss Raymarine
[sensordata]: datenfluss/sensordata.png "Sensordatenfluss"
![sensordata]

### Cortex
[cortex]: datenfluss/cortex.png "Cortex"
![cortex]

### Cortex Netzwerk (upcomming)
[cortex_network]: datenfluss/cortex_network.png "Cortex Netzwerk"
![cortex_network]
