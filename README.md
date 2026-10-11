# DeadRisingVR

DeadRisingVR is an unofficial OpenXR VR mod for the PC version of **Dead Rising**.

This project is currently an **Alpha release**. It adds true stereo VR rendering, 6DoF head tracking, VR controller input, motion-based aiming and throwing, World Scale adjustment, TPS/FPS switching, and an in-VR Alpha Menu.

> **Alpha warning:** some features are experimental and some visual issues remain. Please read the setup and known-issues sections before playing.

## Disclaimer

DeadRisingVR is an unofficial fan-made VR mod for the PC version of **Dead Rising**.

Dead Rising and related trademarks and game content belong to their respective owners. DeadRisingVR is not affiliated with or endorsed by Capcom.

## Requirements

- Dead Rising on Steam
- Windows 10 or Windows 11
- A PC VR headset
- An active OpenXR runtime
- Microsoft Visual C++ Redistributable x64

## Recommended setup

The most tested configuration is:

- Meta Quest 3
- Virtual Desktop
- VDXR / OpenXR
- 3840x2160 render resolution

SteamVR / OpenXR can also be used, but support is currently considered experimental.

## IMPORTANT — Game settings

Before playing in VR, configure Dead Rising as follows:

- **Fullscreen: OFF**
- **Framerate: Variable**
- **V-Sync: OFF**

### Lock the game FPS

DeadRisingVR has been validated at:

- **72 Hz / 72 FPS**
- **80 Hz / 80 FPS**
- **90 Hz / 90 FPS**

Use an external FPS limiter and lock the game framerate to the refresh rate currently selected for your VR headset.

Examples:

- Headset at 72 Hz -> cap the game to 72 FPS
- Headset at 80 Hz -> cap the game to 80 FPS
- Headset at 90 Hz -> cap the game to 90 FPS

You can use the NVIDIA Control Panel, RivaTuner Statistics Server (RTSS), or another reliable FPS limiter.

If the game framerate is not locked to the headset refresh rate, noticeable judder can occur.

## OpenXR runtime

DeadRisingVR requires an active OpenXR runtime.

### Virtual Desktop / VDXR — recommended

For Quest headsets with Virtual Desktop:

1. Select **VDXR** as the active OpenXR runtime.
2. Start Virtual Desktop.
3. Launch `DeadRisingVRLauncher.exe`.
4. Accept the Windows UAC prompt.

### Steam Link / SteamVR — experimental

When using Steam Link / SteamVR:

1. Make sure **SteamVR is selected as the active OpenXR runtime**.
2. Start SteamVR completely before launching DeadRisingVR.
3. Launch `DeadRisingVRLauncher.exe`.

If SteamVR is not configured as the active OpenXR runtime, the game can launch in normal 2D mode even if the mod DLL has loaded.

The 3840x2160 SteamVR/OpenXR rendering path has been validated.

## Installation

1. Download the latest DeadRisingVR Alpha ZIP from **GitHub Releases**.
2. Extract the ZIP anywhere.
3. Double-click `Install.bat`.
4. Accept Windows UAC if requested.
5. Select the folder containing `DeadRising.exe` if requested.

The installer places the DeadRisingVR runtime files beside `DeadRising.exe`.

Player settings and logs are stored separately in:

`%LOCALAPPDATA%\DeadRisingVR`

## Launching

Do **not** use the normal Steam Play button to launch the VR mod.

Open the Dead Rising installation folder and double-click:

`DeadRisingVRLauncher.exe`

Accept the Windows UAC prompt.

The launcher starts Dead Rising through Steam and loads the VR mod.

## Controls

