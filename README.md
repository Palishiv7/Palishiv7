<!-- ═══════════════════════════ HEADER ═══════════════════════════ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24c6dc&height=230&section=header&text=Shivam%20Paliwal&fontSize=70&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Backend%20%E2%80%A2%20Distributed%20Storage%20%E2%80%A2%20AI%20Systems&descAlignY=58&descSize=20" width="100%"/>
</p>

<p align="center">
  <a href="https://github.com/Palishiv7">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=800&color=24C6DC&center=true&vCenter=true&width=720&lines=I+build+distributed+systems+%F0%9F%A7%B1;Storage+engines+that+survive+crashes+%F0%9F%92%A5;LLM+agents+that+actually+ship+%F0%9F%A4%96;Voice+AI+with+sub-200ms+latency+%F0%9F%8E%99%EF%B8%8F;MCP+servers+for+humans+%2B+AI+%F0%9F%94%8C" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/📍_Bengaluru,_India-0f0c29?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Currently_@_Couchbase-EA2328?style=for-the-badge&logo=couchbase&logoColor=white"/>
  <img src="https://komarev.com/ghpvc/?username=Palishiv7&style=for-the-badge&color=24c6dc&label=PROFILE+VIEWS"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/shivampaliwal"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:paliwal.shivam42000@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://play.google.com/store/apps/details?id=com.moneypulse.app"><img src="https://img.shields.io/badge/MoneyPulse_on_Play-414141?style=for-the-badge&logo=googleplay&logoColor=white"/></a>
  <a href="https://moneypulse.vercel.app/"><img src="https://img.shields.io/badge/MoneyPulse_Web-000000?style=for-the-badge&logo=vercel&logoColor=white"/></a>
</p>

<!-- ═══════════════════════════ ABOUT ═══════════════════════════ -->
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🧠 `whoami`

```yaml
name:      Shivam Paliwal
role:      Backend / AI Systems Engineer
now:       Couchbase  → storage engine platform & developer infrastructure
           ├── LLM-powered code review wired into the review pipeline
           ├── internal MCP server serving engineering context to humans + AI assistants
           └── fault injection & correctness validation for a production storage engine
before:    PhonePe      → concurrent Java services, core backend platform
           Ingram Micro → Python/SQL data pipelines, GCP migration
motto:     "If it hasn't survived a crash test, it isn't done."
```

## ⚡ What I work on

<table>
<tr>
<td width="50%" valign="top">

### 💾 Distributed storage
Crash recovery · persistence · write-ahead logging · fault injection · correctness under failure

</td>
<td width="50%" valign="top">

### 🤖 LLM systems
Real-time voice pipelines · tool-calling agents · multi-model orchestration · MCP servers · automated code review

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ⚙️ Backend services
Concurrent Java & Python systems · REST APIs · sharded data operations at multi-million-user scale

</td>
<td width="50%" valign="top">

### 📊 Data infrastructure
ETL pipelines · columnar processing · BigQuery · GCP

</td>
</tr>
</table>

<!-- ═══════════════════════════ PROJECTS ═══════════════════════════ -->
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🚀 Selected projects

### 🎙️ VaaniFlow — real-time voice AI platform

> Voice agents for Indian businesses. Callers can interrupt the agent mid-sentence — and it listens.

<p>
  <img src="https://img.shields.io/badge/latency-%3C200ms-24c6dc?style=flat-square"/>
  <img src="https://img.shields.io/badge/barge--in-detection-302b63?style=flat-square"/>
  <img src="https://img.shields.io/badge/providers-10%2B_swappable-ff6f61?style=flat-square"/>
</p>

```mermaid
flowchart LR
    C([📞 Caller]) -->|audio stream| STT
    subgraph STT[🎧 Speech-to-Text]
      D1[Deepgram] ~~~ D2[Sarvam] ~~~ D3[Voxtral]
    end
    STT --> LLM
    subgraph LLM[🧠 Reasoning + Tools]
      L1[Groq] ~~~ L2[OpenAI] ~~~ L3[Anthropic] ~~~ L4[Gemini]
    end
    LLM -->|tool calls| T[(📅 Calendar · Contacts · Booking)]
    LLM --> TTS
    subgraph TTS[🔊 Text-to-Speech]
      S1[Inworld] ~~~ S2[Cartesia] ~~~ S3[Sarvam]
    end
    TTS -->|audio stream| C
    C -. barge-in .-> LLM
```

