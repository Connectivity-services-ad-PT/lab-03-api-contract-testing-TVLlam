# Local Testing Status

Lab 03 collection is designed to run on both environments:

- Mock: `baseUrl=http://localhost:4010`
- Local: `baseUrl=http://localhost:8000`

As of 2026-06-02, the local IoT Ingestion implementation is not running in this repository. `npm run test:local` produces `ECONNREFUSED 127.0.0.1:8000` for the main IoT endpoints, while the consumer-side AI Vision mock test still passes through `http://localhost:4011`.

This is the current local-environment note required by the lab condition: the local service is pending implementation/startup. The same exported collection and local environment are ready to run again once the real service is available on port 8000.
