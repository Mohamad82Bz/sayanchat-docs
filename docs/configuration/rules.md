# rules.yml

Regex-based chat filters. Each rule can warn, block, and notify staff.

## Key Options

- `settings.replace-swear`: String replacement for swear mode.
- `settings.return-on-first-blocking`: Stop after first blocking rule.
- `rules`: List of rule objects.

Rule object fields:

- `id`: Unique id
- `enabled`: Enable/disable
- `regex`: Regex pattern
- `mode`: `SWEAR`, `ADVERTISE`, `OTHER`
- `mode-display`: Display label
- `mode-alias`: Short alias
- `ignores`: List of ignored strings
- `ignore-match`: `CONTAINS`, `EQUALS`, etc
- `warn`: Warning message
- `block`: Block message if true
- `flag`: Flag label used in history
- `notify`: Send to notify chat box

## Example

```yaml
settings:
  replace-swear: '****'
  return-on-first-blocking: true
rules:
- id: url
  enabled: false
  regex: (https?|ftp|file)://[-A-Za-z0-9+&@#/%?=~_|!:,.;]*|[-A-Za-z0-9]+\.[A-Za-z]{2,}\b
  mode: ADVERTISE
  mode-display: <yellow>Advertise
  mode-alias: advertise
  ignores:
  - google.com
  ignore-match: CONTAINS
  warn: ''
  block: true
  flag: advertise
  notify: true
```
