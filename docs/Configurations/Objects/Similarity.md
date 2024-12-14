# Similarity

This page covers the configuration of similarity settings in SayanChat. Similarity settings are used to detect and block similar messages sent by players to prevent spam.

### Properties

- **enabled**: A boolean indicating whether the similarity feature is enabled.
- **threshold**: A double representing the similarity threshold. Messages with a similarity score above this threshold will be considered similar.
- **remember-count**: An integer representing the number of past messages to remember for similarity comparison.

### Example

Here is an example of a similarity configuration:

```yaml
enabled: true
threshold: 0.8
remember-count: 1
```