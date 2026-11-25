# Changelog
## 8.5.0
### Fixed
  extraEnvVars was rendered two columns too far left: a normal YAML list
  became a second container and the install failed. If you passed it as a
  pre-indented block string ("|2-") to work around this, change it back to
  a normal list.
  extraVolumeMounts was rendered at the wrong indentation and did not parse;
  it now renders in the main container's volumeMounts.

## 8.4.0 (2025-04-14)

### Changed
  Updated Intentation in deployment yaml