# Cerebrium (cerebrium)

Cerebrium is a serverless GPU infrastructure platform for real-time AI and ML workloads. Developers package code with the Cortex framework and Cerebrium CLI, then deploy each function as an authenticated REST endpoint on autoscaling GPU/CPU compute billed per second, with streaming, WebSocket, async, and OpenAI-compatible invocation patterns.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cerebrium/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cerebrium/refs/heads/main/apis.yml)

## Tags

- AI
- GPU
- Serverless
- Inference
- ML Infrastructure

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Cerebrium Inference / Run Endpoints API

Calls each deployed function as an authenticated POST endpoint at /v4/{project}/{app}/{function}, billed per second of GPU/CPU compute. Supports synchronous JSON, Server-Sent Events streaming, async submission via async=true, and OpenAI-compatible chat/embedding requests using the standard OpenAI client with a Cerebrium JWT.

- **Human URL:** [https://www.cerebrium.ai/docs/cerebrium/endpoints/inference-api](https://www.cerebrium.ai/docs/cerebrium/endpoints/inference-api)
- **Base URL:** `https://api.aws.us-east-1.cerebrium.ai/v4`

#### Tags

- Inference
- Run
- GPU
- Streaming

#### Properties

- [Documentation](https://www.cerebrium.ai/docs/cerebrium/endpoints/inference-api)
- [API Reference](https://www.cerebrium.ai/docs/cerebrium/endpoints/inference-api)
- [OpenAPI](openapi/cerebrium-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cerebrium.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cerebrium.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cerebrium Streaming Endpoints API

Streams live model output over a Server-Sent Events (text/event-stream) response from a Python generator that yields data, invoked on the same /run endpoint with an Accept of text/event-stream.

- **Human URL:** [https://www.cerebrium.ai/docs/cerebrium/endpoints/streaming](https://www.cerebrium.ai/docs/cerebrium/endpoints/streaming)
- **Base URL:** `https://api.aws.us-east-1.cerebrium.ai/v4`

#### Tags

- Streaming
- SSE
- Inference

#### Properties

- [Documentation](https://www.cerebrium.ai/docs/cerebrium/endpoints/streaming)
- [OpenAPI](openapi/cerebrium-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cerebrium.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cerebrium.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cerebrium Async Requests API

Submits long-running inference asynchronously with the async=true query parameter, returning 202 Accepted with a run_id; results are forwarded to a configured webhookEndpoint rather than polled.

- **Human URL:** [https://www.cerebrium.ai/docs/cerebrium/endpoints/async](https://www.cerebrium.ai/docs/cerebrium/endpoints/async)
- **Base URL:** `https://api.aws.us-east-1.cerebrium.ai/v4`

#### Tags

- Async
- Jobs
- Webhooks

#### Properties

- [Documentation](https://www.cerebrium.ai/docs/cerebrium/endpoints/async)
- [OpenAPI](openapi/cerebrium-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cerebrium.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cerebrium.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cerebrium App Deployment / Management API

Packages a Cortex project and deploys each function as a persistent REST endpoint via the Cerebrium CLI (init, login, run, deploy), with apps, deployments, scaling, and configuration managed through the CLI and dashboard.

- **Human URL:** [https://www.cerebrium.ai/docs/cerebrium/getting-started/introduction](https://www.cerebrium.ai/docs/cerebrium/getting-started/introduction)
- **Base URL:** `https://api.aws.us-east-1.cerebrium.ai/v4`

#### Tags

- Deployment
- Management
- Apps
- CLI

#### Properties

- [Documentation](https://www.cerebrium.ai/docs/cerebrium/getting-started/introduction)
- [OpenAPI](openapi/cerebrium-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cerebrium.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cerebrium.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cerebrium Logs / Status API

Surfaces app logs, metrics, and platform status through the CLI (cerebrium logs, cerebrium status), the app dashboard, and the public status page.

- **Human URL:** [https://status.cerebrium.ai/](https://status.cerebrium.ai/)
- **Base URL:** `https://api.aws.us-east-1.cerebrium.ai/v4`

#### Tags

- Logs
- Status
- Observability

#### Properties

- [Documentation](https://www.cerebrium.ai/docs/cerebrium/getting-started/introduction)
- [Status Page](https://status.cerebrium.ai/)
- [OpenAPI](openapi/cerebrium-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cerebrium.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cerebrium.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/CerebriumAI)
- [LinkedIn](https://www.linkedin.com/company/cerebrium)
- [Website](https://www.cerebrium.ai)
- [Documentation](https://www.cerebrium.ai/docs)
- [Plans](plans/cerebrium-plans-pricing.yml)
- [Rate Limits](rate-limits/cerebrium-rate-limits.yml)
- [Fin Ops](finops/cerebrium-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
