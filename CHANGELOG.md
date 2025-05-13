# Changelog

## [0.11.0](https://github.com/still-forest/renovate-config/compare/v0.10.0...v0.11.0) (2025-04-20)

### Features

- Only patch once a week ([#43](https://github.com/still-forest/renovate-config/issues/43)) ([3bd3ffb](https://github.com/still-forest/renovate-config/commit/3bd3ffb25ee90515dfa8b6b7a7d9e0a113dc11aa))

## [0.10.0](https://github.com/still-forest/renovate-config/compare/v0.9.0...v0.10.0) (2025-04-11)

### Features

- Define schedule by version type ([#39](https://github.com/still-forest/renovate-config/issues/39)) ([ca7fbc4](https://github.com/still-forest/renovate-config/commit/ca7fbc4262fd40441c3016b8d71de183bd929ae4))

## [0.9.0](https://github.com/still-forest/renovate-config/compare/v0.8.0...v0.9.0) (2025-04-07)

### Features

- Reduce update frequency to twice per week ([#35](https://github.com/still-forest/renovate-config/issues/35)) ([6d456ef](https://github.com/still-forest/renovate-config/commit/6d456efad8e74268c0b20fc506e541e705c4d105))

## [0.8.0](https://github.com/still-forest/renovate-config/compare/v0.7.0...v0.8.0) (2025-04-06)

### Features

- Automerge testing-library/react and other /testing/ packages ([#33](https://github.com/still-forest/renovate-config/issues/33)) ([362f768](https://github.com/still-forest/renovate-config/commit/362f768144a99e57389dd2ffd5ca5a1f4883da02))

## [0.7.0](https://github.com/still-forest/renovate-config/compare/v0.6.0...v0.7.0) (2025-04-05)

### Features

- Automerge patch updates ([#31](https://github.com/still-forest/renovate-config/issues/31)) ([d7ca136](https://github.com/still-forest/renovate-config/commit/d7ca136d7ccc5838edc1a4b2b8cce3d77547c5fb))
- Use all package managers by default ([#27](https://github.com/still-forest/renovate-config/issues/27)) ([c2db62b](https://github.com/still-forest/renovate-config/commit/c2db62b08abcde21ec713ddd01f3895e0ab0d4b9))

## [0.6.0](https://github.com/still-forest/renovate-config/compare/v0.5.1...v0.6.0) (2025-03-30)

### Features

- Automerge Python linting & testing packages ([#24](https://github.com/still-forest/renovate-config/issues/24)) ([24aedbd](https://github.com/still-forest/renovate-config/commit/24aedbddfc4a18b202e50f6fa8ac6a26c47d928e))

### Bug Fixes

- Use regex to properly group eslint packages ([#25](https://github.com/still-forest/renovate-config/issues/25)) ([608f299](https://github.com/still-forest/renovate-config/commit/608f299054ee63af7f4b5cc4f15fbc74a1726161))

## [0.5.1](https://github.com/still-forest/renovate-config/compare/v0.5.0...v0.5.1) (2025-03-29)

### Minor tweaks

- Revise schedule ([#21](https://github.com/still-forest/renovate-config/issues/21)) ([7122997](https://github.com/still-forest/renovate-config/commit/71229975a711cc1ee057a67ff50483d90e243cba))

## [0.5.0](https://github.com/still-forest/renovate-config/compare/v0.4.0...v0.5.0) (2025-03-29)

### Features

- Add Github Actions, Node/NPM as enabled managers ([#18](https://github.com/still-forest/renovate-config/issues/18)) ([e7d57a4](https://github.com/still-forest/renovate-config/commit/e7d57a4c0fd62cef93a2035f0b207f4ab11f162c))
- Use custom manager presets for biome, Docker, Github actions ([#19](https://github.com/still-forest/renovate-config/issues/19)) ([4fb4918](https://github.com/still-forest/renovate-config/commit/4fb49181a9628e69d6cf079e221c15478ac23db8))

## [0.4.0](https://github.com/still-forest/renovate-config/compare/v0.3.1...v0.4.0) (2025-03-29)

### Features

- Add docker versioning ([#14](https://github.com/still-forest/renovate-config/issues/14)) ([1b846a3](https://github.com/still-forest/renovate-config/commit/1b846a3e719e9b1d2b0ad495e903cdc0c30d918f))
- Apply custom schedule for updates ([#16](https://github.com/still-forest/renovate-config/issues/16)) ([b309264](https://github.com/still-forest/renovate-config/commit/b309264ba9e10f76e53355f9ea9a65a9b0fab582))
- Pin Github Action digests ([#15](https://github.com/still-forest/renovate-config/issues/15)) ([c4449b2](https://github.com/still-forest/renovate-config/commit/c4449b2c0ef716e5a211eba5d2925d4d021c037f))

## [0.3.1](https://github.com/still-forest/renovate-config/compare/v0.3.0...v0.3.1) (2025-03-29)

### Bug Fixes

- Use latest default internally ([#7](https://github.com/still-forest/renovate-config/issues/7)) ([dd5b5cd](https://github.com/still-forest/renovate-config/commit/dd5b5cd4087a5f83414ec3c8896ae132a0f06233))

### Code Refactoring

- Additional cleanup, document Python groupings ([#12](https://github.com/still-forest/renovate-config/issues/12)) ([83c95e8](https://github.com/still-forest/renovate-config/commit/83c95e81e43c2270781a850ec3c8477537251ca6))
- Centralize JS package grouping & automerge rules ([#11](https://github.com/still-forest/renovate-config/issues/11)) ([b1293f5](https://github.com/still-forest/renovate-config/commit/b1293f5de9654cea108ecb71183034c096ee79eb))
- Centralize lockfile, PR limit options ([#9](https://github.com/still-forest/renovate-config/issues/9)) ([baefae6](https://github.com/still-forest/renovate-config/commit/baefae6f36de42e9d849c9ceea11d310ed59a361))
- Remove redundant docker enablement (enabled by default) ([#10](https://github.com/still-forest/renovate-config/issues/10)) ([48747dc](https://github.com/still-forest/renovate-config/commit/48747dc40f33953ea9c2a4538e8a6acad441d845))

## [0.3.0](https://github.com/still-forest/renovate-config/compare/0.2.0...v0.3.0) (2025-03-29)

### Features

- Consolidate preset extensions ([#5](https://github.com/still-forest/renovate-config/issues/5)) ([81f7976](https://github.com/still-forest/renovate-config/commit/81f7976527bb6611d868e3a6ee4165a2ce9edfac))
