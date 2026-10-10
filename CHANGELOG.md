# Changelog

All notable changes to the **Skip Intro & Legal Messages (Straight to Story Mode)** ASI plugin will be documented in this file.

## [1.0.0] - 2026-10-10

### Initial Release

- Implemented high-performance Boyer-Moore-Horspool memory scanner.
- Added intro screens bypass (Rockstar logos, opening sirens movie) for both Legacy (`GTA5.exe`) and Enhanced (`GTA5_Enhanced.exe`).
- Added legal warnings & copyright disclaimers bypass.
- Added direct boot to Story Mode by patching the landing page check function.
- Added fallback path redirection for `platform:/movies/rockstar_logos` memory string.
- Added INI configuration support (`SkipIntroStoryMode.ini`).
- Added optional timestamped diagnostic logging (`SkipIntroStoryMode.log`).
- Automated build & deployment script (`build.ps1`).