<details>
<summary><b>🔍 Under the hood</b></summary>
<br>

- Streaming **STT → LLM → TTS** pipeline with sub-200ms latency and barge-in detection
- Every provider is swappable from a single config file without touching business logic
- Tool-calling agent autonomously checks availability, books appointments and looks up contacts, syncing to Google Calendar over OAuth2
- Every call is tracked for cost, latency and turn count

</details>

<img src="https://skillicons.dev/icons?i=ts,nodejs,react,postgres&theme=dark"/> &nbsp; `WebSockets` `AudioWorklet` `Neon` `JWT`

---

<table>
<tr>
<td width="50%" valign="top">

### 💸 MoneyPulse
**Privacy-first expense tracker** — live on Google Play

Reads bank SMS and categorizes transactions **entirely on-device**.

- 🏦 10+ bank & payment-provider formats
- 🎯 95%+ extraction accuracy on messy templates
- 🔐 Room + SQLCipher, AES-256
- 🚫 No cloud sync, no analytics, no third-party servers

<a href="https://play.google.com/store/apps/details?id=com.moneypulse.app"><img src="https://img.shields.io/badge/Get_it_on-Google_Play-34A853?style=for-the-badge&logo=googleplay&logoColor=white"/></a>
<a href="https://moneypulse.vercel.app/"><img src="https://img.shields.io/badge/Website-moneypulse.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white"/></a>

<img src="https://skillicons.dev/icons?i=kotlin,androidstudio&theme=dark"/>
<br><sub>Jetpack Compose · MVVM · Hilt · Coroutines + Flow</sub>

</td>
<td width="50%" valign="top">

### ⚖️ WaapasLao
**Legal notice generation**

Generates jurisdiction-correct legal demand notices as PDFs.

- 🗺️ State-law data + statutory citations
- 🔤 Devanagari script rendering
- ✅ LLM output passes a quality-control gate before any draft goes out

<br>

<img src="https://skillicons.dev/icons?i=ts,react,firebase,vercel&theme=dark"/>
<br><sub>Gemini API</sub>

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### 📈 NSE Paper-Trading Simulator
**Fully unattended paper trading over the Nifty 50** — backtesting, intraday and live paper execution against realistic broker cost models.

`🔁 survives reboots` &nbsp; `🕘 decides on its own if the exchange is open` &nbsp; `🩹 repairs ledger state after a crash` &nbsp; `🌙 runs research overnight`

<img src="https://skillicons.dev/icons?i=python&theme=dark"/> &nbsp; `pandas` `launchd` &nbsp; <sub>Simulation only — no real capital.</sub>

</td>
</tr>
</table>

<!-- ═══════════════════════════ BUILDING NOW ═══════════════════════════ -->
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🔒 What I'm building now

<sub>Most of these repos are private, so only live products have links. Happy to demo any of them on request.</sub>

<table>
<tr>
<td colspan="2" valign="top">

### 💸 MoneyPulse · <sub>🟢 LIVE</sub>
**Your Money, Your Rules.** Privacy-first expense tracker for India that works offline: no ads, no logins, no cloud sync. It reads bank SMS **on the device** and sorts every transaction into a category for you.

<a href="https://play.google.com/store/apps/details?id=com.moneypulse.app"><img src="https://img.shields.io/badge/Get_it_on-Google_Play-34A853?style=for-the-badge&logo=googleplay&logoColor=white"/></a>
<a href="https://moneypulse.vercel.app/"><img src="https://img.shields.io/badge/Website-moneypulse.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white"/></a>

`Kotlin` `Jetpack Compose` `SQLCipher` &nbsp; ✅ *shipped & maintained*

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ⚡ Instapply
AI job-application autofill as a browser extension. One click fills forms on ~30 ATS platforms (Workday, Greenhouse, Lever, Ashby…), scores how well you fit the job, and tailors your résumé to each posting.

