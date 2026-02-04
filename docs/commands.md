# Commands

!!! note
    Some subcommands require permissions. See `permissions.md` for explicit nodes and chatbox permissions.

## Core

- `/sayanchat` (`/sc`)
- `/sayanchat version`
- `/sayanchat reload`
- `/sayanchat toggleglobalreadonly`
- `/sayanchat benchmark <proxy|bukkit>`

## Chat Boxes

- `/chatbox` (`/cb`)
- `/chatbox switch global`
- `/chatbox switch permissionbased <chatbox>`
- `/chatbox switch privatemessage <player>`
- `/chatbox switch <...> --output` (only changes output, not active box)
- `/chatbox send global <message>`
- `/chatbox send permissionbased <chatbox> <message>`
- `/defaultchatbox global`
- `/defaultchatbox permissionbased <chatbox>`
- `/defaultchatbox privatemessage <player>`
- `/mutechatbox list`
- `/mutechatbox unmuteall`
- `/mutechatbox global [--unmuteall]`
- `/mutechatbox permissionbased <chatbox>`
- `/mutechatbox privatemessage <player>`
- `/mutechatbox system`
- `/mutechatbox notify`
- `/mutechatbox spy`

## Private Messages

- `/msg <player> [message]` (aliases: `/privatemessage`, `/pm`, `/tell`, `/whisper`, `/w`)
- `/reply <message>` (alias: `/r`)

## Player Settings

- `/nickname <nickname>` (alias: `/nick`)
- `/nickname set <player> <nickname>`
- `/nickname reset [player]`
- `/defaultcolor <color>` (aliases: `/defaultcolor`, `/defaultcolors`)
- `/defaultcolor set <player> <color>`
- `/togglemention` (aliases: `/togglementions`)
- `/toggleprivatemessage` (aliases: `/toggleprivatemessages`)
- `/togglenotifyunseenmessages`
- `/ignore add <player>` (alias: `/block`)
- `/ignore remove <player>`
- `/ignore list`

## Moderation / Utilities

- `/history [chatBoxType] [--user <player>] [--target <player>] [--permissionbased <chatbox>] [--chatBoxId <id>] [--time <duration>] [--limit <n>] [--page <n>] [--flag <flag>] [--withtimestamp] [--scrollingcontent]`
- `/announcement <message> [-g] [-p] [-r]` (aliases: `/announce`)
