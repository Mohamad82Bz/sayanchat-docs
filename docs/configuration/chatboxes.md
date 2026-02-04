# chatboxes.yml

Controls all chat boxes and chat behavior.

## Sections

- `system-chat-box`: System messages and history settings.
- `global-chat-box`: Main public chat settings.
- `private-message-chat-box`: PM behavior and formatting.
- `permission-based-chat-boxes`: List of permission-gated chat boxes.
- `notify-chat-box`: Format for rule notifications and staff alerts.
- `chat-box-command-switch-proxy`: Alternate command for switching chatboxes.
- `chat-box-command-permission-based-send-proxy`: Alternate command for sending to permission-based boxes.

## Example

```yaml
system-chat-box:
  save-in-database: true
  cleanup-options:
    enabled: true
    delete-after-days: 1
    delete-after-messages: 100
  can-be-muted: true
  mute-when-not-in-global: false
  send-notify-action-bar-when-muted: true
  send-history: true
  enabled: true

global-chat-box:
  enabled-worlds: []
  chat-radius: 0
  per-world-chat: false
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
    additional-height: 0.0
  forwarding:
    enabled: true
    forward-id: lobby-2
    receive-from:
    - lobby-1
    - lobby-3
  mention:
    enabled: true
    format: <green>@<username></green>
    sound:
      enabled: true
      sound: ENTITY_EXPERIENCE_ORB_PICKUP
      volume: 0.5
      pitch: 0.5
    cooldown: 10
  apply-rules: true
  format:
    in-chat-box: <prefix> <nickname><suffix> <dark_gray>> <gray><message>
    notify: ''
  web-format:
    in-chat-box: <aqua>[Web] <gray><nickname> <dark_gray>> <gray><message>
    notify: ''
  notify-toast:
    enabled: false
    icon: BOOK
    format: <gold><username> <dark_gray>> <gray><message>
  sound:
    enabled: false
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.0
  notify-sound:
    enabled: false
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.0
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
  cleanup-options:
    enabled: true
    delete-after-days: 30
    delete-after-messages: 1000
  read-only: false
  console-log:
    enabled: true
    format: '[<chatboxtype>] [<chatboxid>] <user>: <message>'
  send-history: true
  trigger-prefix:
    enabled: false
    prefix: '#'
    case-sensitive: false
  parse-message-per-player: false

private-message-chat-box:
  sender-notify-format: <hover:show_text:'<light_purple>Click to Reply'><click:suggest_command:'/pm <username> '><blue>✉ <green>You <aqua>-> <gold><username></hover> <gray>> <aqua><message>
  receiver-notify-format: <hover:show_text:'<light_purple>Click to Reply'><click:suggest_command:'/pm <username> '><blue>✉ <gold><username> <aqua>-> <green>You</hover> <gray>> <aqua><message>
  web-receiver-notify-format: <hover:show_text:'<light_purple>Click to Reply'><click:suggest_command:'/pm <username> '><blue>✉ [Web] <gold><username> <aqua>-> <green>You</hover> <gray>> <aqua><message>
  spy-format: <red>✉ <gold><sender> <aqua>-> <gold><receiver> <dark_gray>> <gray><message>
  unread-private-messages-notify-sender-count: 5
  exit-keybind:
    keybind: SWITCH_OFFHAND
    while-crouching: true
    crouch-time-frame: 250
  suggest-all-players-in-command: true
  apply-rules: true
  format:
    in-chat-box: <blue>✉ <gold><username> <dark_gray>> <#F7F7F7><message>
    notify: ''
  web-format:
    in-chat-box: <blue>✉ [Web] <gold><username> <dark_gray>> <#F7F7F7><message>
    notify: ''
  notify-toast:
    enabled: true
    icon: BEACON
    format: <red>PM <gold><username> <gray>> <aqua><message>
  sound:
    enabled: false
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.0
  notify-sound:
    enabled: false
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.0
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
  cleanup-options:
    enabled: true
    delete-after-days: 90
    delete-after-messages: 250
  read-only: false
  console-log:
    enabled: true
    format: '[<chatboxtype>] <sender> -> <receiver>: <message>'
  send-history: true
  trigger-output:
    enabled: true
    prefix: '@'
    case-sensitive: false

permission-based-chat-boxes:
- id: staff
  permission: sayanchat.chatbox.staff
  exit-keybind:
    keybind: SWITCH_OFFHAND
    while-crouching: true
    crouch-time-frame: 250
  trigger-prefix:
    enabled: false
    prefix: '!'
    case-sensitive: false
  send-history: true
  apply-rules: false
  format:
    in-chat-box: '<red>Staff <dark_gray>> <white><username>: <gray><message>'
    notify: '<gray>[<red>Staff<gray>] <white><username>: <gray><message>'
  web-format:
    in-chat-box: ''
    notify: ''
  notify-toast:
    enabled: false
    icon: NETHER_STAR
    format: <aqua><username> <gray>> <red><message>
  sound:
    enabled: true
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 0.75
    pitch: 1.25
  notify-sound:
    enabled: false
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 1.0
    pitch: 1.0
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
  cleanup-options:
    enabled: true
    delete-after-days: 30
    delete-after-messages: 500
  console-log:
    enabled: true
    format: '[<chatboxtype>] [<chatboxid>] <user>: <message>'
  read-only: false

save-queue-interval: 10000

chat-box-command-switch-proxy:
  enabled: true
  command: switchchat

chat-box-command-permission-based-send-proxy:
  enabled: true
  command: sendchat

notify-chat-box:
  format:
  - <dark_gray> ┏
  - '<dark_gray> | <gold>• <gray>Rule: <rulemode>'
  - '<dark_gray> | <gold>• <gray>Server: <yellow><server>'
  - '<dark_gray> | <gold>• <gray>User: <yellow><user>'
  - '<dark_gray> | <gold>• <gray>Time: <yellow><time>'
  - <dark_gray> |
  - '<dark_gray> | <gold>• <gray>Message: <message>'
  - <dark_gray> ┗
  sound:
    enabled: true
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    volume: 0.5
    pitch: 1.5
  send-private-message-spy: true
  send-history: true

delete-per-messages: 100
send-chat-box-notice-when-connecting-with-same-server-alias: false
silent-join-when-connecting-with-same-server-alias: true
```
