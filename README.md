# Hey, I'm Josh

I'm a software engineer in Boulder, CO. I like building systems that take messy real-world data (live video, healthcare records, and lately on-chain lending markets) and turn it into something reliable. By day I engineer data and reports for federal healthcare programs in Databricks. Outside of that I'm usually deep in some side project.

## What I'm building now: a Morpho liquidation bot

*Private for now, but it's what I spend most of my time on.*

It's a bot that watches [Morpho Blue](https://morpho.org) lending markets and liquidates unhealthy positions to earn the liquidation bonus. It runs live and competes against other bots, so being fast and being safe both matter.

- Keeps a local mirror of every position, built from on-chain events, and computes health locally. The only network call between "this position is liquidatable" and "transaction sent" is the send itself.
- Its Solidity contract enforces the outcome on-chain: whitelisted markets and routers, balance checks before and after every swap, minimum-profit floors, and profit sent to a separate treasury wallet in the same transaction.
- Guardrails include gas caps, auto-pause, a kill switch, and Telegram alerts. New markets run in shadow mode before they go live.
- Testing uses a lot of replays: mainnet fork tests, recorded price-crash replays, and fuzz tests on the contract.

**Stack:** TypeScript, viem, Solidity, Foundry, AWS

## Day job: RELI Group

Since May 2024 I've worked on healthcare data for the Centers for Medicare & Medicaid Services (CMS), and I'm in Databricks every day. Most of my work is engineering the reports that go to stakeholders: I turn what they need to know into SQL and PySpark, make sure the numbers hold up, and get the results delivered. I'm also under the hood a lot, working on the pipelines that feed those reports, on data-quality checks, and on tracking down why two numbers don't match.

## Previously

### Upstream Vision (co-founder, May–Sep 2026)

I co-founded Upstream with [Elkan Bruha](https://github.com/elkanbruha). It was a reliability layer for computer vision in production: it streamed video from real cameras, ran detection on it, and told operators when and why detection quality slipped. The platform is split across these repos:

- [upstream-agent](https://github.com/UpstreamCV/upstream-agent): pip-installable Python agent that reads a camera feed and streams it securely to Upstream
- [upstream-streaming-server](https://github.com/UpstreamCV/upstream-streaming-server): accepts, validates, routes, and monitors incoming video streams (SRT + MediaMTX)
- [upstream-processor](https://github.com/UpstreamCV/upstream-processor): runs one worker per stream, including NVIDIA DeepStream inference
- [upstream-api-server](https://github.com/UpstreamCV/upstream-api-server): control plane for accounts, agents, cameras, and stream sessions (FastAPI + Postgres)
- [upstream-dashboard](https://github.com/UpstreamCV/upstream-dashboard): operator dashboard with live video (Next.js + Supabase Auth)
- [upstream-admin-panel](https://github.com/UpstreamCV/upstream-admin-panel): internal admin tool for system health, accounts, usage, and the audit log
- [upstream-monitoring](https://github.com/UpstreamCV/upstream-monitoring): Uptime Kuma, Prometheus, and Alertmanager on a separate box, so it stays up when everything else is down
- [upstream-web](https://github.com/UpstreamCV/upstream-web): the marketing site at [upstreamcv.com](https://upstreamcv.com)

### CrowdCount (co-founder & CV lead, Dec 2025–Sep 2026)

Real-time people counting and occupancy analytics, piloted at **25 locations**. I co-founded it with Elkan and a small team. My focus was the models: training YOLO on data we collected ourselves, testing and evaluating each version, and getting the models working in the live counting pipeline. That included tuning ByteTrack and re-ID so tracking held up through bad lighting and occlusion.

The rest of the system:

- [crowdcount-counter](https://github.com/Crowd-Count/crowdcount-counter): the counter device, a Raspberry Pi Zero 2W with a global shutter camera
- [crowdcount-counter-server](https://github.com/Crowd-Count/crowdcount-counter-server): takes in the counter streams and runs detection and counting
- [crowdcount-counter-manager](https://github.com/Crowd-Count/crowdcount-counter-manager): manage a counter from the web
- [crowdcount-ios](https://github.com/Crowd-Count/crowdcount-ios): the iOS app on the App Store
- [crowdcount-web](https://github.com/Crowd-Count/crowdcount-web): the CrowdCount website
- [crowdcount-devtools](https://github.com/Crowd-Count/crowdcount-devtools): internal tool for managing users, counters, and server performance

[Watch the demo](https://youtu.be/wB6bHNOxsBk)

## Tools I use

- **Languages:** Python, TypeScript, SQL, Solidity
- **Data:** PySpark, Databricks, Delta Lake, Postgres, DuckDB, SQLite
- **ML & vision:** YOLO, ByteTrack, OpenCV, DeepStream, scikit-learn, TensorFlow
- **Backend & web:** FastAPI, Flask, Next.js, React, WebSockets
- **Infra & video:** AWS, Docker, Linux, GitHub Actions, SRT/RTSP/WebRTC, MediaMTX, FFmpeg
- **Onchain:** viem, Foundry, Morpho Blue

---

B.S. Statistics & Data Science, CU Boulder ('25), minor in Information Science
