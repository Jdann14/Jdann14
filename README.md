# Josh D'Annunzio

**Software engineer · Data engineer · Applied AI & computer vision**

I'm a software engineer and founder based in Boulder, Colorado. I build systems that turn raw data and live video into useful, reliable applications—from federal healthcare data pipelines to computer vision platforms and AI developer tools.

My work spans model training and evaluation, real-time inference, backend APIs, distributed data processing, and full-stack product development. I care about what happens after deployment: data quality, observability, recovery, and making results easy to inspect.

## What I'm working on

### Upstream Vision — Founder & Software Engineer
*May 2026–present*

Building infrastructure to help teams deploy, monitor, and improve live-camera AI workflows.

- Developed camera-agent and control-plane workflows for secure video ingestion, stream validation, heartbeats, reconnection, and frame sampling.
- Built with Python, FastAPI, Docker, PostgreSQL/Supabase, and SRT/MediaMTX, with WebRTC playback and a Next.js operator dashboard.
- Working across model serving, camera-health monitoring, model-output reliability, and rules/event workflows, including APIs, webhooks, and audit/replay.

[Website](https://upstreamcv.com) · [Public architecture notes and roadmap](https://github.com/Jdann14/upstream-architecture-notes)

### CrowdCount — Co-Founder & Computer Vision Lead
*December 2025–present*

Co-founded a real-time people-counting and occupancy analytics platform piloted at **25 locations**, owning the pipeline from camera ingestion to inference, tracking, and analytics.

- Trained YOLO models on self-collected data and improved performance through model evaluation, reflection filtering, and low-light preprocessing.
- Tuned ByteTrack and re-identification recovery for tracking continuity across changing lighting, camera angles, and occlusion.
- Built Python/Flask services, GPU-aware batched inference, SQLite-backed outage queues, and automatic stalled-camera recovery across Raspberry Pi/GPU infrastructure.

[Watch the demo](https://youtu.be/wB6bHNOxsBk)

### RELI Group — Software Engineer / Data Analyst
*May 2024–present*

Develop and support production data workflows for Centers for Medicare & Medicaid Services (CMS) healthcare initiatives.

- Build, validate, and troubleshoot ETL/ELT pipelines with Python, PySpark, Spark SQL, Databricks, Delta Lake, and AWS.
- Translate reporting requirements into reusable transformations and investigate discrepancies through SQL/Python analysis, reconciliation, and data-quality checks.
- Support releases with Git, Jenkins CI/CD, testing, technical documentation, and collaboration across engineering, QA, and business teams.

## Selected public projects

| Project | What it does |
| --- | --- |
| **[Tracework](https://github.com/Jdann14/tracework)** | An inspectable AI data workspace with versioned SQL pipelines, durable execution, data-quality checks, evidence, and run comparisons. Built with FastAPI, DuckDB, SQLite, and React/TypeScript. |
| **[Beacon](https://github.com/Jdann14/beacon)** | A local-first control center for AI coding agents, combining a CLI, session management, SQLite-backed history, and a live React dashboard over WebSockets. |
| **[srt-bench](https://github.com/Jdann14/srt-bench)** | An early live-video ingest benchmark tool with an SRT loopback runner and time-to-first-frame measurement. Additional transports and network-condition testing are planned. |

## Technical skills

| Area | Tools and experience |
| --- | --- |
| **Languages** | Python, SQL, PySpark, Spark SQL, JavaScript, TypeScript, HTML/CSS |
| **Data engineering** | Databricks, Apache Spark, Delta Lake, ETL/ELT, data modeling, validation, reconciliation, Pandas, NumPy |
| **Machine learning & vision** | OpenCV, YOLO, ByteTrack, ReID, TensorFlow, scikit-learn, model training and evaluation, statistical analysis, real-time and batched inference |
| **Backend & applications** | FastAPI, Flask, REST APIs, WebSockets, webhooks, React, Next.js |
| **Databases** | PostgreSQL/Supabase, SQLite, DuckDB |
| **Cloud & delivery** | AWS, AWS EMR, Docker, Linux, Git, GitHub Actions, Jenkins, CI/CD, automated testing, observability |
| **Video systems** | MediaMTX, FFmpeg, SRT, RTSP, WebRTC, Raspberry Pi, GPU processing |
| **AI development workflows** | Model integration, tool-driven AI workflows, Claude Code, Codex CLI, AI-assisted debugging and rapid prototyping |

## Education

**University of Colorado Boulder**  
B.S. in Statistics and Data Science, 2025 · Minor in Information Science

Interested in building reliable AI applications, data platforms, and developer tools.
