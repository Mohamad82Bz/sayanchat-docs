# Announces

This guide covers the configuration and usage of announcements in SayanChat.

!!! note
    All formats in this documentation use Adventure MiniMessage. For a guide on how to use the format, please refer to [MiniMessage Documentation](https://docs.advntr.dev/minimessage/index.html).

## Command Usage

To use the announcement command, you need to provide a message that must be quoted with double quotations. The command also supports several flags to modify its behavior:

- **global** or **g**: This flag indicates that the announcement should be broadcast globally to all players.
- **preview** or **p**: This flag allows you to preview the announcement. The preview will only be visible to the player who issued the command.
- **raw** or **r**: This flag indicates that the message should be sent without any formatting.

### Example

Here is an example of how to use the announcement command:

```plaintext
/announcement "This is a test announcement" --global
```

In this example, the message "This is a test announcement" will be broadcast globally to all players.

Another example with the preview flag:

```plaintext
/announcement "This is a preview announcement" --preview
```

In this example, the message "This is a preview announcement" will only be visible to the player who issued the command.

Using the raw flag:

```plaintext
/announcement "This is a raw announcement" --raw
```

In this example, the message "This is a raw announcement" will be sent without any formatting.

## Configuration

The announcements configuration is defined in the `announces.yml` file. The configuration file is located at `pluginDirectory/announces.yml`.

### Announcement Configuration

```yaml
announcement:
  header:
    - "<st>                                                </st>"
  footer:
    - "<st>                                                </st>"
  prefix: "<gold>> <reset>"
  suffix: ""
  sound:
    enabled: true
    name: "ENTITY_EXPERIENCE_ORB_PICKUP"
    volume: 1.0
    pitch: 1.2
```

- **header**: A list of strings that will be displayed at the top of each announcement.
- **footer**: A list of strings that will be displayed at the bottom of each announcement.
- **prefix**: A string that will be prefixed to each line of the announcement.
- **suffix**: A string that will be suffixed to each line of the announcement.
- **sound**: An object that defines the sound to be played when an announcement is made. See [Sound](Objects/Sound.md) for more details.

### AutoAnnounce Configuration

```yaml
auto-announce:
  enabled: false
  random: false
  interval: 900
  sound:
    enabled: true
    name: "ENTITY_EXPERIENCE_ORB_PICKUP"
    volume: 1.0
    pitch: 1.2
  header:
    - "<st>                                                </st>"
    - "<st>                                                </st>"
  footer:
    - "<st>                                                </st>"
    - "<st>                                                </st>"
  announces:
    - "<gold>You can buy ranks on <underlined><click:open_url:'https://www.examplemc.net'>our website"
    - "<gold>Join our discord server <underlined><click:open_url:'https://discord.gg/example'>here"
    - "<gold>Don't forget to vote for us on <underlined><click:open_url:'https://www.examplemc.net/vote'>our website"
```

- **enabled**: A boolean indicating whether automatic announcements are enabled.
- **random**: A boolean indicating whether the announcements should be made in random order.
- **interval**: An integer representing the interval (in seconds) between automatic announcements.
- **header**: A list of strings that will be displayed at the top of each automatic announcement.
- **footer**: A list of strings that will be displayed at the bottom of each automatic announcement.
- **announces**: A list of strings, each representing an announcement message.
- **sound**: An object that defines the sound to be played when an automatic announcement is made. See [Sound](Objects/Sound.md) for more details.