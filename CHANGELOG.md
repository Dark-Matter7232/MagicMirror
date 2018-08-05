# SmartMirror Change Log

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

---

## [0.1] - 2018-07-04

### Fixed

- Fix weather parsing issue #1332.

## [2.4.0] - 2018-07-01

⚠️ **Warning:** This release includes an updated version of Electron. This requires a Raspberry Pi configuration change to allow the best performance and prevent the CPU from overheating. Please read the information on the [MagicMirror Wiki](https://github.com/michmich/magicmirror/wiki/configuring-the-raspberry-pi#enable-the-open-gl-driver-to-decrease-electrons-cpu-usage).

ℹ️ **Note:** This update uses new dependencies. Please update using the following command: `git pull && npm install`

### Added

- Enabled translation of feelsLike for module currentweather
- Added support for on-going calendar events
- Added scroll up in fullscreen newsfeed article view
- Changed fullscreen newsfeed width from 100% to 100vw (better results)
- Added option to calendar module that colors only the symbol instead of the whole line
- Added option for new display format in the calendar module with date headers with times/events below.
- Ability to fetch compliments from a remote server
- Add regex filtering to calendar module
- Customize classes for table
- Added option to newsfeed module to only log error parsing a news article if enabled
- Add update translations for Português Brasileiro

### Changed
- Upgrade to Electron 2.0.0.
- Remove yarn-or-npm which breaks production builds.
- Invoke module suspend even if no dom content. [#1308](https://github.com/MichMich/MagicMirror/issues/1308)

### Fixed
- Fixed issue where wind chill could not be displayed in Fahrenheit. [#1247](https://github.com/MichMich/MagicMirror/issues/1247)
- Fixed issues where a module crashes when it tries to dismiss a non existing alert. [#1240](https://github.com/MichMich/MagicMirror/issues/1240)
- In default module currentWeather/currentWeather.js line 296, 300, self.config.animationSpeed can not be found because the notificationReceived function does not have "self" variable.
- Fixed browser-side code to work on the Midori browser.
- Fixed issue where heat index was reporting incorrect values in Celsius and Fahrenheit. [#1263](https://github.com/MichMich/MagicMirror/issues/1263)
- Fixed weatherforecast to use dt_txt field instead of dt to handle timezones better
- Newsfeed now remembers to show the description when `"ARTICLE_LESS_DETAILS"` is called if the user wants to always show the description. [#1282](https://github.com/MichMich/MagicMirror/issues/1282)
- `clientonly/*.js` is now linted, and one linting error is fixed
- Fix issue #1196 by changing underscore to hyphen in locale id, in align with momentjs.
- Fixed issue where heat index and wind chill were reporting incorrect values in Kelvin. [#1263](https://github.com/MichMich/MagicMirror/issues/1263)

### Updated
- Updated Italian translation
- Updated German translation
- Updated Dutch translation
