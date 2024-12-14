# System Chat Box

This page covers the configuration of system chat box settings in SayanChat. System chat box settings are used to define how system messages are handled in the chat.

### Properties

- **save-in-database**: A boolean indicating whether the system messages should be saved in the database.
- **cleanup-options**: A [CleanupOptions](../CleanupOptions.md) object representing the cleanup options for the chat box.
- **can-be-muted**: A boolean indicating whether the system chat box can be muted by players.

### Example

Here is an example of a system chat box configuration:

```yaml
save-in-database: true
cleanup-options:
  enabled: true
  delete-after-days: 1
  delete-after-messages: 100
can-be-muted: true
```