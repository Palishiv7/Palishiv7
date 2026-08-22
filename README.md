# Shivam Paliwal

**Backend / AI Systems Engineer — Bengaluru, India**

I build distributed systems and the developer tooling around them.

Currently at **Couchbase**, working on storage engine platform and developer
infrastructure: LLM-powered code review wired into the review pipeline, an internal
MCP (Model Context Protocol) server that serves engineering context to both humans
and AI coding assistants, and fault-injection and correctness validation for a
production storage engine.

Previously **PhonePe** (concurrent Java services on the core backend platform) and
**Ingram Micro** (Python/SQL data pipelines, GCP migration).

---

## What I work on

**Distributed storage** — crash recovery, persistence, write-ahead logging, fault
injection, correctness under failure
**LLM systems** — real-time voice pipelines, tool-calling agents, multi-model
orchestration, MCP servers, automated code review
**Backend services** — concurrent Java and Python systems, REST APIs, sharded data
operations at multi-million-user scale
**Data infrastructure** — ETL pipelines, columnar processing, BigQuery, GCP

---

## Selected projects

### VaaniFlow — real-time voice AI platform
A voice agent platform for Indian businesses. Streaming **STT → LLM → TTS** pipeline
with sub-200ms latency and barge-in detection, so callers can interrupt the agent
mid-sentence.

The provider layer is fully pluggable — Deepgram, Sarvam, and Voxtral for speech
recognition; Groq, OpenAI, Anthropic, and Gemini for reasoning; Inworld, Cartesia,
and Sarvam for synthesis — swappable from a single config file without touching
business logic. A tool-calling agent autonomously checks availability, books
appointments, and looks up contacts, syncing to Google Calendar over OAuth2.
Every call is tracked for cost, latency, and turn count.

`TypeScript` · `Node.js` · `WebSockets` · `AudioWorklet` · `Neon PostgreSQL` · `JWT` · `React`

### MoneyPulse — privacy-first expense tracker
Android app on the Google Play Store that detects and categorizes transactions from
SMS entirely on-device. Parses **10+ bank and payment-provider formats** at 95%+
extraction accuracy across malformed and heterogeneous templates. Room + SQLCipher
with AES-256 encryption; no cloud sync, no analytics, no third-party servers — every
transaction stays on the phone.

[Google Play](https://play.google.com/store/apps/details?id=com.moneypulse.app) ·
`Kotlin` · `Jetpack Compose` · `Clean Architecture / MVVM` · `Hilt` · `Coroutines + Flow`

### WaapasLao — legal notice generation
Generates jurisdiction-correct legal demand notices as PDFs, with state-law data,
statutory citation handling, and Devanagari script rendering. LLM generation runs
behind a quality-control gate rather than emitting drafts unchecked.

`TypeScript` · `React` · `Firebase` · `Vercel` · `Gemini API`

### NSE Paper-Trading Simulator
Fully unattended paper-trading system over the Nifty 50 universe — backtesting,
intraday, and live paper execution against realistic broker cost models. Runs on a
scheduled agent that survives reboots, decides on its own whether the exchange is
open, repairs ledger state after a crash, and runs research overnight. Simulation
only; no real capital.

`Python` · `launchd` · `pandas`

---

## Tools

`Python` `Java` `TypeScript` `Kotlin` `SQL` `C` `Bash`
`Couchbase` `PostgreSQL` `BigQuery` `Room/SQLCipher`
`GCP` `Docker` `Jenkins` `Gerrit` `Firebase` `Vercel` `Linux`
`MCP` `Claude Code` `Grafana`

---

## A note on this profile

Most of my code lives in private repositories — client work, unreleased projects, and
everything at my employer, which runs on Gerrit rather than GitHub. The public repo
list here is thin by design, not by inactivity.

Happy to walk through architecture and tradeoffs on any of the above.

**[LinkedIn](https://linkedin.com/in/shivampaliwal)** · paliwal.shivam42000@gmail.com
