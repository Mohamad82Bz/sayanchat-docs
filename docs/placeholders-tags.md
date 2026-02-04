# Placeholders and Tags

## Built-in Placeholders

These are configured in `settings.yml` under `placeholders:`. You can change serializer type per placeholder.

- `prefix`
- `suffix`
- `username`
- `nickname`
- `displayname`
- `defaultcolor`
- `message`

## Custom Placeholders

Add your own in `settings.yml` under `custom-placeholders:`.

```yaml
custom-placeholders:
- id: mycustomplaceholder
  type: LEGACY_AMPERSAND
  value: '&6My Custom Tag!'
```

If PlaceholderAPI is installed, SayanChat will parse PAPI placeholders inside custom placeholder values.

## Placeholder Serializers

Supported serializer types:

- `PLAIN_TEXT`
- `LEGACY_AMPERSAND`
- `LEGACY_SECTION`
- `MINIMESSAGE`
- `GSON`

## MiniMessage Tags

SayanChat adds several tags for use in chat formats and messages.

- `<link:URL>`: Clickable URL using `settings.yml` `url.format`.
- `<mention:player>`: Mention a player using the configured mention format.
- `<item:slot player>`: Insert an item component.

`<item:slot player>` slots:

- `hand`, `offhand`, `head`, `chest`, `legs`, `feet`, or `0-26` for hotbar/slots.

### Rule Tag

- `<rule:id>`: Inserts the replace string or rule display based on `rules.yml`.

### Permissions for Tags

Tag usage is controlled by permissions (see `permissions.md`).
