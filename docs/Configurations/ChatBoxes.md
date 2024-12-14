# Chat Boxes

This page covers the configuration of various chat boxes in SayanChat. The chat boxes include system chat, global chat, private message chat, and permission-based chat boxes.

### Properties

- **system-chat-box**: A [SystemChatBoxConfig](Objects/ChatBoxes/SystemChatBox.md) object representing the system chat box settings.
- **global-chat-box**: A [GlobalChatBoxConfig](Objects/ChatBoxes/GlobalChatBox.md) object representing the global chat box settings.
- **private-message-chat-box**: A [PrivateMessageChatBoxConfig](Objects/ChatBoxes/PrivateMessageChatBox.md) object representing the private message chat box settings.
- **permission-based-chat-boxes**: A list of [PermissionBasedChatBoxConfig](Objects/ChatBoxes/PermissionBasedChatBox.md) objects representing the permission-based chat box settings.

!!! tip
    SayanChat does not have any staff chat feature, you can actually create staff chat feature yourself by creating a permission-based chat box with a permission that only staff members have. (Default configuration does include staff chat, you can remove or create new ones as you wish)

!!! tip
    There are many use-cases for permission based staff chat boxes. You can create locale based chat boxes, rank based chat boxes, or even chat boxes for specific groups of players.

### Example

Here is an example of a chat boxes configuration:

```yaml
system-chat-box:
  # See the System Chat Box page for more details
global-chat-box:
  # See the Global Chat Box page for more details
private-message-chat-box:
  # See the Private Message Chat Box page for more details
permission-based-chat-boxes:
  # See the Permission-Based Chat Box page for more details
```
