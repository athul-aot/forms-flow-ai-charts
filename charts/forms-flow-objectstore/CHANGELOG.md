# Changelog
## 8.5.0

### Added
  New chart for offline form submissions: forms-flow-objectstore.
  Shared settings are read from the forms-flow-ai ConfigMap and Secret
  (see forms-flow-ai 8.5.0).

### Changed
  image.tag v8.4.0-alpha (was v7.3.1). EE CI does not publish this image yet
  (forms-flow-objectstore has a CI workflow only): build it from
  forms-flow-ai-ee/forms-flow-objectstore on develop and push it with this tag.
