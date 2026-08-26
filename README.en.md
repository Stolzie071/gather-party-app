<div align="center">
  <img src="assets/branding/app-icon.png" width="150" alt="Gather app icon" />

  # Gather

  **An offline party-game companion focused on polished UX, responsive layouts, and local-first play.**

  [![Version](https://img.shields.io/badge/version-1.0.0-9B73E6?style=flat-square)](https://github.com/Stolzie071/gather-party-app/releases/latest)
  [![Android](https://img.shields.io/badge/Android-7.0%2B-3DDC84?style=flat-square&logo=android&logoColor=white)](https://github.com/Stolzie071/gather-party-app/releases/latest)
  [![React Native](https://img.shields.io/badge/React_Native-0.81-20232A?style=flat-square&logo=react&logoColor=61DAFB)](#tech-stack)
  [![Expo](https://img.shields.io/badge/Expo_SDK-54-000020?style=flat-square&logo=expo&logoColor=white)](#tech-stack)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?style=flat-square&logo=typescript&logoColor=white)](#tech-stack)

  [Русская версия](README.md) · [Download APK](https://github.com/Stolzie071/gather-party-app/releases/latest) · [Architecture](docs/ARCHITECTURE.md) · [Privacy](docs/PRIVACY.md)
</div>

## About

Gather turns one phone into a companion for in-person party games. Version 1.0 ships a complete **Spy** experience: configure a party, privately reveal roles, run the timer, choose winners, and keep local player statistics — without accounts, a backend, or an internet connection.

The project was designed and built independently from initial Figma concepts through responsive React Native implementation, native Android release preparation, performance tuning, and device testing.

## Highlights

- Complete Spy game flow for 3–12 players and one or multiple spies.
- Built-in and user-created word packs; several packs can be combined into one game.
- 62 illustrated locations across Nature, Entertainment, and Cities.
- Persistent players with preset avatars or cropped personal photos.
- Configurable timer, spy count, and whether spies know each other.
- Role distribution, teammate hints, leave protection, winner selection, and haptic feedback.
- Local game history, player profiles, search, filters, sorting, and performance statistics.
- Responsive layouts tested on small and large Android screens.
- Russian and English interface localization.
- Alias and Mafia are presented in the catalog as future games.

## Screenshots

<table>
  <tr>
    <td align="center"><img src="assets/screenshots/main_screen.jpg" width="210" alt="Gather home screen"><br><sub>Home</sub></td>
    <td align="center"><img src="assets/screenshots/spy_game.jpg" width="210" alt="Spy game screen"><br><sub>Spy</sub></td>
    <td align="center"><img src="assets/screenshots/spy_settings.jpg" width="210" alt="Game setup"><br><sub>Game setup</sub></td>
    <td align="center"><img src="assets/screenshots/player_card.jpg" width="210" alt="Private role reveal"><br><sub>Role reveal</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="assets/screenshots/timer.jpg" width="210" alt="Game timer"><br><sub>Game timer</sub></td>
    <td align="center"><img src="assets/screenshots/stats.jpg" width="210" alt="Statistics overview"><br><sub>Statistics</sub></td>
    <td align="center"><img src="assets/screenshots/player_stats.jpg" width="210" alt="Player statistics"><br><sub>Player profile</sub></td>
    <td align="center"><img src="assets/screenshots/settings.jpg" width="210" alt="Application settings"><br><sub>Settings</sub></td>
  </tr>
</table>

## Spy game flow

1. Select a category and one or more built-in or custom packs.
2. Pick saved players or create new profiles with an avatar or photo.
3. Configure the number of spies, timer, and teammate visibility.
4. Pass the phone around while each player privately reveals their role.
5. Play with or without a timer, then select one or more winners.
6. Review the saved match and updated player statistics.

## Engineering highlights

- **Local-first data model:** settings, players, custom packs, active game state, history, and statistics are stored on the device.
- **Reusable game architecture:** shared navigation, cards, dialogs, controls, transitions, player management, and storage are separated from Spy-specific rules and content.
- **Release optimization:** the ARM64 APK was reduced from approximately **190.84 MB to 33.55 MB**; the universal APK is **82.12 MB**.
- **Asset optimization:** 62 location images were reduced from **113.44 MB to 5.32 MB** while preserving their in-app quality.
- **Quality checks:** the project currently passes **35 automated tests across 7 suites**, alongside manual testing on physical devices and multiple screen sizes.
- **Native release:** Android shrinking and obfuscation are enabled, and releases use a persistent signing key so future versions can update the installed app.

## Tech stack

| Area | Technology |
| --- | --- |
| Application | React Native 0.81, React 19, Expo SDK 54, TypeScript 5.9 |
| Navigation | React Navigation 7, native stack, custom screen transitions |
| Motion & gestures | Reanimated 4, Gesture Handler |
| Persistence | AsyncStorage and app-managed local files |
| Device integrations | Image Picker, Image Manipulator, Media Library, Haptics, Keep Awake, Localization |
| Graphics | SVG assets and optimized raster illustrations |
| Quality | Jest, jest-expo, ESLint, TypeScript |
| Android release | Gradle, R8 code shrinking, resource shrinking, permanent signing |

More detail is available in the high-level [architecture overview](docs/ARCHITECTURE.md).

## Download

Download the latest APK from [GitHub Releases](https://github.com/Stolzie071/gather-party-app/releases/latest):

- **ARM64 APK** — recommended for most modern Android phones; smaller download.
- **Universal APK** — fallback for devices with a different CPU architecture.

Minimum supported version: **Android 7.0 (API 24)**. Because the app is distributed outside Google Play, Android may ask you to allow installation from the browser or file manager used to open the APK.

## Privacy

Gather does not require an account and does not send gameplay or player data to a server. Player profiles, photos, custom packs, history, and settings remain on the device. Photo and media permissions are requested only when the related feature is used. See the [privacy overview](docs/PRIVACY.md).

## Project status

Version 1.0 is a portfolio-ready Android release centered on the Spy game. Planned work includes game rules, sound and music, dark theme, expanded content, and fully playable Alias and Mafia modes.

## Source availability

This public repository intentionally contains the product presentation and release information, not the proprietary application source code or original design files. The private codebase can be demonstrated during a technical interview on request.

## Author

Designed and developed by **Tony** — [@Stolzie071](https://github.com/Stolzie071).

See [NOTICE.md](NOTICE.md) for usage restrictions.
