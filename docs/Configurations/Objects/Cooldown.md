# Cooldown

This page covers the configuration of cooldown settings in SayanChat. Cooldown settings are used to control the rate at which players can send messages, helping to prevent spam.

### Properties

- **enabled**: A boolean indicating whether the cooldown feature is enabled. Default is `true`.
- **cooldown**: An integer representing the cooldown period in seconds. This is the time players must wait before they can send another message after reaching the rate limit.
- **default-rate-limit**: An integer representing the default rate limit for players. This is the maximum number of messages a player can send within the cooldown period.
- **rate-limits**: A map of rate limits for specific groups. The key is the group name, and the value is the rate limit for that group. This allows different groups (e.g., staff, VIP) to have different rate limits.

### Example

Here is an example of a cooldown configuration:

```yaml
enabled: true
cooldown: 10
default-rate-limit: 3
rate-limits:
  staff: 8
  vip: 5
```

## How Cooldowns Work

Cooldowns in SayanChat are a rate-limiting system designed to prevent players from sending too many messages in a short period, which helps to reduce spam. The cooldown system works as follows:

1. **Rate Limit**: The `default-rate-limit` property defines the maximum number of messages a player can send within the cooldown period. For example, if the default rate limit is set to 3, players can send up to 3 messages before the cooldown period starts.

2. **Cooldown Period**: The `cooldown` property defines the period (in seconds) that players must wait before they can send another message after reaching the rate limit. For example, if the cooldown is set to 10 seconds, players must wait 10 seconds after sending the maximum number of messages before they can send another message.

3. **Group-Specific Rate Limits**: The `rate-limits` property allows you to define different rate limits for specific groups. For example, staff members might be allowed to send more messages than regular players. In the example configuration, staff can send up to 8 messages before the cooldown period starts, while VIP members can send up to 5 messages.
