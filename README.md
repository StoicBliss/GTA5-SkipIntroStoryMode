# Skip Intro & Legal Messages - Straight to Story Mode (GTA V ASI Mod)

A fast, lightweight, and modern C++ ASI plugin for Grand Theft Auto V that skips the opening Rockstar logos, siren intro animation, and legal warning screens, and loads straight into Story Mode without stopping at the landing page / main menu.

## Features

- **Skip Intro Videos**: Bypasses the Rockstar North / Rockstar Games intro cinematics and siren sequences.
- **Skip Legal Messages**: Bypasses the copyright disclaimer and legal warning screens.
- **Straight to Story Mode**: Patches the landing page check so the game boots directly into Story Mode loading screens instead of halting at the landing menu.
- **Enhanced & Legacy Support**: Compatible with both `GTA5.exe` (Legacy builds) and `GTA5_Enhanced.exe` (Enhanced edition).
- **Graceful Safeguards**: Never crashes or shows fatal popups if a pattern changes in a game update; includes fallback string redirection for `platform:/movies/rockstar_logos`.
- **Configurable INI**: Every feature can be toggled on or off independently in `SkipIntroStoryMode.ini`.
- **Zero Performance Overhead**: Patches memory during initialization and uses 0% CPU while playing.

---

## Installation

1. Make sure you have an ASI Loader installed (such as `dinput8.dll`, typically included with [Script Hook V](http://www.dev-c.com/gtav/scripthookv/)).
2. Place `SkipIntroStoryMode.asi` and `SkipIntroStoryMode.ini` into your root **Grand Theft Auto V** game folder (where `GTA5.exe` is located).
3. Start the game. The game will now skip all intro screens and load directly into Story Mode.

---

## Configuration (`SkipIntroStoryMode.ini`)

```ini
[Features]
; Skip the Rockstar Games logos and intro siren animation
; 1 = Enabled (Fast launch), 0 = Disabled
SkipIntro = 1

; Skip the legal warning and copyright disclaimer screen
; 1 = Enabled (Instant skip), 0 = Disabled
SkipLegal = 1

; Skip the landing page / main menu and boot directly into Story Mode
; 1 = Enabled (Straight to Story Mode), 0 = Disabled (Show landing page)
StraightToStoryMode = 1

; Overwrite the internal movie path "platform:/movies/rockstar_logos" in memory
; Serves as an extra safeguard if the byte signature fails on updated builds
; 1 = Enabled, 0 = Disabled
FallbackLogoString = 1

[Logging]
; Write diagnostic status and memory addresses to a log file
; 1 = Enabled, 0 = Disabled
EnableLogging = 1

; Name of the output log file (saved next to the .asi file)
LogFileName = SkipIntroStoryMode.log
```

---

## Compilation

Run the PowerShell build script:

```powershell
.\build.ps1
```

To build and package into a release zip in `dist`:

```powershell
.\build.ps1 -Package
```

---

## Disclaimer

This mod is designed exclusively for **Single-Player (Story Mode)**. As with any mod or ASI plugin, remove all mod files before playing GTA Online.


## Download & Releases

Download the latest compiled release from [GitHub Releases](https://github.com/StoicBliss/GTA5-SkipIntroStoryMode/releases/latest).

Each release includes:
- `SkipIntroStoryMode.asi` (native 64-bit ASI plugin)
- `SkipIntroStoryMode.ini` (default configuration)
- `SkipIntroStoryMode_Release.zip` (complete release archive)