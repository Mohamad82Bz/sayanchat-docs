# Custom Placeholder

This page covers the configuration of custom placeholders in SayanChat. Custom placeholders allow you to define your own placeholders with specific values and serializers.

### Properties

- **id**: A unique identifier for the custom placeholder.
- **type**: The serializer used for the custom placeholder value. Available serializers include `PLAIN_TEXT`, `LEGACY_AMPERSAND`, `LEGACY_SECTION`, `MINIMESSAGE`, and `GSON`.
- **value**: The value of the custom placeholder.

### Example

Here is an example of a custom placeholder configuration:

```yaml
customPlaceholders:
  - id: "mycustomplaceholder"
    type: "LEGACY_AMPERSAND"
    value: "&6My Custom Tag!"
```

### Serializer Enum

The `Serializer` enum defines the available serializers for custom placeholders:

- **PLAIN_TEXT**: Uses `PlainTextComponentSerializer`.
- **LEGACY_AMPERSAND**: Uses `LegacyComponentSerializer` with ampersand (`&`) as the color code character.
- **LEGACY_SECTION**: Uses `LegacyComponentSerializer` with section (`§`) as the color code character.
- **MINIMESSAGE**: Uses `MiniMessage` for advanced text formatting. For more details, see [MiniMessage Documentation](https://docs.advntr.dev/minimessage/index.html).
- **GSON**: Uses `GsonComponentSerializer` for JSON-based text formatting. For more details, see [Minecraft JSON Component Documentation](https://minecraft.fandom.com/wiki/Raw_JSON_text_format).

!!! tip "How to use properly parsed [PlaceholderAPI](https://github.com/PlaceholderAPI/PlaceholderAPI/wiki) placeholders in chat format"
    You can use [PlaceholderAPI](https://github.com/PlaceholderAPI/PlaceholderAPI/wiki) placeholders in custom placeholders with any serializer.
    This is particularly useful because many, if not all, of [PlaceholderAPI](https://github.com/PlaceholderAPI/PlaceholderAPI/wiki)'s placeholders use legacy color codes,
    so you can create custom placeholders with the `LEGACY_AMPERSAND` serializer and use these custom placeholders anywhere
    within SayanChat's chat formats where it uses [MiniMessage](https://docs.advntr.dev/minimessage/index.html) formatting.