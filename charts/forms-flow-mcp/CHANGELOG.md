# Changelog
## 8.5.0
### Fixed
  extraEnvVars was rendered two columns too far left: a normal YAML list
  became a second container and the install failed. If you passed it as a
  pre-indented block string ("|2-") to work around this, change it back to
  a normal list.
  extraVolumes was rendered without a volumes: key; it now renders in the
  pod's volumes.

## 8.4.0 (2026-4-28)

### Changed
  Updated image tag to v8.4.0.
### Updates
Added Env variables for forms-flow-ai-mcp.
 MCP_MULTI_TENANCY_ENABLED
  MCP_SERVER_HOST
  MCP_SERVER_PORT
  MCP_FORMSFLOW_ADMIN_URL
  FORMSFLOW_BEARER_TOKEN
  MCP_USERNAME
  MCP_PASSWORD
  MCP_ROPC_CLIENT_ID
  MCP_ROPC_CLIENT_SECRET