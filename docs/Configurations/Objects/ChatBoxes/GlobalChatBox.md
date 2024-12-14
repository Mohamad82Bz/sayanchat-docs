# Global Chat Box

This page covers the configuration of global chat box settings in SayanChat. Global chat box settings are used to define how the global chat is managed and displayed in the chat.

### Properties

- **enabled-worlds**: A list of strings representing the worlds where the global chat is enabled.
- **apply-rules**: A boolean indicating whether chat rules should be applied. See [Rules](../Rules.md) for more details.
- **chat-radius**: An integer representing the radius within which messages are visible.
- **format**: A string representing the format of the chat message. Placeholders like `<prefix>`, `<nickname>`, `<suffix>`, and `<message>` can be used.
- **notify-format**: A string representing the format of the notification message.
- **per-world-chat**: A boolean indicating whether the chat is separated per world.
- **cooldown**: A [CooldownConfig](../Cooldown.md) object representing the cooldown settings for the chat.
- **similarity**: A [SimilarityConfig](../Similarity.md) object representing the similarity settings for the chat.
- **chat-bubble**: A [ChatBubbleConfig](../ChatBubble.md) object representing the chat bubble settings.
- **forwarding**: A [Forwarding](../Forwarding.md) object representing the forwarding settings.
- **mention**: A [MentionConfig](../Mention.md) object representing the mention settings.

### Example

Here is an example of a global chat box configuration:

```yaml
enabled-worlds: []
apply-rules: true
chat-radius: 0
format: "<prefix> <nickname><suffix> <dark_gray>» <gray><message>"
notify-format: ""
per-world-chat: false
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
chat-bubble:
  enabled: true
  fade-in: 5
  stay: 60
  fade-out: 20
  background-color:
    alpha: 64
    red: 0
    green: 0
    blue: 0
forwarding:
  enabled: true
  receive-from:
    - "lobby-2"
    - "lobby-3"
mention:
  enabled: true
  format: "<green>@<username></green>"
  sound:
    enabled: true
    name: "ENTITY_EXPERIENCE_ORB_PICKUP"
    volume: 0.5
    pitch: 0.5
  cooldown: 10
```