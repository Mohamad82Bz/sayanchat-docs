# Forwarding

This page covers the configuration of forwarding settings in SayanChat. Forwarding settings are used to define how messages are forwarded between different servers.

### Properties

- **enabled**: A boolean indicating whether the forwarding feature is enabled.
- **receive-from**: A list of strings representing the servers from which messages should be received.

### Example

Here is an example of a forwarding configuration:

```yaml
enabled: false
receive-from:
  - "lobby-2"
  - "lobby-3"
```