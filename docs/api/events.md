# Events

Package: `org.sayandev.sayanchat.api.event`

## ChatBoxSendMessageEvent

- `ChatBox getChatBox()`
- `User getUser()`
- `String getMessage()` / `setMessage(String)`
- Cancellable

## DefaultChatBoxEvent

- `User getUser()`
- `ChatBox getDefaultChatBox()` / `setDefaultChatBox(ChatBox)`

## GlobalChatBoxEvent

- `User getUser()`
- `String getMessage()` / `setMessage(String)`
- `Collection<Player> getMessageViewers()`
- Cancellable

## GlobalChatReceiveEvent

- `User getSender()`
- `List<Player> getReceivers()`
- `String getMessage()` / `setMessage(String)`

## InvalidPermissionBasedMessageReceiveEvent

Called when a permission-based chatbox message is received but the chatbox does not exist locally.

- `String getId()`
- `String getMessage()`
- `Component getParsedMessage()`
- `PermissionBasedChatBox getChatBox()` / `setChatBox(PermissionBasedChatBox)`

## PlayerMentionEvent

- `User getMentioner()`
- `User getMentioned()`
- Cancellable

## PlayerReceiveMessageEvent

- `User getSender()`
- `ChatBox getChatBox()`
- `Player getPlayer()`
- `String getMessage()`
- `Component getParsedMessage()`
- `Component getNotifyParsedMessage()`
- `MessageType getMessageType()`
- Cancellable

Message types:

- `VIEWER_MESSAGE`
- `NOTIFY_MESSAGE`
