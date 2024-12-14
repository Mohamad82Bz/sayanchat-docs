# Mention

This page covers the configuration of mention settings in SayanChat. Mention settings are used to define how player mentions are formatted and handled in the chat.

### Properties

- **enabled**: A boolean indicating whether the mention feature is enabled.
- **format**: A string representing the format of the mention. The placeholder `<username>` will be replaced with the mentioned player's name.
- **sound**: An object that defines the sound to be played when a player is mentioned. See [Sound](Sound.md) for more details.
- **cooldown**: An integer representing the cooldown period (in seconds) before a player can mention another player again.

### Example

Here is an example of a mention configuration:

```yaml
enabled: true
format: "<green>@<username></green>"
sound:
  enabled: true
  name: "ENTITY_EXPERIENCE_ORB_PICKUP"
  volume: 0.5
  pitch: 0.5
cooldown: 10
```