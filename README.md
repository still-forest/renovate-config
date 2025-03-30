These are my set of personal [Renovate](https://docs.renovatebot.com/) configurations.  See [Renovate documentation](https://docs.renovatebot.com/config-presets/) on using shared configs/presets.

### Guiding principles

- [Renovate's best practices](https://docs.renovatebot.com/presets-config/#configbest-practices) should be followed as a baseline.  Deviations should generally be in the form of extensions, rather than overrides.
- Automerge:
  - Packages central to CI functions (e.g., linting, testing) should be automerged to reduce volume and noise
  - All other packages should be reviewed for appropriateness prior to merge
- Grouping:
  - Packages should be grouped when they are typically released together, e.g. as part of a monorepo release.
- PR titles should follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) guidelines, i.e. be prefixed with `chore(deps):`


### Configurations

There are 4 custom/specific configurations, each inheriting from the default configuration.  In summary:

- `default`: Baseline config, centered around Typescript / React development.  It's suitable for non-React projects, as the matching & handling rules will simply not apply.
- `fastapi-react`: Adds configurations for Python package management (poetry) and grouping of [FastAPI](https://fastapi.tiangolo.com/) and [Strawberry](https://strawberry.rocks/)-related packages.
- `fullstack-js`: At present, an alias of `default`.  It's kepy separately for future usage.  e.g., to group all `nextjs` packages together
- `npm-package`: Modification of `peerDependencies` is disabled, to preserve support of older core libraries (e.g., React 18).
- `svelte`: Adds grouping of [Svelte](https://svelte.dev/) monorepo packages.

#### Features: 

<table>
<tr>
<th></th><th>default</th><th>fastapi-react</th><th>fullstack-js</th><th>npm-package</th><th>svelte</th></tr>

<tr><td colspan=6 align=center><b>Package managers</b></td></tr>
<tr><td>Javascript/Typescript</td><td colspan=5 align=center>✅ (npm / pnpm)</td></tr>
<tr><td>Python</td><td colspan=5 align=center>✅ (poetry)</td></tr>
<tr><td>Dockerfile</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Docker Compose</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>

<tr><td colspan=6 align=center><b>Grouping (presets)</b></td></tr>
<tr><td>React</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Vite</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>ES/TSLint</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>JS test</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>

<tr><td colspan=6 align=center><b>Grouping (custom)</b></td></tr>
<tr><td>Babel</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>FastAPI / Starlette / Pydantic</td><td>❌</td><td>✅</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Motion</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Prettier</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Strawberry (Python GQL)</td><td>❌</td><td>✅</td><td>❌</td><td>❌</td><td>❌</td></tr>
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
<tr><td>FastAPI / Starlette / Pydantic</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Motion</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Prettier</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Strawberry (Python GQL)</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Svelte</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
<tr><td>Types (any)</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Typescript</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Vitest</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>All others</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td><td>❌</td></tr>
</table>

### Scheduling
By default, [Renovate runs around the clock](https://docs.renovatebot.com/key-concepts/scheduling/).  To reduce noise, the configs limit this to:
- Monday-Friday: 
  - before 9am
  - *note:* lock-file maintenance only runs on Tuesdays
- Saturday/Sunday: anytime
- Singapore time, as that's where I'm currently located

There is no specific schedule for automerges, as [there may be a several hour delay](https://docs.renovatebot.com/key-concepts/automerge/).  If desired, one may be set with `automergeSchedule`.  

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
