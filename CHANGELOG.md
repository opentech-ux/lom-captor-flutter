## 2.0.1

### Changed

- Package renamed from `session_recorder_flutter` to `lom_captor_flutter`.
- Updated dependency and public import to:

  ```yaml
  dependencies:
    lom_captor_flutter: ^2.0.1
  ```

  ```dart
  import 'package:lom_captor_flutter/lom_captor_flutter.dart';
  ```

- Added endpoint validation. Invalid endpoints leave the SDK in no-op mode and report the error through the configured logger.

The package rename does not change the public API or SDK behavior.

## 2.0.0

> **Breaking:** Introduced a new integration and UI capture model.

### Breaking

- New initialization API:
  `SessionRecorder.init(SessionRecorderConfig(...))`.
- `SessionRecorderWidget` is now required around the application UI.
- Requires Flutter `>=3.22.0` and Dart `>=3.4.0 <4.0.0`.
- UI capture now represents only elements visible within the application viewport.

### Added

- Visible-only UI structure capture.
- Automatic capture after relevant UI changes.
- Optional `SessionNavigatorObserver` for navigation signals.
- Optional `screenNameProvider` for complex navigation.
- Debug visualization of captured UI bounds.

### Improved

- Gesture and scroll recording.
- Navigation and lifecycle handling.
- Capture scheduling and LOM deduplication.
- Runtime CPU and memory usage.
- Session reporting reliability.

### Documentation

- Added Quick Start and updated integration examples.
- Added Data Collection & Privacy documentation.
- Added migration guidance.
- Added examples for `MaterialApp`, `MaterialApp.router`, GoRouter and obfuscated builds.