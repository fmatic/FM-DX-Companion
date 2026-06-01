# FM-DX Companion

![Version](https://img.shields.io/badge/version-v0.5.1-blue)
![Status](https://img.shields.io/badge/status-beta-orange)
![Platform](https://img.shields.io/badge/platform-browser-green)

A lightweight browser-based companion for SDRconnect and FM-DX enthusiasts.

FM-DX Companion combines FMScan userlists, SDRconnect WebSocket data, FMList logging and FMDX Maps into a streamlined DX workflow.

---

## Screenshot

![FM-DX Companion](docs/screenshot.jpg)

## Features

- Real-time SDRconnect integration via WebSocket
- PI and PS based station matching
- Supports FMScan Tropo, Sporadic-E and Meteor Scatter userlists
- FMList logging integration
- FMDX Maps integration
- Automatic remarks generation
- Browser-based, no installation required
- IndexedDB local storage
- Fast station lookup and ranking

---

## Getting Started

### 1. Enable SDRconnect WebSocket Server

Default connection:

```text
ws://127.0.0.1:5454
```

### 2. Download FMScan Userlists

Download all three FMScan userlists:

- Tropo
- Sporadic-E
- Meteor Scatter

Export settings:

- CSV format
- TAB separator

![FMScan Export Settings](https://raw.githubusercontent.com/fmatic/FM-DX-Companion/main/docs/IMG_5188.gif)

### 3. Rename Files

Rename the downloaded files:

```text
tropo.csv
es.csv
meteor.csv
```

### 4. Import Lists

Load the files into FM-DX Companion:

| List | File |
|--------|--------|
| Tropo | tropo.csv |
| Es | es.csv |
| Meteor | meteor.csv |

The lists are stored locally in your browser and automatically restored when Companion is reopened.

### 5. FMList Login

To use FMList logging, you must be logged into FMList in the same browser.

Companion opens the FMList logging page directly and copies remarks to the clipboard automatically, but FMList authentication is handled by FMList itself.

If you are not logged in, FMList will redirect you to the login page.

---

## Typical Workflow

1. Tune a station in SDRconnect
2. Companion receives Frequency, PI and PS data
3. Matching stations are ranked automatically
4. Right-click a station entry
5. Open FMList logging or FMDX Maps
6. Remarks are automatically copied to clipboard
7. Log the station

---

## Current Status

### v0.5.0.1

Quick fix release.

## Fixed

- Old PS values no longer remain visible after changing frequency
- PI value `0000` is now ignored and shown as empty
- Fixed stale RDS data handling when changing frequency. PI value 0000 is ignored.


## Notes

This release improves reliability while tuning quickly across the FM band.

Recommended update for all v0.5.0 users.

### v0.5.0 — Initial Public Beta

FM-DX Companion is already fully usable for everyday FM-DX work.

### Planned Features

- Toast notifications
- Station search
- Site Explorer
- PI history
- DX notes
- FMList Companion Theme
- FMDX Maps Companion Theme

---

## Philosophy

FM-DX Companion is intentionally lightweight.

It is **not intended to replace SDRconnect, FMList or FMDX Maps**.

Instead, it acts as a bridge between them, providing a faster and more efficient FM-DX workflow while keeping the interface simple and distraction-free.

---

## Author

**Janne Heinikangas** 🇫🇮

- Blog: https://fmatic.online
- GitHub: https://github.com/fmatic

---

*Minimal DX workflow for SDRconnect users.*
