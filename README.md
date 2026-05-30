### FM-DX Companion

A lightweight browser-based companion for SDRconnect and FM-DX enthusiasts.

FM-DX Companion combines FMScan userlists, SDRconnect WebSocket data and FMList logging into a single, simple workflow.

Features

* Real-time SDRconnect integration via WebSocket
* PI and PS based station matching
* Supports FMScan Tropo, Sporadic-E and Meteor Scatter userlists
* FMList logging integration
* FMDX Map integration
* Automatic remarks generation
* Browser-based, no installation required
* Stores userlists locally using IndexedDB

## Requirements

1. SDRconnect

Enable the SDRconnect WebSocket Server.

Default connection:
```
ws://127.0.0.1:5454
```
2. FMScan Userlists

Download all three FMScan userlists:

* Tropo
* Sporadic-E
* Meteor Scatter

Use the following settings when exporting:

* CSV format
* TAB separator

3. Rename Files

Rename the downloaded files as:

tropo.csv
es.csv
meteor.csv

4. Load Lists

Open FM-DX Companion and import:

* Tropo → tropo.csv
* Es → es.csv
* Meteor → meteor.csv

The lists are stored locally in your browser and will automatically reload the next time you open Companion.

⸻

Workflow

1. Tune a station in SDRconnect
2. Companion receives frequency, PI and PS information
3. Matching stations are ranked automatically
4. Right-click a station
5. Open FMList logging page or FMDX Map
6. Remarks are automatically copied to clipboard

⸻

Current Status

v0.5.0 (Initial Public Beta)

The software is fully usable for daily FM-DX work, but additional features and UI refinements are planned.

Planned features include:

* Toast notifications
* Station search
* Site Explorer
* PI history
* DX notes
* Companion themes for FMList and FMDX Map

⸻

Author

Developed in Finland 🇫🇮 by Janne Heinikangas

* Blog: https://fmatic.online
* GitHub: https://github.com/fmatic

⸻

Philosophy

FM-DX Companion is intentionally lightweight.

It is not intended to replace SDRconnect, FMList or FMDX Maps.

Instead, it acts as a simple bridge between them, providing a faster and more efficient FM-DX workflow. 📻
