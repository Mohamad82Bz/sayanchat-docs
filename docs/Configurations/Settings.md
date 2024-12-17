# Settings

This page covers the configuration of various settings in SayanChat.

### Properties

- **proxy-mode**: A boolean indicating whether the proxy mode is enabled.
!!! note "Note on Proxy Mode"
    You should enable this if you are running a Proxy (e.g. BungeeCord, Velocity).
- **server-id**: A string representing the server ID.
!!! warning "Warning on Server ID"
    You must set this to a unique value for each server in a network. Database stores messages based on this ID.
- **send-chat-history-after-join**: A boolean indicating whether to send chat history after a player joins. Having this feature enabled can help players catch up on conversations, and they won't have an empty chat box after entering a server.
- **join-leave**: A `JoinLeave` object representing the join/leave message settings.
    - **enabled**: A boolean indicating whether join/leave messages are enabled.
    - **broadcast-in-world**: A boolean indicating whether to broadcast join/leave messages in the world.
- **placeholders**: A list of predefined placeholders used in chat formatting. You can change the serializer for each placeholder if needed.
    - **prefix**: A `Placeholder` object for the prefix.
    - **suffix**: A `Placeholder` object for the suffix.
    - **username**: A `Placeholder` object for the username.
    - **nickname**: A `Placeholder` object for the nickname.
    - **displayname**: A `Placeholder` object for the display name.
    - **defaultcolor**: A `Placeholder` object for the default color.
    - **message**: A `Placeholder` object for the message.

!!! tip "Prefix/Suffix Serializers"
    Set the serializers based on your prefix/suffix formatting. For example if you use legacy color codes in your prefix/suffix, set the serializer to `LEGACY_SECTION`.

- **custom-placeholders**: A list of [Custom Placeholder](Objects/CustomPlaceholder.md) objects representing custom placeholders.
- **notifier**: A `Notifier` object representing the notifier settings.
    - **format**: A string representing the format of the notifier message.
    - **sound**: A `Sound` object representing the sound settings for the notifier.
- **url**: A `URL` object representing the URL formatting settings.
    - **enabled**: A boolean indicating whether URL formatting is enabled.
    - **format**: A string representing the format of the URL.
- **nickname**: A `Nickname` object representing the nickname settings.
    - **character-limit**: An integer representing the character limit for nicknames.
- **logger**: A `Logger` object representing the logger settings.
    - **packet-warnings**: A boolean indicating whether packet warnings are enabled.

#### Placeholder Object
- **id**: A unique identifier for the placeholder.
- **serializer**: The serializer used for the placeholder value. Common serializers include `LEGACY_SECTION`, `PLAIN_TEXT`, and `MINIMESSAGE`.

### Example

Here is an example of a settings configuration:

```yaml
settingsConfig:
  proxy-mode: false
  server-id: "default"
  send-chat-history-after-join: true
  join-leave:
    enabled: true
    broadcast-in-world: false
  placeholders:
    prefix:
      id: "prefix"
      serializer: "LEGACY_SECTION"
    suffix:
      id: "suffix"
      serializer: "LEGACY_SECTION"
    username:
      id: "username"
      serializer: "PLAIN_TEXT"
    nickname:
      id: "nickname"
      serializer: "MINIMESSAGE"
    displayname:
      id: "displayname"
      serializer: "LEGACY_SECTION"
    defaultcolor:
      id: "defaultcolor"
      serializer: "MINIMESSAGE"
    message:
      id: "message"
      serializer: "MINIMESSAGE"
  custom-placeholders:
    - id: "mycustomplaceholder"
      serializer: "LEGACY_AMPERSAND"
      value: "&6My Custom Tag!"
  notifier:
    format: "<dark_gray>[<light_purple>Notifier<dark_gray>] <gray><message>"
    sound:
      enabled: true
      name: "ENTITY_EXPERIENCE_ORB_PICKUP"
      volume: 0.5
      pitch: 1.5
  url:
    enabled: true
    format: "<blue><url>↗</white>"
  nickname:
    character-limit: 16
  logger:
    packet-warnings: true
```