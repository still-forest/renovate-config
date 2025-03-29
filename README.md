These are my set of personal [Renovate](https://docs.renovatebot.com/) configurations.  See [Renovate documentation](https://docs.renovatebot.com/config-presets/) on using shared configs/presets.


### Configurations

#### Features: 

<table>
<tr>
<th></th><th>default</th><th>fastapi-react</th><th>fullstack-js</th><th>npm-package</th><th>svelte</th></tr>

<tr><td colspan=6 align=center><b>Package managers</b></td></tr>
<tr><td>Javascript/Typescript</td><td colspan=5 align=center>✅ (npm / pnpm)</td></tr>
<tr><td>Python</td><td colspan=5 align=center>✅ (poetry)</td></tr>
<tr><td>Dockerfile</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Docker Compose</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>

<tr><td colspan=6 align=center><b>Grouping (presets)</b></td></tr>
<tr><td>React</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Vite</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>ES/TSLint</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>JS test</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>

<tr><td colspan=6 align=center><b>Grouping (custom)</b></td></tr>
<tr><td>Babel</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Prettier</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Svelte</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>✅</td></tr>
<tr><td>Types (any)</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Typescript</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Vitest</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>

<tr><td colspan=6 align=center><b>Timing, pacing</b></td></tr>
<tr><td>PR limits</td><td colspan=5 align=center>10 per hour, 20 total open</td></tr>
<tr><td>Lock-file maintenance</td><td colspan=5 align=center>Every tuesday before 5am</td></tr>
<tr><td>Delay (npm)</td><td colspan=5 align=center>3 days after publishing</td></tr>
<tr><td>Delay (other)</td><td colspan=5 align=center>None</td></tr>

<tr><td colspan=6 align=center><b>Pull requests</b></td></tr>
<tr><td>PR limits</td><td colspan=5 align=center>10 per hour, 20 total open</td></tr>


<tr><td colspan=6 align=center><b>Automerge</b></td></tr>
<tr><td>Lock-file maintenance</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Babel</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>ESLint</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Prettier</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Svelte</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Types (any)</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Typescript</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Vitest</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>All others</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
</table>


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
