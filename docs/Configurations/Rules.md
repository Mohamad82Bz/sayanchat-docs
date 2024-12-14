# Rules

!!! note "If you are using Proxy"
    There is also a rules configuration in Proxy (Bungeecord/Velocity) which will be applied to all servers. You don't have to copy-paste rules in all servers, you can configure global-rules in proxy and server-specific ones in the server configuration.

This page covers the configuration of rules in SayanChat. Rules are used to control, block, or replace unwanted phrases in chat messages. They help maintain a clean and friendly chat environment by filtering out inappropriate or unwanted content.

## Configuration

The rules configuration is defined in the `rules.yml` file. The configuration file is located at `pluginDirectory/rules.yml`. Each rule has the following properties:

- **id**: A unique identifier for the rule.
- **enabled**: A boolean indicating whether the rule is enabled.
- **regex**: A regular expression used to match unwanted phrases.
- **mode**: The mode of the rule, which determines how the matched phrase is handled (e.g., `ADVERTISE`, `SWEAR`, `OTHER`).
- **ignores**: A list of phrases to ignore when applying the rule.
- **ignoreMatch**: The method used to match ignored phrases (`EQUALS` or `CONTAINS`).
- **warn**: An optional warning message to display when the rule is triggered.
- **block**: A boolean indicating whether to block the message if the rule is triggered.
- **replace**: An optional replacement string for the matched phrase.
- **flag**: The flag property is stored in the database and can be used to retrieve chat history with a specific flag (e.g., all messages that contained special characters).

### Example

Here is an example of a rules configuration:

```yaml
rules:
  - id: "url"
    enabled: false
    regex: "(https?|ftp|file)://[-A-Za-z0-9+&@#/%?=~_|!:,.;]*|[-A-Za-z0-9]+\\.[A-Za-z]{2,}\\b"
    mode: "ADVERTISE"
    ignores: ["google.com"]
    ignoreMatch: "CONTAINS"
    block: true
    flag: "url"
  - id: "somepixel"
    enabled: false
    regex: "(s+(\\W|\\d|_)*o+(\\W|\\d|_)*m+(\\W|\\d|_)*e+(\\W|\\d|_)*p+(\\W|\\d|_)*i+(\\W|\\d|_)*x+(\\W|\\d|_)*e+(\\W|\\d|_)*l+(\\W|\\d|_)*)"
    mode: "ADVERTISE"
    warn: "Please don't advertise other servers!"
    block: false
    flag: "somepixel"
  - id: "freak"
    enabled: true
    regex: "(f+(\\W|\\d|_)*r+(\\W|\\d|_)*e+(\\W|\\d|_)*a+(\\W|\\d|_)*k+(\\W|\\d|_)*)"
    mode: "SWEAR"
    replace: "freak"
    flag: "swear"
  - id: "specialcharacter"
    enabled: false
    regex: ".*[^\\da-zA-Z\\s@#\$%^&*()_+=-{};:'\"<>,./!«»()].*"
    mode: "OTHER"
    warn: "Please don't use special characters!"
    block: true
    flag: "specialcharacter"
```

!!!note
    The `enabled` property must be set to `true` for the rule to be active. It is false by default in the default configuration of the plugin.

## Rule Modes

The `mode` property of a rule determines how the matched phrase is handled. The available modes are:

- **ADVERTISE**: Used to handle advertisements.
- **SWEAR**: Used to handle swear words.
- **OTHER**: Used to handle other types of unwanted phrases.

## Ignored Phrases

The `ignores` property is a list of phrases that should be ignored when applying the rule. The `ignoreMatch` property determines how these phrases are matched:

- **EQUALS**: The phrase must match exactly.
- **CONTAINS**: The phrase must be contained within the message.

## Permissions

Players with the `sayanchat.bypass.rules` permission will not be affected by the rules.
