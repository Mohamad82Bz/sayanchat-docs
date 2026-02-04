# SayanChatNodeAPI

Package: `org.sayandev.sayanchat.api`

## Methods

- `CompletableFuture<List<ChatNodePackage>> getChatNodePackage(String sender)`
- `CompletableFuture<Map<ChatBoxInformation, ? extends List<ChatNode>>> getPrivateMessageChatNodes(String sender, int page, Long timestamp)`
- `CompletableFuture<Map<ChatBoxInformation, ? extends List<ChatNode>>> getPrivateMessageChatNodes(String sender, Integer page, Long timestamp)`
- `CompletableFuture<Map<ChatBoxInformation, ? extends List<ChatNode>>> getPermissionBasedChatNodes(int page, Long timestamp)`
- `CompletableFuture<Map<ChatBoxInformation, ? extends List<ChatNode>>> getPermissionBasedChatNodes(UUID userId, Integer page, Long timestamp)`
- `CompletableFuture<Map<ChatBoxInformation, ? extends List<ChatNode>>> getGlobalMessageChatNodes(int page, Long timestamp)`
- `CompletableFuture<Map<ChatBoxInformation, ? extends List<ChatNode>>> getGlobalMessageChatNodes(UUID userId, Integer page, Long timestamp)`
- `CompletableFuture<Unit> clearUnreadPrivateMessages(String sender, String receiver)`
- `CompletableFuture<String> getSessionToken(String name, String password)`
- `CompletableFuture<String> validateToken(String token)`

These methods expose chat history and web session helpers.
