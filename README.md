# community-day-api

Single source of truth für den REST-Contract der Community-Day Talk-Scheduling App.

- `openapi.yaml` – OpenAPI 3.0 Contract (Talks, Slots, Assignment)
- Wird als Git-Submodule in `backend` und `frontend` eingebunden und dort per
  OpenAPI-Generator zu Server-Interfaces (Kotlin/Spring) bzw. TS-Client (Angular) generiert.

## Workflow

1. Contract hier ändern (`openapi.yaml`)
2. Commit + Push
3. In `backend`/`frontend`: `git submodule update --remote api && ./gradlew build` bzw. `npm run generate:api`
