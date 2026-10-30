# Hey, I'm Josh

I'm a software engineer in Boulder, CO. I like building systems that take messy real-world data (live video, healthcare records, and lately on-chain lending markets) and turn it into something reliable. My day job is data engineering. Outside of that I'm usually deep in some side project.

## What I'm building now: a Morpho liquidation bot

*Private for now, but it's what I spend most of my time on.*

It's a bot that watches [Morpho Blue](https://morpho.org) lending markets and liquidates unhealthy positions to earn the liquidation bonus. It runs live and competes against other bots, so being fast and being safe both matter.

- Keeps a local mirror of every position, built from on-chain events, and computes health locally. The only network call between "this position is liquidatable" and "transaction sent" is the send itself.
- Its Solidity contract enforces the outcome on-chain: whitelisted markets and routers, balance checks before and after every swap, minimum-profit floors, and profit sent to a separate treasury wallet in the same transaction.
- Guardrails include gas caps, auto-pause, a kill switch, and Telegram alerts. New markets run in shadow mode before they go live.
- Testing uses a lot of replays: mainnet fork tests, recorded price-crash replays, and fuzz tests on the contract.

**Stack:** TypeScript, viem, Solidity, Foundry, AWS

## Day job: RELI Group

Since May 2024 I've done software and data engineering on healthcare data for the Centers for Medicare & Medicaid Services (CMS). I build and debug ETL pipelines in PySpark and Databricks on AWS, track down why numbers don't match, and help keep releases boring.

## Previously

### Upstream Vision (founder, May–Sep 2026)

A reliability layer for computer vision in production. It streamed video from real cameras, ran detection on it, and told operators when and why detection quality slipped. I built most of the platform, from the camera agent all the way to the status page.

- [upstream-agent](https://github.com/UpstreamCV/upstream-agent): pip-installable Python agent that reads a camera feed and streams it securely to Upstream
- [upstream-streaming-server](https://github.com/UpstreamCV/upstream-streaming-server): accepts, validates, routes, and monitors incoming video streams (SRT + MediaMTX)
- [upstream-processor](https://github.com/UpstreamCV/upstream-processor): runs one worker per stream, including NVIDIA DeepStream inference
- [upstream-api-server](https://github.com/UpstreamCV/upstream-api-server): control plane for accounts, agents, cameras, and stream sessions (FastAPI + Postgres)
- [upstream-dashboard](https://github.com/UpstreamCV/upstream-dashboard): operator dashboard with live video (Next.js + Supabase Auth)
- [upstream-admin-panel](https://github.com/UpstreamCV/upstream-admin-panel): internal admin tool for system health, accounts, usage, and the audit log
- [upstream-monitoring](https://github.com/UpstreamCV/upstream-monitoring): Uptime Kuma, Prometheus, and Alertmanager on a separate box, so it stays up when everything else is down
- [upstream-web](https://github.com/UpstreamCV/upstream-web): the marketing site at [upstreamcv.com](https://upstreamcv.com)

### CrowdCount (co-founder & CV lead, Dec 2025–Sep 2026)

Real-time people counting and occupancy analytics, piloted at **25 locations**. I owned the computer vision pipeline. I trained YOLO models on data we collected ourselves and tuned ByteTrack and re-ID to keep tracking people through bad lighting and occlusion. I also built the server that takes in Raspberry Pi camera feeds and runs batched GPU inference.

- [crowdcount-counter-server](https://github.com/Crowd-Count/crowdcount-counter-server): ingests the Pi camera streams and does the counting
- [Watch the demo](https://youtu.be/wB6bHNOxsBk)

## Tools I use

- **Languages:** Python, TypeScript, SQL, Solidity
- **Data:** PySpark, Databricks, Delta Lake, Postgres, DuckDB, SQLite
- **ML & vision:** YOLO, ByteTrack, OpenCV, DeepStream, scikit-learn, TensorFlow
- **Backend & web:** FastAPI, Flask, Next.js, React, WebSockets
- **Infra & video:** AWS, Docker, Linux, GitHub Actions, SRT/RTSP/WebRTC, MediaMTX, FFmpeg
- **Onchain:** viem, Foundry, Morpho Blue

---

B.S. Statistics & Data Science, CU Boulder ('25), minor in Information Science
