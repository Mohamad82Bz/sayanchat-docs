# Features Overview

## Chat Boxes

SayanChat organizes chat into multiple boxes:

- Global chat
- Permission-based chat boxes (e.g., staff chat)
- Private message chat boxes
- System chat box
- Notify/spy chat boxes

Configuration lives in `configuration/chatboxes.md`.

## Chat History

Chat history can be queried with `/history` and shown in a scrolling UI on supported server versions.

## Mentions

Mentions can trigger sounds, toasts, and cooldowns. Configure in `chatboxes.yml` under `global-chat-box.mention`.

## Announcements

Manual and automatic announcements are configured in `announces.yml`.

## Rules

Rules allow regex filtering with different modes (swear, advertise, other). Configure in `rules.yml` and `rulesettings.yml`.

## Default Colors and Nicknames

Players can pick default colors and set nicknames. Configure colors in `defaultcolors.yml` and nickname limits in `settings.yml`.
