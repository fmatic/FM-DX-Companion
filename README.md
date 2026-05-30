FM-DX Companion

A lightweight browser-based companion for SDRconnect and FM-DX enthusiasts.

FM-DX Companion combines FMScan userlists, SDRconnect WebSocket data, FMList logging and FMDX Maps into a streamlined DX workflow.

⸻

Features

* Real-time SDRconnect integration via WebSocket
* PI and PS based station matching
* Supports FMScan Tropo, Sporadic-E and Meteor Scatter userlists
* FMList logging integration
* FMDX Maps integration
* Automatic remarks generation
* Browser-based, no installation required
* Local storage using IndexedDB
* Fast station lookup and ranking

⸻

Requirements

1. SDRconnect

Enable the WebSocket Server in SDRconnect.

Default connection:

ws://127.0.0.1:5454

2. FMScan Userlists

Download all three FMScan userlists:

* Tropo
* Sporadic-E
* Meteor Scatter

When exporting, use:

* CSV format
* TAB separator

Example:

3. Rename Files

Rename the downloaded files to:

tropo.csv
es.csv
meteor.csv

4. Load Lists

Open FM-DX Companion and import:

* Tropo → tropo.csv
* Es → es.csv
* Meteor → meteor.csv

The lists are stored locally in your browser and automatically restored the next time you open Companion.

⸻

Typical Workflow

1. Tune a station in SDRconnect
2. Companion receives frequency, PI and PS information
3. Matching stations are ranked automatically
4. Right-click a station entry
5. Open FMList logging or FMDX Maps
6. Remarks are automatically copied to clipboard
7. Log the station

⸻

Current Status

v0.5.0 — Initial Public Beta

FM-DX Companion is already fully usable for everyday FM-DX work.

Planned future improvements include:

* Toast notifications
* Station search
* Site Explorer
* PI history
* DX notes
* Companion themes for FMList
* Companion themes for FMDX Maps

⸻

Philosophy

FM-DX Companion is intentionally lightweight.

It is not intended to replace SDRconnect, FMList or FMDX Maps.

Instead, it acts as a bridge between them, providing a faster and more efficient FM-DX workflow while keeping the interface simple and distraction-free.

⸻

Author

Developed in Finland 🇫🇮 by Janne Heinikangas

* Blog: https://fmatic.online
* GitHub: https://github.com/fmatic

⸻

“Minimal DX workflow for SDRconnect users.”
