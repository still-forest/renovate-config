These are my set of personal [Renovate](https://docs.renovatebot.com/) configurations.  See [Renovate documentation](https://docs.renovatebot.com/config-presets/) on using shared configs/presets.


### Configurations

#### Features: 

|  | [default](default.json)  | [fastapi-react](fastapi-react.json) | [fullstack-js](fullstack-js.json) | [npm-package](npm-package.json) | [svelte](svelte.json) |
| ----- | ----- | ---- | ---- | ---- | ---- |
| Javascript/Typescript (NPM) | ✅ | ✅ | ✅ | ✅ | ✅ |
| Python (Poetry) | ❌ | ✅ |❌ |❌ |❌ |


### Usage

#### Default config only

Your renovate.json should extend this repo:
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    // latest version:
    "github>jszymanowski/renovate-config"
    // OR specific version:
    "github>jszymanowski/renovate-config#1.0.0" 
  ]
}
```

#### Specific config

Your renovate.json should specify which config to use.  The default config is included automatically.
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    // latest version:
    "github>jszymanowski/renovate-config//fastapi-react"
    // OR specific version:
    "github>jszymanowski/renovate-config//fastapi-react#1.0.0" 
  ]
}
```
