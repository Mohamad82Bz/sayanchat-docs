# Private Message Chat Box

This page covers the configuration of private message chat box settings in SayanChat. Private message chat box settings are used to define how private messages are formatted and handled in the chat.

### Properties

- **apply-rules**: A boolean indicating whether chat rules should be applied. See [Rules](../Rules.md) for more details.
- **format**: A string representing the format of the private message. Placeholders like `<username>` and `<message>` can be used.
- **sender-notify-format**: A string representing the format of the notification message for the sender.
- **receiver-notify-format**: A string representing the format of the notification message for the receiver.
- **spy-format**: A string representing the format of the spy message.
- **notify-toast**: A [Toast](../Toast.md) object representing the toast notification settings.
- **cooldown**: A [CooldownConfig](../Cooldown.md) object representing the cooldown settings for the chat.
- **similarity**: A [SimilarityConfig](../Similarity.md) object representing the similarity settings for the chat.
- **unread-private-messages-notify-sender-count**: An integer representing the number of unread private messages to notify the sender about.
- **exit-keybind**: A [KeybindConfig](../Keybind.md) object representing the keybind settings for exiting the chat box.
- **suggest-all-players-in-command**: A boolean indicating whether to suggest all players in the command.

### Example

Here is an example of a private message chat box configuration:

```yaml
apply-rules: true
format: "<blue>✉ <gold><username> <dark_gray>» <#F7F7F7><message>"
sender-notify-format: "<hover:show_text:'<light_purple>• <green>Destination: <aqua><destination>\n\n<light_purple>Click to Reply'><click:suggest_command:'/pm <username> '><blue>✉ <green>You <aqua>-> <gold><username></hover> <gray>» <aqua><message>"
receiver-notify-format: "<hover:show_text:'<light_purple>• <green>Source: <aqua><source>\n\n<light_purple>Click to Reply'><click:suggest_command:'/pm <username> '><blue>✉ <gold><username> <aqua>-> <green>You</hover> <gray>» <aqua><message>"
spy-format: "<hover:show_text:'<light_purple>• <green>Source: <aqua><source>\n<light_purple>• <green>Destination: <aqua><destination>'><red>✉ <gold><sender> <aqua>-> <gold><receiver></hover> <dark_gray>» <gray><message>"
notify-toast:
  enabled: true
  icon: "BEACON"
  format: "<red>PM <gold><username> <gray>» <aqua><message>"
cooldown:
  enabled: true
  cooldown: 10
  default-rate-limit: 3
  rate-limits:
    staff: 8
    vip: 5
similarity:
  enabled: true
  threshold: 0.8
  remember-count: 1
unread-private-messages-notify-sender-count: 5
exit-keybind:
  keybind: "SWITCH_OFFHAND"
  while-crouching: true
  crouch-time-frame: 250
suggest-all-players-in-command: true
```