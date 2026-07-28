# YokeForge Changelog

This file records notable changes in public YokeForge releases.

The repository contains release information and downloadable binary packages.
The YokeForge source code is maintained separately and is not published here.

## [0.1.2]

Maintenance release focused on interface usability, tray behavior and
installer flexibility.

### Added

- Light and dark interface themes.
- In-app project support controls.
- Current-user and all-users installation modes.

### Changed

- Minor interface and usability improvements.
- Improved contextual tooltip behavior.
- A left click on the system-tray icon now toggles the YokeForge window
  between visible and hidden states, while still restoring a minimized window.

## [0.1.1]

Maintenance release focused on safer first-run defaults and interface polish.

### Changed

- English is now the default interface language on first launch.
- Automatic Microsoft Flight Simulator 2024 launch is disabled by default.
- Automatic force activation is disabled by default.
- Increased the YokeForge logo size in the navigation pane.
- Clarified the Russian force-activation confirmation label.

### Fixed

- A left click on the system-tray icon now restores and activates the YokeForge
  window directly, including when the window was minimized.

## [0.1.0]

First public release.

### Added

- Self-contained single-file Windows x64 application.
- Compact Windows 11-style WinUI 3 control panel.
- English, Russian and German user interface.
- Connection to Microsoft Flight Simulator 2024 through SimConnect.
- Force-feedback control for a custom yoke based on Microsoft SideWinder
  Force Feedback 2 hardware.
- Independent roll and pitch force handling.
- Independent Spring effect containers for the two control axes.
- Autopilot-related force-feedback control.
- Adjustable flight, aircraft, runway and ground effects.
- Individual effect enable and disable controls.
- Live adjustment of supported effect parameters.
- Device calibration workflow.
- Local user settings.
- Optional telemetry graphs.
- Application and simulator launch controls.
- System tray integration.

### Safety

- Calibration-based device travel limits.
- Separate protection for roll and pitch axes.
- Automatic force disarming when unsafe conditions are detected.
- Runtime telemetry watchdog.
- Hardware regression tests for protected force-output behaviour.

### Fixed

- Corrected Windows App SDK startup in the self-contained single-file build.
- Corrected WinRT manifest generation for single-file publishing.
- Removed obsolete manual WinRT preload logic.

### Known limitations

- Version 0.1.0 is intended for the tested custom SideWinder Force Feedback 2
  yoke configuration.
- Other force-feedback devices are not considered supported.
- The software is not certified aviation equipment.

---

Version 0.1.0 is the first public YokeForge release.
