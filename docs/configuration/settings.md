# settings.yml

Controls global behavior, placeholders, join/leave, nicknames, and other plugin settings.

## Key Options

- `proxy-mode`: Enable if this server is part of a proxy network.
- `server-id`: Server identifier used in chat history and routing.
- `enabled-worlds`: If non-empty, only these worlds use SayanChat.
- `join-leave`: Join/leave message settings.
- `placeholders`: Serializer configuration for built-in placeholders.
- `custom-placeholders`: Custom placeholders (supports PAPI).
- `rules.notifier`: Notification format for rule triggers.
- `notifier`: Notify format/sound for system notifications.
- `send-chat-history-after-join`: Send history on join.
- `anti-bot`: Require movement before chatting.
- `fix-persian-font`: Enables font fix for Persian characters.

## Example

```yaml
proxy-mode: true
server-id: lobby
enabled-worlds: []
join-leave:
  enabled: true
  broadcast-in-world: false
  disable-default-join-leave: false
placeholders:
  prefix:
    id: prefix
    type: LEGACY_SECTION
  suffix:
    id: suffix
    type: LEGACY_SECTION
  username:
    id: username
    type: PLAIN_TEXT
  nickname:
    id: nickname
    type: MINIMESSAGE
  displayname:
    id: displayname
    type: LEGACY_SECTION
  defaultcolor:
    id: defaultcolor
    type: MINIMESSAGE
  message:
    id: message
    type: MINIMESSAGE
custom-placeholders:
- id: mycustomplaceholder
  type: LEGACY_AMPERSAND
  value: '&6My Custom Tag!'
rules:
  notifier:
    format: <dark_gray>[<light_purple>Notifier<dark_gray>] <gray><message>
    sound:
      enabled: true
      sound: ENTITY_EXPERIENCE_ORB_PICKUP
      volume: 0.5
      pitch: 1.5
    toast:
      enabled: false
      icon: BOOK
      format: <gold>Notifier <gray>> <aqua><message>
url:
  enabled: true
  format: <blue><url>></blue>
nickname:
  character-limit: 16
notifier:
  format:
    in-chat-box: <prefix> <nickname><suffix> <dark_gray>> <gray><message>
    notify: ''
  sound:
    enabled: true
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 0.5
    pitch: 1.5
  send-private-message-spy: true
logger:
  packet-warnings: true
  toast-warnings: true
  packet-debug: false
send-chat-history-after-join: true
anti-bot:
  enabled: false
  move-threshold: 1
fix-persian-font: true
```
