# YokeForge Changelog

This file records notable changes in public YokeForge releases.

The repository contains release information and downloadable binary packages.
The YokeForge source code is maintained separately and is not published here.

## [0.1.6]

Feature release focused on manual-control feel, live force feedback and trim
behavior.

### Added

- Live manual-force status indicators for:
  - airspeed contribution;
  - resulting X/Y stiffness;
  - damping;
  - propeller loading on Y;
  - pitch and roll trim;
  - force-neutral target and actual physical yoke position.
- Independent X and Y trim-influence controls.
- Live roll-trim support when the aircraft/runtime provides that telemetry.
- Step-by-step manual-force setup guide in English, Russian and German.

### Changed

- Manual X and Y control loading can now be tuned independently.
- Refined airspeed loading on the pitch axis for a more natural manual-control
  feel.
- Propeller loading on Y is now adjustable independently from airspeed loading.
- The autopilot setup guide now includes a short Y-axis tuning check while
  keeping the existing X-axis workflow unchanged.
- Expanded and clarified user-facing setting tooltips and setup guidance.

### Fixed

- Removed hidden manual-trim target caps that could limit available trim-neutral
  movement.
- Corrected the automatic force-activation readiness gate.
- Optional roll-trim telemetry no longer has to be part of the mandatory
  SimConnect data set.

### Safety

- This release intentionally changes manual-control loading and trim behavior.
- Autopilot force calculations, calibration, travel protection, watchdog and
  DISARM safety logic remain unchanged.
- The independent roll and pitch Spring containers remain separate.

## [0.1.5]

Feature release focused on clearer system-tray status and persistent
controller tuning.

### Added

- Color-coded system-tray status indicator:
  - gray while waiting for Microsoft Flight Simulator 2024;
  - green when telemetry, device connection and force output are ready;
  - red when YokeForge reports an active fault.
- Status-specific system-tray tooltips.

### Changed

- Controller tuning values, effect checkboxes and the general autopilot-effects
  switch are now saved automatically.
- Settings loaded from an exported INI file now remain active after restarting
  YokeForge.
- Restoring accepted defaults now also updates the persistent controller
  settings.

### Fixed

- Controller tuning sliders no longer return to their accepted defaults after
  YokeForge is restarted.

### Safety

- This release does not change force-feedback calculations, DirectInput force
  behavior, SimConnect telemetry, calibration, travel protection, hardware
  safety or the independent roll and pitch Spring containers.

## [0.1.4]

Feature release focused on autopilot tuning feedback, application lifecycle,
portable interface preferences and verified in-app updates.

### Added

- Live autopilot roll monitor showing the cockpit command, calculated target,
  physical yoke position and recorded peak travel.
- Contextual autopilot tuning guide in English, Russian and German.
- Manual update checks and an optional check when YokeForge starts.
- Confirmed update download flow that selects the exact published installer,
  verifies its GitHub-provided SHA-256 digest and launches the normal
  interactive installer.
- YokeForge-managed interface preferences in exported settings files; loading
  such a file now restores the saved interface checkboxes.

### Changed

- YokeForge now closes after Microsoft Flight Simulator 2024 exits only when
  that simulator session was launched by the current YokeForge session.
- Update downloads are stored under the current user's local application data.
- Active force output is stopped before a verified update installer is
  launched.
- Refined update-card and settings tooltip behavior.

### Fixed

- Exported settings now preserve all YokeForge interface checkbox states.
- The update-card tooltip no longer appears over unrelated empty card space.

### Safety

- Update installers are never launched unless the expected filename and
  SHA-256 digest match the published release metadata.
- Updates require explicit confirmation and are never installed silently.
- This release does not change force-feedback calculations, DirectInput force
  behavior, SimConnect telemetry, calibration, travel protection, hardware
  safety or the independent roll and pitch Spring containers.

## [0.1.3]

Maintenance release focused on single-instance startup and reliable window
activation.

### Fixed

- Prevented multiple YokeForge processes and system-tray icons when the
  application is launched more than once.
- A repeated launch now restores and activates the existing YokeForge window
  instead of opening another application instance.
- Restoring the window through the system-tray icon now reliably brings it to
  the foreground.

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
