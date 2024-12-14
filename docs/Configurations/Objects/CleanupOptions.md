# Cleanup Options

This page covers the configuration of cleanup options in SayanChat. Cleanup options are used to automatically delete old messages from database after a certain number of days or after a certain number of messages.

### Properties

- **enabled**: A boolean indicating whether the cleanup feature is enabled. Default is `true`.
- **delete-after-days**: An integer representing the number of days after which messages should be deleted.
- **delete-after-messages**: An integer representing the number of messages after which old messages should be deleted.

### Example

Here is an example of a cleanup options configuration:

```yaml
enabled: true
delete-after-days: 30
delete-after-messages: 1000
```