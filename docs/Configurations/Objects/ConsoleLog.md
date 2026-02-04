# Console Log

This page covers the configuration of console log settings in SayanChat. The console log settings allow you to enable or disable logging of chat messages to the console and define the format of the log messages.

### Properties

- **enabled**: A boolean indicating whether console logging is enabled.
- **format**: A string representing the format of the console log messages. The format can include placeholders such as `<chatboxtype>`, `<chatboxid>`, `<user>`, and `<message>`.

### Example

Here is an example of a console log configuration:

```yaml
consoleLog:
  enabled: true
  format: "[<chatboxtype>] [<chatboxid>] <user>: <message>"
```

### Usage

When console logging is enabled, chat messages will be logged to the console using the specified format. This can be useful for monitoring chat boxes activity.