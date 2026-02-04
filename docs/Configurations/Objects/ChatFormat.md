# Chat Format

This page covers the configuration of chat formats in SayanChat. Chat formats define how messages are displayed in the chat.

### Properties

- **inChatBox**: A string representing the format of messages displayed in the chat box. This format can include placeholders such as `<prefix>`, `<nickname>`, `<suffix>`, and `<message>`.
- **notify**: A string representing the format of notification messages. This format can also include placeholders.

### Example

Here is an example of a chat format configuration:

```yaml
chatFormat:
  inChatBox: "<prefix> <nickname><suffix> <dark_gray>» <gray><message>"
  notify: ""
```

### Usage

The `inChatBox` format is used to display messages in the chat box, while the `notify` format is used when the user is not inside the chat box. You can customize these formats to include various placeholders to dynamically insert values into the messages.