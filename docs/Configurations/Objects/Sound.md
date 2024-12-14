# Sound

This page covers the configuration of sounds used in multiple configuration files in SayanChat.

## Sound Object

The `sound` object is used to define the sound settings. It has the following properties:

- **enabled**: A boolean indicating whether the sound is enabled.
- **name**: The name of the sound to be played. This can be a custom sound in resource packs or a sound name from [Bukkit Sounds List](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Sound.html).
- **volume**: The volume of the sound.
- **pitch**: The pitch of the sound.

### Example

Here is an example of a sound configuration:

```yaml
enabled: true
name: "ENTITY_EXPERIENCE_ORB_PICKUP"
volume: 1.0
pitch: 1.2
```