# Message of the Day

This page covers the configuration of the Message of the Day (MOTD) settings in SayanChat. The MOTD is displayed to players when they join the server.

### Properties

- **message**: A list of strings representing the lines of the MOTD. The messages can include formatting tags.

### Example

Here is an example of a Message of the Day configuration:

```yaml
messageOfTheDay:
  message:
    - "<gold>Welcome to <reset>ExampleMC"
    - "<gold>Join our discord server <underlined><click:open_url:'https://discord.gg/example'>here"
    - "<gold>Don't forget to vote for us on <underlined><click:open_url:'https://www.examplemc.net/vote'>our website"
```

!!! note
    All formats in this documentation use Adventure MiniMessage. For a guide on how to use the format, please refer to [MiniMessage Documentation](https://docs.advntr.dev/minimessage/index.html).