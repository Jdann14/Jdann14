## Josh D'Annunzio

**I'm building [UpStream](https://upstreamcv.com) — the developer infrastructure for live camera intelligence.**

Every camera in the world is generating video that nobody watches. The bottleneck isn't the cameras or the models — it's the plumbing in between: stream ingest, codec handling, session auth, GPU scheduling, model serving, storage, alerts, APIs. Today every team rebuilds it from scratch.

UpStream is the layer between cameras and code. Connect any camera, declare what to detect, count, or track, and we handle the rest. Think AWS Lambda for live video.

→ [upstreamcv.com](https://upstreamcv.com) · status: private beta · architecture: **[upstream-architecture-notes](https://github.com/Jdann14/upstream-architecture-notes)**

---

### What ships today

UpStream is at Milestone 7. The platform is four services:

- **Agent** — pip-installable Python CLI. Captures from any camera (webcam, RTSP), publishes SRT to ingest with heartbeat and reconnect. ~6k LOC, 367 tests.
- **Streaming server** — MediaMTX on a custom Alpine + FFmpeg image. SRT ingest on UDP 18890, WebRTC fanout via WHEP, HTTP publish-auth gate.
- **Control plane** — FastAPI + asyncpg + Supabase. 31 endpoints across accounts, agents, cameras, sessions, snapshots, ingest webhooks. Live at [api.upstreamcv.com](https://api.upstreamcv.com).
- **Operator dashboard** — Next.js 16, Tailwind v4, Supabase Realtime. Live WebRTC playback, snapshot capture, API token management.

Architecture, design decisions, and roadmap: **[upstream-architecture-notes](https://github.com/Jdann14/upstream-architecture-notes)**

---

### Prior work

**CrowdCount** — Computer vision lead. Production people-counting on live camera feeds: YOLO detection, ByteTrack + ReID for cross-frame identity, line-crossing logic, API-connected analytics dashboards.
→ [Demo video](https://youtu.be/wB6bHNOxsBk)

**RELI Group** — Data engineering on federal cloud modernization. Spark, Databricks, EMR on AWS. Production data workflows.

**B.S. Statistics & Data Science** — ML, model evaluation, applied statistics.

---

### Stack

Python · TypeScript · FastAPI · Next.js · OpenCV · FFmpeg · SRT · RTSP · WebRTC · MediaMTX · Supabase · Postgres · AWS

### Reach me

[upstreamcv.com](https://upstreamcv.com) · [LinkedIn](https://www.linkedin.com/in/josh-d-annunzio-3b0171227/)
```
