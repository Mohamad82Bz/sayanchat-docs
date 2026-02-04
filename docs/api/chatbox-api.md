# SayanChatChatBoxAPI

Package: `org.sayandev.sayanchat.api`

## Methods

- `CompletableFuture<?> switchChatBox(Player player, ChatBox chatBox, boolean locked, boolean onJoin, boolean silent)`

Switches a player to a chat box. Returns a future that completes when the switch is done.

- `CompletableFuture<Unit> setDefaultChatBox(UUID uniqueId, ChatBox chatBox)`

Sets the default chat box for a user.
