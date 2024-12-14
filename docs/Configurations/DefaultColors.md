# Default Colors

This page covers the configuration of default colors in SayanChat. A default color is a color that will be applied to a player's message.

## Command Usage

To use the default color command, you need to provide the color id. The command supports the following arguments:

- **color**: The color to be set as the default.
- **player**: The player for whom the default color is being set.

### Examples

Here are examples of how to use the default color command:

```plaintext
/defaultcolor <color>
```

In this example, the command sets the default color for the player issuing the command.

```plaintext
/defaultcolor set <player> <color>
```

In this example, the command sets the default color for the specified player.

## Configuration

The default colors configuration is defined in the `defaultcolors.yml` file. The configuration file is located at `pluginDirectory/defaultcolors.yml`.

- **id**: A unique identifier for the color. This is used in the default color command.
- **tag**: The MiniMessage tag representing the color.

## Permissions

Default color permissions are used to control which players can use specific default colors. The permission format is:

```plaintext
sayanchat.defaultcolor.<id>
```

Where `<id>` is the unique identifier for the color. For example, to allow a player to use the "gold" color, you would grant them the `sayanchat.defaultcolor.gold` permission.

### Example

Here is an example of a default color configuration:

```yaml
defaultColors:
  - id: "gray"
    tag: "<gray>"
  - id: "gold"
    tag: "<gold>"
  - id: "dark_green"
    tag: "<dark_green>"
  - id: "yellow"
    tag: "<yellow>"
  - id: "blue"
    tag: "<blue>"
  - id: "white"
    tag: "<white>"
  - id: "green"
    tag: "<green>"
  - id: "red"
    tag: "<red>"
  - id: "light_purple"
    tag: "<light_purple>"
  - id: "dark_aqua"
    tag: "<dark_aqua>"
  - id: "aqua"
    tag: "<aqua>"
  - id: "blue_gradient"
    tag: "<gradient:aqua:blue>"
  - id: "green_gradient"
    tag: "<gradient:green:dark_green>"
  - id: "purple_gradient"
    tag: "<gradient:light_purple:dark_purple>"
  - id: "rainbow"
    tag: "<rainbow>"
```

!!! note
    All formats in this documentation use Adventure MiniMessage. For a guide on how to use the format, please refer to [MiniMessage Documentation](https://docs.advntr.dev/minimessage/index.html).