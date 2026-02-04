# announces.yml

Controls manual and automatic announcements.

## Example

```yaml
announcement:
  header:
  - <st>                                                </st>
  footer:
  - <st>                                                </st>
  prefix: <gold>> <reset>
  suffix: ''
  sound:
    enabled: true
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.2
auto-announce:
  enabled: false
  random: false
  interval: 900
  sound:
    enabled: true
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.2
  header:
  - <st>                                                </st>
  - <st>                                                </st>
  footer:
  - <st>                                                </st>
  - <st>                                                </st>
  announces:
  - <gold>You can buy ranks on <underlined><click:open_url:'https://www.examplemc.net'>our website
  - <gold>Join our discord server <underlined><click:open_url:'https://discord.gg/example'>here
  - <gold>Don't forget to vote for us on <underlined><click:open_url:'https://www.examplemc.net/vote'>our website
```
