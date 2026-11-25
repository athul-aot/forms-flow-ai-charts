# Changelog
## 8.5.0
### Changed
  Process engine calls go through forms-flow-process-gateway: BPM_API_URL
  is forms-flow-ai's PROCESS_GATEWAY_SERVICE_URL (was BPM_API_SERVICE_URL,
  Camunda directly). Added BPM_API_PREFIX (forms-flow-ai BPM_API_URL_PREFIX).

### Fixed
  extraEnvVars was rendered two columns too far left: a normal YAML list
  became a second container and the install failed. If you passed it as a
  pre-indented block string ("|2-") to work around this, change it back to
  a normal list.
  extraVolumeMounts was rendered at the wrong indentation and did not parse;
  it now renders in the main container's volumeMounts.
  extraVolumes was rendered at the wrong indentation and did not parse; it
  now renders in the pod's volumes.

## 8.4.0 (2026-05-05)

### Added

  Added env variables
    STRIPE_WEBHOOK_SECRET
    STRIPE_SECRET_KEY
    STRIPE_PUBLISHABLE_KEY
    STRIPE_PRICING_TABLE_ID
    TRIAL_PERIOD