`JavaScript` `Manifest V3` &nbsp; 🚧 *building*

</td>
<td width="50%" valign="top">

### 📡 SonarAi
Real-time AI assistant app for the desktop.

`TypeScript` &nbsp; 🚧 *building*

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📈 Chartroom
Local charting workspace built on the open-source Lightweight Charts renderer, with a paper-broker service running in the background. It binds only to localhost, so everything stays on your machine.

`TypeScript` `Vite` `Python` `launchd` &nbsp; 🧪 *personal tool*

</td>
<td width="50%" valign="top">

### 📚 toolbook
Knowledge base for choosing open-source tools: **545 reviewed repos across 39 categories**, each review dated with its evidence. Gives project-aware recommendations and dependency checks for both humans and AI coding agents.

`Python` `Markdown` `YAML` `GitHub Actions` &nbsp; ✅ *active*

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🧸 KidsPlay Factory
<sub>repo: Automation_kids_store</sub><br>
An autonomous loop for kids' screen-free activity products: demand → decide → create → QA → list → sell → measure → learn → repeat. Runs in supervised mode until it's commercially validated.

`TypeScript` `Node.js` &nbsp; 🚧 *building*

</td>
<td width="50%" valign="top">

### 🎙️ VaaniFlow · ⚖️ WaapasLao
VaaniFlow is the voice-agent platform, and WaapasLao generates legal notices. Both are covered in detail under **Selected projects** above.

`TypeScript` `React` `Gemini` &nbsp; 🧪 *in development*

</td>
</tr>
</table>

<!-- ═══════════════════════════ TOOLS ═══════════════════════════ -->
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🛠️ Toolbox

<p align="center"><b>Languages</b></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=python,java,ts,kotlin,c,bash&theme=dark&perline=6"/>
</p>

<p align="center"><b>Data & Storage</b></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=postgres,firebase&theme=dark"/>
  <br>
  <img src="https://img.shields.io/badge/Couchbase-EA2328?style=for-the-badge&logo=couchbase&logoColor=white"/>
  <img src="https://img.shields.io/badge/BigQuery-669DF6?style=for-the-badge&logo=googlebigquery&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQLCipher-003B57?style=for-the-badge&logo=sqlite&logoColor=white"/>
</p>

<p align="center"><b>Infra & Tooling</b></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=gcp,docker,jenkins,linux,vercel,grafana&theme=dark&perline=6"/>
  <br>
  <img src="https://img.shields.io/badge/Gerrit-EEEEEE?style=for-the-badge&logo=gerrit&logoColor=black"/>
</p>

<p align="center"><b>AI</b></p>
<p align="center">
  <img src="https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white"/>
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=claude&logoColor=white"/>
  <img src="https://img.shields.io/badge/Anthropic-191919?style=for-the-badge&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white"/>
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white"/>
  <img src="https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logoColor=white"/>
</p>

<!-- ═══════════════════════════ STATS ═══════════════════════════ -->
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 📊 GitHub pulse

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Palishiv7&theme=tokyonight&hide_border=true&background=0D1117&ring=24C6DC&fire=FF6F61&currStreakLabel=24C6DC" width="70%"/>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Palishiv7/Palishiv7/output/github-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Palishiv7/Palishiv7/output/github-snake.svg"/>
    <img alt="contribution snake" src="https://raw.githubusercontent.com/Palishiv7/Palishiv7/output/github-snake.svg"/>
  </picture>
</p>

> [!NOTE]
> Most of my code lives in private repositories — client work, unreleased projects, and everything at my employer, which runs on Gerrit rather than GitHub. **The public repo list here is thin by design, not by inactivity.**

<!-- ═══════════════════════════ FOOTER ═══════════════════════════ -->
<p align="center">
  <b>Happy to walk through architecture and tradeoffs on any of the above.</b><br><br>
  <a href="https://linkedin.com/in/shivampaliwal"><img src="https://img.shields.io/badge/Let's_talk_on-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:paliwal.shivam42000@gmail.com"><img src="https://img.shields.io/badge/Drop_a-Mail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24c6dc,50:302b63,100:0f0c29&height=120&section=footer" width="100%"/>
