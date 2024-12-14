# Toast

This page covers the configuration of toast settings in SayanChat. Toast settings are used to define how toast notifications are formatted and displayed in the chat.

### Properties

- **enabled**: A boolean indicating whether the toast feature is enabled.
- **icon**: A `Material` object representing the icon to be displayed with the toast notification. See the [Material List](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html) for available options.
- **format**: A string representing the format of the toast notification. The placeholder `<username>` will be replaced with the player's name, and `<message>` will be replaced with the message content.

### Example

Here is an example of a toast configuration:

```yaml
enabled: false
icon: "BOOK"
format: "<gold><username> <dark_gray>» <gray><message>"
```