| Input | Action |
| --- | --- |
| Right index trigger | Attack / take photo |
| Right grip | Aim weapon / throwing gesture |
| Right grip + R3 while aiming | Mark a destination for Survivors (Ctrl+A) |
| A | Jump / contextual confirm |
| B | Inventory next / contextual back |
| Left index trigger | Interact / use / talk |
| Left grip | Photo camera |
| L3 | Use Walkie-talkie |
| R3 | Call Survivors |
| L3 + R3 or F9 | Toggle TPS/FPS |
| X short press | Check Watch |
| X long press or F7 | Toggle Alpha Menu |
| Y short press | Check Map |
| Y long press | Pause menu |
| Left stick | Move / contextual navigation |
| Right stick | Move camera |

### Photo camera controls

While using the photo camera:

- **B**: zoom-in
- **A**: zoom-out

### Map controls

While viewing the map:

- **B**: zoom-in
- **A**: zoom-out

## Alpha Menu

Open or close the Alpha Menu with:

- **X long press**
- **F7**

Keyboard navigation:

- **Up Arrow**: previous item
- **Down Arrow**: next item
- **Enter**: confirm
- **F7**: close menu

`Escape` remains the native Dead Rising Pause/Menu key.

### Cheats

The current Alpha Menu can spawn:

- Handgun
- SMG
- Shotgun
- Machinegun
- Katana
- Fire Axe

### World Scale

World Scale can be adjusted from the Alpha Menu.

Available values:

- 50%
- 75%
- 100%
- 125%
- 150%

Default: **100%**

Increasing the percentage makes the world appear smaller.

## First-person mode

First-person mode is **experimental**.

Use:

- **L3 + R3**
- or **F9**

to toggle between third-person and first-person modes.

Third-person mode remains the recommended/default way to play. FPS mode may show visual, animation, or camera issues that are not present in TPS.

## Known issues / Alpha limitations

- **Shadows do not render correctly in VR in some situations.**
- **First-person mode is experimental.**
- **Occasional judder can still occur**, even with correct frame pacing.
- Incorrect FPS / headset-refresh matching can cause much more noticeable judder.
- During the helicopter photography introduction, pressing **B** may skip directly toward the rooftop sequence.
- SteamVR/OpenXR support is currently experimental/partial.
- Under SteamVR/OpenXR, the F7 Alpha Menu can display a rectangular portion of the game instead of the menu.
- Large intermittent freezes were observed during some Steam Link testing. Their cause has not been proven to be DeadRisingVR.

## Performance tips

For smooth VR:

1. Fullscreen: **OFF**
2. Framerate: **Variable**
3. V-Sync: **OFF**
4. Lock the game FPS to the headset refresh rate

Validated targets:

- 72 Hz / 72 FPS
- 80 Hz / 80 FPS
- 90 Hz / 90 FPS

## Troubleshooting

### The game launches in 2D

Check these first:

1. Make sure an OpenXR runtime is active.
2. With Virtual Desktop, select **VDXR**.
3. With Steam Link / SteamVR, make sure **SteamVR is selected as the active OpenXR runtime**.
4. Start the VR runtime before launching the mod.
5. Launch `DeadRisingVRLauncher.exe`, not the normal Steam Play button.
6. Accept the Windows UAC prompt.

### The game judders

Check:

- Fullscreen = OFF
- Framerate = Variable
- V-Sync = OFF
- Game FPS cap = headset refresh rate

## Antivirus notice

DeadRisingVR uses DLL injection to load the VR mod into Dead Rising.
Because of this, some antivirus engines may report a heuristic or generic detection.

The official Alpha v0.1.0 ZIP SHA-256 is:

`DCF2EB3317E32802473C04FA793082EF1870A97730DA33672C8CD08765B4084D`

Only download DeadRisingVR from the official GitHub repository.

## Diagnostics

When reporting a problem, double-click:

`Collect-Diagnostics.bat`

The diagnostics package collects DeadRisingVR-related logs, configuration, hashes, and relevant system/runtime information for troubleshooting.

## Uninstall

Double-click:

`Uninstall.bat`

Player configuration stored under:

`%LOCALAPPDATA%\DeadRisingVR`

is preserved by default.

## Status

DeadRisingVR is an early Alpha project. Compatibility, input behavior, rendering, and installation procedures may change as testing continues.
