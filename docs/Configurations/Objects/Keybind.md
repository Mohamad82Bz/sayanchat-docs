# Keybind

This page covers the configuration of keybind settings in SayanChat. Keybind settings are used to define custom key combinations for some actions.

### Properties

- **keybind**: An enum representing the keybind action. The available options are:
    - **DROP_ITEM**: Corresponds to the keybind for dropping an item.
    - **DROP_ALL_ITEM**: Corresponds to the keybind for dropping all items, which is a combination of the sprint and drop keys.
    - **SWITCH_OFFHAND**: Corresponds to the keybind for switching the item to the offhand.
- **while-crouching**: A boolean indicating whether the keybind should be activated while crouching.
- **crouch-time-frame**: A long representing the time frame (in milliseconds) within which the crouch action must be performed to activate the keybind.

### Example

Here is an example of a keybind configuration:

```yaml
keybindConfig:
  keybind: "SWITCH_OFFHAND"
  while-crouching: true
  crouch-time-frame: 250
```