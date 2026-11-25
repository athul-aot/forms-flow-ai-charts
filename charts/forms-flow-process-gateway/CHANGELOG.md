# Changelog
## 8.5.0
### Added
  New chart, laid out like forms-flow-api: the gateway, an nginx sidecar
  serving it under /gatewayapi/, Service, Ingress, ServiceAccount, PDB and HPA.

  Offline forms env variables, read from the forms-flow-ai ConfigMap

    OFFLINE_WORKER_CLIENT_ID
    OFFLINE_WORKER_PUBLIC_KEY
    OFFLINE_ON_BEHALF_LEEWAY_S
    OFFLINE_REPLAY_REDIS_URL

### Changed
  camundaBaseUrlKey defaults to BPM_API_SERVICE_URL (was BPM_API_URL): the
  gateway calls Camunda inside the cluster instead of through the ingress.
  image.tag v8.3.1 (was v7.3.1, which does not exist for this EE image; the
  gateway ships with formsflow.ai EE 8.3.0 and later).
  nginx sidecar pinned to nginxinc/nginx-unprivileged:1.27-alpine with
  pullPolicy IfNotPresent (was latest / Always).

### Fixed
  KEYCLOAK_URL now includes the Keycloak context path (/auth). The gateway
  builds its service-account token URL as ${KEYCLOAK_URL}/realms/..., which
  returned 404 without it.
