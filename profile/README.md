# TRV Enterprises

Hi — I'm **Tom Viviano**. I've been designing and building software for over
50 years, from FORTRAN on punch cards and a custom ISAM file system in the
70s through to my last role as Chief Designer and Co-Chief Architect on
**IBM Hybrid Cloud Mesh**, IBM's cloud network management product.

I retired from IBM in 2024, took a year away, and came back because I missed building things. I learned about Claude Code and MCP servers at IBM's TechXchange in 2025 and have been vibing ever since. This organization is where I publish the open-source
projects I build — partly as a contribution to the communities I draw from,
and partly as a working portfolio of how I think about systems.

Everything here is released under the **Apache License 2.0**.

## Core Projects

### [trv-outpost](https://github.com/trv-enterprises/trv-outpost)
A full-stack **dashboard platform** for building, managing, and viewing
real-time data visualizations — with an AI-assisted component builder.

- **Design / View / Manage** modes — build connections, charts, and layouts; view with live auto-refresh; administer the system 
- **10 datasource types** behind one unified adapter pattern: SQL, REST, CSV, WebSocket, MQTT, ts-store, Prometheus, and EdgeLake
- **AI Chart Builder** — natural language to ECharts, streamed live over
  SSE, with an embedded MCP server for AI-driven chart and dashboard generation
- **Chart code stored in the database** and evaluated at runtime — no build-and-deploy cycle for new components
- Go + Gin backend, React 18 + Carbon Design System frontend, MongoDB for storage.

### [ts-store](https://github.com/trv-enterprises/ts-store)
A lightweight, embedded time-series store with a **predictable storage
footprint** — built for the edge. You set the size at creation and it never
grows: when the buffer fills, the oldest data is reclaimed automatically.
No retention policies to tune, no unbounded disk usage.

- **Store-and-forward** for time-series data at the edge
- **Fixed disk budget** via a circular-buffer / partitioned architecture
- **Raw data preserved** — no lossy downsampling
- **O(log n)** nanosecond-timestamp lookups; query by time, newest, oldest,
  since-duration, or range
- **Zero external dependencies** — a single Go binary and flat files
- Connectors in and out: REST, WebSocket, Unix socket, and MQTT, with
  aggregation (avg/sum/min/max), a rule-based alerting engine, cursor
  persistence, and auto-reconnect


## Built with Claude Code

Both of these projects were developed with **Claude Code** as a collaborator
across the whole lifecycle — design consultation, development, documentation,
testing, and deployment. After four decades of doing this work, I came in
skeptical and have been genuinely surprised by the productivity gains. It
hasn't replaced the architecture and judgment; it's amplified them, and let
me ship real, well-tested, well-documented systems on my own.

## Get in touch

- 📫 [tom.viviano@trv-enterprises.com](mailto:tom.viviano@trv-enterprises.com)
- 💬 Questions about either project? Open an issue on the repo.
