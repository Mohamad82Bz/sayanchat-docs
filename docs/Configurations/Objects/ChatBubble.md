# Chat Bubble

This page covers the configuration of chat bubble settings in SayanChat. Chat bubble settings are used to define how chat bubbles are displayed in the chat.

### Properties

- **enabled**: A boolean indicating whether the chat bubble feature is enabled.
- **fade-in**: An integer representing the duration (in ticks) for the chat bubble to fade in.
- **stay**: An integer representing the duration (in ticks) for the chat bubble to stay visible.
- **fade-out**: An integer representing the duration (in ticks) for the chat bubble to fade out.
- **background-color**: An `ARGB` representing the background color of the chat bubble. The `ARGB` format includes alpha, red, green, and blue components.

### Example

Here is an example of a chat bubble configuration:

```yaml
enabled: true
fade-in: 5
stay: 60
fade-out: 20
background-color:
  alpha: 64
  red: 0
  green: 0
  blue: 0
```