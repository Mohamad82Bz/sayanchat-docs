# Permissions

This list includes explicit permission nodes used by SayanChat. Some permissions are also defined by config (e.g., permission-based chatboxes).

## Chat Boxes

- `sayanchat.chatbox.<id>`: Access a permission-based chatbox (use the chatbox `id`).
- `sayanchat.staff.notify`: Access the notify chatbox mute toggle.
- `sayanchat.staff.spy`: Access the spy chatbox mute toggle.
- `sayanchat.bypass.chatradius`: Ignore global chat radius limit.

## Nicknames and Colors

- `sayanchat.nickname`: Use nicknames.
- `sayanchat.commands.nickname.reset.others`: Reset another player's nickname.
- `sayanchat.defaultcolor.<id>`: Use a default color by `id`.

## Rules and Filters

- `sayanchat.bypass.rules`: Bypass all chat/rule filters.
- `sayanchat.bypass.antibot`: Bypass anti-bot movement checks.
- `sayanchat.bypass.similarity`: Bypass similarity checks.
- `sayanchat.bypass.cooldown`: Bypass chat cooldowns.
- `sayanchat.cooldown.<role>`: Use a specific cooldown tier (`role` in `chatboxes.yml`).

## Mentions and Private Messages

- `sayanchat.bypass.mentiondisabled`: Mention players who disabled mentions.
- `sayanchat.bypass.mentioncooldown`: Bypass mention cooldown.
- `sayanchat.bypass.privatemessagedisabled`: Message players who disabled PMs.
- `sayanchat.bypass.ignore`: Message players who ignored you.
- `sayanchat.bypass.spy`: Hide private messages from spy output.
- `sayanchat.bypass.vanish`: Bypass vanish checks for mentions/PM.

## Formatting Tags (MiniMessage)

These permissions control which tags are allowed in chat and nicknames. The parent permission is `sayanchat.chat` (chat) and `sayanchat.nickname` (nickname).

- `sayanchat.chat.newline`
- `sayanchat.chat.color`
- `sayanchat.chat.decorations`
- `sayanchat.chat.magic`
- `sayanchat.chat.gradient`
- `sayanchat.chat.rainbow`
- `sayanchat.chat.hoverevent`
- `sayanchat.chat.clickevent`
- `sayanchat.chat.keybind`
- `sayanchat.chat.reset`

For nicknames, use the same suffixes under `sayanchat.nickname.*`.
