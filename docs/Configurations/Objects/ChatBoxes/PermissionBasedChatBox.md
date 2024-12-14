# Permission-Based Chat Box

This page covers the configuration of permission-based chat box settings in SayanChat. Permission-based chat box settings are used to define chat boxes that are accessible only to players with specific permissions.

### Properties

- **id**: A string representing the unique identifier for the chat box.
- **permission**: A string representing the permission required to access the chat box.
- **apply-rules**: A boolean indicating whether chat rules should be applied. See [Rules](../Rules.md) for more details.
- **format**: A string representing the format of the chat message. Placeholders like `<username>` and `<message>` can be used.
- **notify-format**: A string representing the format of the notification message.
- **notify-toast**: A [Toast](../Toast.md) object representing the toast notification settings.
- **sound**: A [Sound](../Sound.md) object representing the sound settings.
- **cooldown**: A [CooldownConfig](../Cooldown.md) object representing the cooldown settings for the chat.
- **similarity**: A [SimilarityConfig](../Similarity.md) object representing the similarity settings for the chat.
- **exit-keybind**: A [KeybindConfig](../Keybind.md) object representing the keybind settings for exiting the chat box.
- **cleanup-options**: A [CleanupOptions](../CleanupOptions.md) object representing the cleanup options for the chat box.

### Example

Here is an example of a permission-based chat box configuration:

```yaml
permissionBasedChatBoxConfig:
  id: "staff"
  permission: "sayanchat.chatbox.staff"
  apply-rules: false
  format: "<dark_red>[StaffChat] <gray><username> <dark_gray>» <aqua><message>"
  notify-format: "<red>[StaffChat] <gray><username> <dark_gray>» <aqua><message>"
  notify-toast:
    enabled: true
    icon: "BARRIER"
    format: "<red>Staff <gold><username> <gray>» <aqua><message>"
  sound:
    enabled: true
    name: "ENTITY_EXPERIENCE_ORB_PICKUP"
    volume: 1.0
    pitch: 1.2
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
  exit-keybind:
    keybind: "SWITCH_OFFHAND"
    while-crouching: true
    crouch-time-frame: 250
  cleanup-options:
    enabled: true
    delete-after-days: 30
    delete-after-messages: 500
```