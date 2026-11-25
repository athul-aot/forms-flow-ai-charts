# Changelog
## 8.5.0

### Added
  New chart for offline form submissions: forms-flow-edge.
  Shared settings are read from the forms-flow-ai ConfigMap and Secret
  (see forms-flow-ai 8.5.0).

### Changed
  image.tag v8.4.0-alpha (was v7.3.1, which does not exist for this EE image):
  the tag EE develop publishes. Pin the release tag once offline forms ship
  in an EE release.
