# walmart-ads · Ad Service

Contextual advertisement gRPC service. Returns category-targeted ads based on product context keys passed by the frontend.

## Stack
- **Language:** Java 17
- **Framework:** gRPC / Netty
- **Build:** Gradle

## API
Implements `AdService` from `demo.proto`:
- `GetAds(AdRequest) → AdResponse` — returns a list of ads matching the provided context keys

## Running locally
```bash
./gradlew installDist
./build/install/hipstershop/bin/AdService
```
Service listens on port `9555` by default (`AD_SERVICE_PORT`).

## Building Docker image
```bash
docker build ./
```

## Dependencies
None — ad data is served from an in-memory static map. No downstream service calls.

