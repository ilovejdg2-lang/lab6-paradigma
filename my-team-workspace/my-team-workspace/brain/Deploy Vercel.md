# Deploy Vercel

## Facts

- Vercel Functions + Fluid Compute support Socket.IO / WebSockets (docs 2026).
- Connections pin to one instance; max duration ends the socket → client must reconnect.
- In-memory `io.emit` does **not** cross instances → need `@socket.io/redis-adapter` + Redis URL for multi-user chat in production.

## Plan (approved direction)

- Export Express/HTTP server for Vercel; enable Fluid Compute.
- Optional `REDIS_URL`: when set, attach Redis adapter; without it, local single-process still works.
- Domain: pending `<VERCEL_DOMAIN>`.

## Redis / Upstash (docs check — before creating)

- Socket.IO adapter needs **Redis Pub/Sub** over a real Redis protocol connection.
- Upstash: use **TCP** connection string `rediss://default:<TOKEN>@<ENDPOINT>:<PORT>` from Connect → **TCP** tab.
- **Do not** use `UPSTASH_REDIS_REST_URL` / `UPSTASH_REDIS_REST_TOKEN` as `REDIS_URL` — REST does not replace TCP Pub/Sub for the adapter.
- Free plan (docs): $0, **250 MB** data, **500K commands/month**, **10 GB** bandwidth, **1** database; no SLA; TLS on.
- Installed client: `redis` (node-redis) + `@socket.io/redis-adapter`. Upstash documents node-redis SUBSCRIBE over TCP. Socket.IO docs warn node-redis may fail to restore subscriptions after reconnect and suggest **ioredis** — if Prod Pub/Sub flakes, switch adapter clients to ioredis before blaming Upstash.
- **Not created yet.** Local verification does not need Redis.

## Status

Local Auth0 verification in progress; **deploy not verified**.

Last reinforced 2026-10-28

