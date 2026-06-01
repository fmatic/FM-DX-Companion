# Changelog

All notable changes to **FM-DX Companion** will be documented in this file.

The format loosely follows [Keep a Changelog](https://keepachangelog.com/), and versioning follows a practical pre-1.0 beta scheme.

---

[0.6.0] - 2026-06-01

Site Explorer Release

FM-DX Companion now includes live transmitter site exploration and direct SDRconnect tuning support.

⸻

Added

* Site Explorer
    * Show all known frequencies from the same transmitter site
    * Opens directly from station row context menu
    * Displays:
        * Frequency
        * Station
        * PI
        * PS
    * Removes duplicate entries automatically
    * Respects active mode filters
    * Smooth auto-scroll when opening
    * Close button support
* Direct SDRconnect tuning
    * Click Site Explorer rows to tune SDRconnect
    * Uses SDRconnect WebSocket API
    * Supports live VFO tuning from browser UI
    * Toast feedback for tuning actions
* Site Explorer row states
    * Current frequency highlight
    * Last tuned frequency highlight
    * Tune/play icon for clickable rows
* DX workflow improvements
    * Faster checking of related frequencies from the same site
    * Better Es and tropo workflow
    * Improved identification workflow after confirming one station

⸻

Improved

* Better panel layout
* Improved UI consistency
* Cleaner Site Explorer rendering
* Improved station deduplication logic
* Better SDRconnect interaction stability

⸻

Notes

Site Explorer is designed especially for:

* Sporadic-E openings
* Tropo openings
* Multi-frequency transmitter sites
* Fast regional band scanning

Typical workflow:

1. Identify one station
2. Open Site Explorer
3. Click other frequencies from the same site
4. Continue scanning directly through SDRconnect

⸻

Known Limitations

* Tuning currently uses only SDRconnect WebSocket support
* No keyboard tuning shortcuts yet
* No automatic “next frequency” stepping yet
* No full receiver control panel yet

⸻

Next Planned Features

* Mini tuning panel
* Previous / next site frequency buttons
* Keyboard shortcuts
* More advanced DX session workflow tools
* Session history improvements

## [0.5.2] - 2026-06-01

 Added

- Station Search
- DX Helper panel

 Improved

- Better live workflow for identifying likely stations
- More useful companion view during active DX sessions
- Search works also without SDRconnect signal

## [0.5.1] - 2026-06-01

This release focuses on stability, workflow polish and UI refinement.

New Features

* Added toast notifications for:
    * Settings saved
    * Database imports
    * FMList logging
    * Clipboard copy actions
    * FMDX Map opening
    * Error handling
* Added improved FMList workflow integration
* Added automatic remarks clipboard copy
* Added footer with author, version and project links
* Added subtle application version badge
* Added browser-side cache handling improvements

Improvements

* Improved English UI translations
* Improved FMScan userlist handling
* Improved context menu workflow
* Improved debug information readability
* Improved layout consistency and spacing
* Improved compatibility with Stylus themes
* Improved overall UI polish

Fixed

* Fixed stale PI/PS clearing behavior
* Fixed SDRconnect RDS persistence issues
* Fixed duplicate clipboard helper issue
* Fixed broken HTML structure affecting toast rendering
* Fixed multiple small UI inconsistencies

## [0.5.0.1] - 2026-05-31

Quick fix release.

## Fixed

- Improved stale RDS handling when changing frequency
- PI and PS are now cleared when tuning to a new frequency
- PI value `0000` is ignored and shown as empty
- Removed time-based RDS expiry to avoid clearing valid stable PI/PS data while listening

Recommended update for all v0.5.0 users.

## [0.5.0] - 2026-05-30

### Initial Public Beta

This is the first quiet public beta release of FM-DX Companion.

FM-DX Companion is a lightweight browser-based companion for SDRconnect and FM-DX enthusiasts. It connects live SDRconnect receiver data with FMScan userlists, FMList logging and FMDX Maps.

---

### Added

- Browser-based single-page application
- SDRconnect WebSocket integration
  - Default WebSocket endpoint: `ws://127.0.0.1:5454`
  - Live frequency tracking
  - Live PI tracking
  - Live PS tracking
- FMScan / FMSCAN userlist support
  - Tropo userlist
  - Sporadic-E userlist
  - Meteor Scatter userlist
- TAB-delimited FMScan userlist parser
- Support for locally imported userlists
- IndexedDB storage for imported userlists
  - Userlists are remembered between sessions
  - No web server required
  - No external database required
- Station matching by:
  - Frequency
  - PI code
  - PS name
- Match ranking system
- Match status labels:
  - `Confirmed`
  - `Probable`
  - `Candidate`
- Mode filters:
  - Tropo
  - Es
  - Meteor
- Optional filters:
  - Hide noRDS entries
  - Hide noPI entries
  - Require PI match if available
- Frequency tolerance setting
- FMList OM ID setting
- Custom remarks source setting
- Right-click station context menu
  - Log to FMList
  - Open FMDX Map
  - Copy FMList remarks
  - Copy station information
- FMList logging link generation
  - Uses the same basic `fi_inslog.php` workflow as existing FM-DX tools
  - Requires the user to be logged in to FMList
- Automatic FMList remarks generation
  - Example: `Logged PS: YLEYKSI, PI: 6201, via FM-DX Companion / SDRconnect`
- FMDX Maps station link support
- English user interface
- Local settings storage via `localStorage`
- Manual test mode for frequency / PI / PS testing
- Debug/status line for troubleshooting
- Version badge in the interface
- Footer with author and project links

---

### Included Companion Styling

- Optional Stylus theme for FMList logging window
  - Dark FM-DX Companion inspired color scheme
  - Improved contrast
  - Styled form fields
  - Highlighted remarks workflow
  - Companion-style visual consistency

---

### Notes

- FM-DX Companion does **not** include FMList or FMScan data.
- Each user must download their own FMScan userlists.
- Userlists remain local in the browser.
- FMList login is handled by FMList itself.
- FM-DX Companion does not store FMList credentials.
- FMList remarks are copied to clipboard instead of being injected into the FMList form.

---

### Known Limitations

- No automatic FMList logging
- No direct manipulation of FMList form fields
- No built-in station search yet
- No PI history yet
- No Site Explorer yet
- No toast notifications yet
- SDRconnect WebSocket must be enabled manually
- Browser security may limit clipboard behavior in some environments

---

## Planned

### [0.5.1]

- Toast notifications
  - Settings saved
  - Remarks copied to clipboard
  - Station info copied
  - FMList link opened
- Minor UI polish
- Better feedback for missing OM ID
- Better feedback for invalid station IDs

### [0.5.2]

- Station search
  - Search by station name
  - Search by site / city
  - Search by country
  - Search by PI
  - Search by PS
- Improved match explanation
  - Frequency match
  - PI match
  - PS match
  - PI + PS match

### [0.5.3]

- Companion themes
  - FMList logging window theme
  - FMDX Maps theme experiments
- Documentation improvements
- Screenshot and GIF demo polish

### [0.6.0]

- DX Helper panel
  - “You are probably listening to...”
  - Confidence-style match summary
  - Current best candidate
  - Confirmed station summary
- PI history
- PS history
- Session notes

### [0.7.0]

- Site Explorer
  - Show all stations from the same transmitter site
  - Show all stations from the same city / area
  - One-click tune candidates through SDRconnect if supported
- Basic tuning controls from Companion
  - Minimal receiver panel
  - Frequency step buttons
  - Possible filter controls if exposed by SDRconnect API

---

## Project Philosophy

FM-DX Companion is intentionally lightweight.

It is not intended to replace:

- SDRconnect
- FMList
- FMScan
- FMDX Maps

Instead, it acts as a simple bridge between them.

The goal is to reduce repetitive FM-DX workflow steps while keeping the final logging decision in the hands of the DXer.
