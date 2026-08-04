# Cerebrium (cerebrium)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
