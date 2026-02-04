# language.yml

Controls all messages, warnings, and UI text. You can customize all output here.

## Sections

- `general`
- `chat-box`
- `join-leave`
- `warnings`
- `usage`
- `messages`
- `message-of-the-day`
- `anti-bot`

## Example (excerpt)

```yaml
general:
  prefix: <dark_aqua>SayanChat <gray>>
  no-permission: <prefix> <dark_red>You don't have permission to perform this command.
  player-not-found: <prefix> <red>Player not found!
chat-box:
  already-in-chat-box: <prefix> <red>You are already in this chat box.
  change-chat-box-notice:
  - ''
  - <aqua>You are now in <chatbox> chat box
warnings:
  chat-on-cooldown: <prefix> <red>Please slow down in chatting and try again in <time> second(s).
  private-message-fail: <prefix> <red>Receiver has disabled their private messages or they have ignored you.
messages:
  nickname-set: <prefix> <green>Nickname has been set.
  default-color-changed: <prefix> <green>Your default color has been changed to <color>.
```
