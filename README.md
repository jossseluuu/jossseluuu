<div align="center">

<img src="assets/banner-dark.png#gh-dark-mode-only" alt="José Luis López" width="100%">
<img src="assets/banner-light.png#gh-light-mode-only" alt="José Luis López" width="100%">

# Hi, I'm José Luis López 👋

<a href="https://github.com/jossseluuu">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=58A6FF&center=true&vCenter=true&width=660&lines=Final-year+Computer+Science+%26+Engineering+student;Backend+%C2%B7+Applied+AI+%C2%B7+Security;Building+multi-agent+systems+and+AI+air+traffic+controllers;Explaining+how+everyday+tech+really+works" alt="Final-year Computer Science & Engineering student · Backend · Applied AI · Security" />
</a>

<p>
  <a href="https://www.linkedin.com/in/joseluislop/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:jossseluuu@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://www.instagram.com/jossseluuu"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram"></a>
</p>

<p>
  <a href="https://github.com/jossseluuu/jossseluuu/raw/main/assets/cv/JoseLuisLopez_CV_EN.pdf"><img src="https://img.shields.io/badge/Download_CV-English-2EA043?style=for-the-badge&logo=readdotcv&logoColor=white" alt="Download CV in English"></a>
  <a href="https://github.com/jossseluuu/jossseluuu/raw/main/assets/cv/JoseLuisLopez_CV_ES.pdf"><img src="https://img.shields.io/badge/Descargar_CV-Español-2EA043?style=for-the-badge&logo=readdotcv&logoColor=white" alt="Descargar CV en español"></a>
</p>

<sub><b>EN</b> English · <b>ES</b> <a href="#es">Versión en español</a></sub>

</div>

---

## 👨‍💻 About Me

I'm a **final-year Computer Science & Engineering student** at the **Universidad de Granada (UGR)**, Spain.

I spent a **full academic year at the University of Montana (USA)** through an international mobility program, where I also **worked in the United States**. That year taught me to study, work and solve problems in English, inside teams with very different backgrounds and ways of working, and made me more independent, adaptable and comfortable with responsibility.

I build software that is **useful, secure and easy to reason about**, and I like to prove what I learn with complete projects.

**What I'm working on**<br>
🏢 **[CompanyAgentsHQ](https://github.com/jossseluuu/CompanyAgentsHQ)**: a company run by AI agents that you manage from a live isometric office.<br>
🛫 **[openScope](https://github.com/jossseluuu/openScope)**: AI bots that act as air traffic controllers, one built on expert rules and optimisation, the other on reinforcement learning.<br>
🔐 **[I-CPU](https://github.com/jossseluuu/I-CPU)**: encrypted steganography in modern C++, with built-in steganalysis.<br>
📡 **[HowThingsTalk](https://github.com/jossseluuu/HowThingsTalk)**: a bilingual library on how everyday devices really work, with **a new article every weekday**.

**How I work**<br>
📐 **I design before I code.** Specs, requirements and written architecture decisions (ADRs) come first, so the code has a clear target and every trade-off is documented.<br>
📏 **I measure instead of guessing.** My projects ship with their own evaluation: steganalysis and distortion metrics in I-CPU, safety and efficiency metrics for the openScope bots, cost tracking in CompanyAgentsHQ.<br>
🛡️ **I treat safety as a feature.** Approval steps, safety shields, least privilege and audit trails are part of the design, not something added at the end.<br>
✅ **I finish what I start.** Tests, CI, documentation and a one-command setup are part of "done".<br>
🗣️ **I explain things clearly.** I write technical content in English and Spanish every weekday, for beginners and experts at the same time.<br>
🌍 **I adapt fast.** A year studying and working in the US taught me to get up to speed quickly in new teams, cultures and codebases.

---

## 🚀 Featured Projects

### 🏢 [CompanyAgentsHQ](https://github.com/jossseluuu/CompanyAgentsHQ) · AI agents as a real company
<sub>Personal project · 🚧 in active development</sub>

You give a goal to a **CEO agent**; it plans it, delegates it to departments, supervisors review the work and everything ends up archived, all inside a **2.5D isometric office** where you can watch the agents work.<br>
• **Real org chart** with supervision, escalation and an **approval inbox** for sensitive actions<br>
• **RAG knowledge bases** per company, department, room or agent, with source citations<br>
• **Hash-chained audit log**, an independent **Auditor agent** and **per-agent AI budgets**

<details>
<summary><b>How it works</b></summary>
<br>

**The problem.** Multi-agent AI systems are usually black boxes: they're configured in code, followed through logs, and it's hard to tell who did what, where each document ended up and how much it cost.

**The idea.** CompanyAgentsHQ turns them into a company you can see. 8 agents (CEO, Chief of Staff, CMO, CTO, CFO, two specialists and an Auditor) work in configurable rooms, each with its own modules: file cabinet, task board, finance dashboard, rest area… Agents walk between rooms (A* pathfinding) according to what they're doing.<br>
• **Supervision rules** per relationship and action type: result review, prior approval and escalation to the owner<br>
• **Append-only audit log** where each event includes the hash of the previous one; the Auditor flags unusual spending, loops and repeated permission denials, and can pause an agent<br>
• **Daily AI spending cap** that stops work when it's reached, and a fake LLM mode to develop and test at zero cost<br>
• **Modular monolith**: room modules are plugins; agent work runs in a separate worker over Redis and streams to the browser via WebSockets<br>
• **Swappable LLM provider** behind its own interface (Claude, OpenAI or local models via Ollama)<br>
• Designed from a full specification: **160+ functional and 60+ non-functional requirements**, all measurable

</details>

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"> <img src="https://img.shields.io/badge/Three.js_/_R3F-000000?style=flat-square&logo=threedotjs&logoColor=white"> <img src="https://img.shields.io/badge/PostgreSQL_+_pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"> <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">

---

### 🛫 [openScope](https://github.com/jossseluuu/openScope) · AI air traffic controllers
<sub>Open-source fork · JavaScript + Python</sub>

On top of the open-source **openScope** ATC simulator, I built **two AI bots that control all the traffic of an airport**, arrivals, departures and conflicts, using only the same commands a human controller would give.<br>
• **Bot A**: expert rules + optimisation: arrival/departure sequencing (AMAN/DMAN), vectors, holds and conflict resolution, with parameters tuned by **CMA-ES**<br>
• **Bot B**: **reinforcement learning (PPO)** in PyTorch with curriculum learning, pre-trained by **imitating Bot A (DAgger)**, exported to **ONNX** to run in the browser<br>
• Both are bound by real **ICAO, EASA (RECAT-EU) and FAA rules** and a shared **safety shield**

<details>
<summary><b>How it works</b></summary>
<br>

- **Headless simulator** that runs the game without a browser, with seeded randomness, a **Bot API** and a **Python bridge** exposed as a **Gymnasium-style environment**
- **Operational realism layer**: regulatory profiles per airport, wake turbulence separation, runway wind limits, terrain clearance and taxi times, with rules ranked by priority (safety → separation → procedure → efficiency)
- **Explainable decisions**: every command Bot A gives comes with its reason
- **Audit page** that records each game step by step and exports it to train Bot B
- **New airports**: Madrid-Barajas (**LEMD**) and Málaga (**LEMG**), with terrain data and airport guides
- In the game, type `bot a`, `bot b` or `bot off` to hand over or take back control
- Unit tests for the bots, the safety shield and the realism rules; Bot B's full training run is the next step

</details>

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"> <img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white"> <img src="https://img.shields.io/badge/Reinforcement_learning_(PPO)-6E40C9?style=flat-square"> <img src="https://img.shields.io/badge/CMA--ES-6E40C9?style=flat-square"> <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white">

---

### 🔐 [I-CPU](https://github.com/jossseluuu/I-CPU) · Encrypted steganography
<sub>Applied cryptography · C++20</sub>

Hides a text or a whole file inside an image so that, **without the password, it can't be read or even proven to exist**, and then measures how detectable the result is.<br>
• **Three hiding domains**: pixel bits (PNG, BMP…), **JPEG DCT coefficients** without recompression and **GIF palette indices**<br>
• **Argon2id + XChaCha20-Poly1305**, with password-derived positions and an **encrypted header**<br>
• **Built-in steganalysis** (chi-square, RS analysis) and distortion metrics (PSNR, SSIM)

<details>
<summary><b>How it works</b></summary>
<br>

- It picks the hiding technique based on the output format, encrypts everything before writing it, and leaves nothing recognisable in the image: without the password there's no header, no signature and no pattern to look for
- Animated GIFs are supported in the palette domain, and JPEG images keep their original compression
- Steganalysis (chi-square, RS analysis, DCT chi-square) lets you compare configurations with real numbers instead of guessing
- **Two interfaces**: a CLI with a guided mode, and an **offline local web GUI** with a before/after slider, difference view, pixel magnifier and live capacity meter
- **Engineering**: CMake presets, automated tests, CI and architecture decision records (ADRs)

</details>

<img src="https://img.shields.io/badge/C++20-00599C?style=flat-square&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white"> <img src="https://img.shields.io/badge/Argon2id_·_XChaCha20--Poly1305-000000?style=flat-square&logo=letsencrypt&logoColor=white"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">

---

### 📡 [HowThingsTalk](https://github.com/jossseluuu/HowThingsTalk) · How everyday devices really work
<sub>Technical writing · ES / EN · new article every weekday</sub>

A growing library that explains **how the devices we use every day work underneath**: phones, laptops, earbuds, watches, speakers, cards, light bulbs and cars. Each article answers **one concrete question**, in Spanish and English.<br>
• **Four layers of depth** per article, so beginners can stop early and experts can go all the way down<br>
• From an everyday analogy (and exactly where it breaks) to protocols, data frames, radio spectrum and real physical numbers<br>
• Timeless on purpose: no news, no reviews, no buying advice

<details>
<summary><b>The four layers</b></summary>
<br>

1. **The question and the depth** it requires, plus the prior knowledge needed
2. **The short answer**: one sentence plus a 60-second summary
3. **The mental model**: an everyday analogy, and the exact point where it breaks
4. **The technical mechanism**: flow diagrams, data frames, protocols, radio spectrum and the real physical numbers

</details>

<img src="https://img.shields.io/badge/Markdown-000000?style=flat-square&logo=markdown&logoColor=white"> <img src="https://img.shields.io/badge/Technical_writing-6E40C9?style=flat-square"> <img src="https://img.shields.io/badge/Networking_·_Radio_·_Hardware-0A66C2?style=flat-square">

---

### 📈 [InvestDashboard](https://github.com/jossseluuu/InvestDashboard) · Personal investment dashboard
<sub>Full-stack · Flask + React</sub>

Tracks an investment portfolio in one place: holdings, real-time prices, performance over time and market news.<br>
• **Real-time prices** and **multi-currency** support with live exchange rates and a fallback provider<br>
• **Per-asset market data**: fundamentals, analyst ratings, earnings with EPS surprises, dividends and news<br>
• **Background jobs**, CSV import/export and optional **weekly Telegram alerts**

<details>
<summary><b>More details</b></summary>
<br>

- Charts for portfolio value and P&L over time, per-ticker price history and allocation
- Market data from yFinance, exchange rates from SerpAPI with yFinance as fallback, news from Finnhub
- SQLite in WAL mode with zero-data-loss migrations, scheduled jobs with APScheduler
- Dark mode that respects the system preference
- Deployment-ready: backend on Railway and frontend on Vercel

</details>

<img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white"> <img src="https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white">

---

<sub>More: 🧮 <a href="https://github.com/jossseluuu/DataStructures-Algorithms">DataStructures-Algorithms</a> (data structures from scratch in C++, with tests) · ✈️ <a href="https://github.com/jossseluuu/airline-database-project">airline-database-project</a> (relational model for airline operations: pilots, crews, flights, aircraft, maintenance)</sub>

---

## 🛠️ Tech Stack

| Area | Daily use | Worked with |
|---|---|---|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![C++](https://img.shields.io/badge/C++20-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) | ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS](https://img.shields.io/badge/CSS-663399?style=flat-square&logo=css&logoColor=white) |
| **Backend** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white) ![REST](https://img.shields.io/badge/REST_APIs-0A66C2?style=flat-square) | ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white) ![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socketdotio&logoColor=white) ![OpenAPI](https://img.shields.io/badge/OpenAPI-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) | ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js_/_R3F-000000?style=flat-square&logo=threedotjs&logoColor=white) ![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white) ![Zustand](https://img.shields.io/badge/Zustand-443E38?style=flat-square) ![React Router](https://img.shields.io/badge/React_Router-CA4245?style=flat-square&logo=reactrouter&logoColor=white) ![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) | ![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![MinIO / S3](https://img.shields.io/badge/MinIO_/_S3-C72E49?style=flat-square&logo=minio&logoColor=white) |
| **AI / ML** | ![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI_/_ChatGPT-412991?style=flat-square&logo=openai&logoColor=white) ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white) ![Prompt engineering](https://img.shields.io/badge/Prompt_engineering-6E40C9?style=flat-square) ![Agents](https://img.shields.io/badge/LLM_agents_&_tool_use-6E40C9?style=flat-square) | ![Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![GitHub Copilot](https://img.shields.io/badge/GitHub_Copilot-000000?style=flat-square&logo=githubcopilot&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)<br>![RAG](https://img.shields.io/badge/RAG-6E40C9?style=flat-square) ![MCP](https://img.shields.io/badge/MCP-6E40C9?style=flat-square) ![Embeddings](https://img.shields.io/badge/Embeddings_&_vector_search-6E40C9?style=flat-square) ![RL](https://img.shields.io/badge/Reinforcement_learning-6E40C9?style=flat-square) ![Metaheuristics](https://img.shields.io/badge/Metaheuristics_(CMA--ES)-6E40C9?style=flat-square) |
| **Security** | ![Crypto](https://img.shields.io/badge/Applied_cryptography-000000?style=flat-square&logo=letsencrypt&logoColor=white) ![OWASP](https://img.shields.io/badge/OWASP_Top_10-000000?style=flat-square&logo=owasp&logoColor=white) ![LLM security](https://img.shields.io/badge/LLM_security_(prompt_injection)-000000?style=flat-square) | ![Stego](https://img.shields.io/badge/Steganography_&_steganalysis-000000?style=flat-square) ![Threat modeling](https://img.shields.io/badge/Threat_modeling-000000?style=flat-square) ![Secure SDLC](https://img.shields.io/badge/Secret_&_dependency_scanning-000000?style=flat-square)<br>![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white) ![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white) ![Nmap](https://img.shields.io/badge/Nmap-4682B4?style=flat-square) ![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white) ![Hack The Box](https://img.shields.io/badge/Hack_The_Box-9FEF00?style=flat-square&logo=hackthebox&logoColor=black) |
| **DevOps & Quality** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) | ![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white) ![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white) ![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white) |

---

## 📊 GitHub Activity

<div align="center">

<img src="./profile-summary-card-output/github_dark/0-profile-details.svg#gh-dark-mode-only" alt="Contributions over time" width="100%">
<img src="./profile-summary-card-output/github/0-profile-details.svg#gh-light-mode-only" alt="Contributions over time" width="100%">

<img src="./profile-summary-card-output/github_dark/3-stats.svg#gh-dark-mode-only" alt="GitHub stats" width="49%">
<img src="./profile-summary-card-output/github/3-stats.svg#gh-light-mode-only" alt="GitHub stats" width="49%">
<img src="./profile-summary-card-output/github_dark/4-productive-time.svg#gh-dark-mode-only" alt="Commits by time of day" width="49%">
<img src="./profile-summary-card-output/github/4-productive-time.svg#gh-light-mode-only" alt="Commits by time of day" width="49%">

<img src="./profile-summary-card-output/github_dark/2-most-commit-language.svg#gh-dark-mode-only" alt="Most committed languages" width="49%">
<img src="./profile-summary-card-output/github/2-most-commit-language.svg#gh-light-mode-only" alt="Most committed languages" width="49%">
<img src="./profile-summary-card-output/github_dark/1-repos-per-language.svg#gh-dark-mode-only" alt="Repositories per language" width="49%">
<img src="./profile-summary-card-output/github/1-repos-per-language.svg#gh-light-mode-only" alt="Repositories per language" width="49%">

<img src="https://raw.githubusercontent.com/jossseluuu/jossseluuu/output/github-snake-dark.svg#gh-dark-mode-only" alt="Contribution graph being eaten by a snake" width="100%">
<img src="https://raw.githubusercontent.com/jossseluuu/jossseluuu/output/github-snake.svg#gh-light-mode-only" alt="Contribution graph being eaten by a snake" width="100%">

</div>

---

<a id="es"></a>

## 🌐 Versión en español (ES)

<details>
<summary><b>Haz clic para leer mi perfil completo en español</b></summary>
<br>

### 👨‍💻 Sobre mí

Soy **estudiante de último curso de Ingeniería Informática** en la **Universidad de Granada (UGR)**.

Pasé **un curso académico completo en la University of Montana (EE. UU.)** gracias a un programa de movilidad internacional, donde además **trabajé en Estados Unidos**. Ese año me enseñó a estudiar, trabajar y resolver problemas en inglés, dentro de equipos con orígenes y formas de trabajar muy distintas, y me hizo más autónomo, adaptable y acostumbrado a asumir responsabilidades.

Construyo software **útil, seguro y fácil de razonar**, y me gusta demostrar lo que aprendo con proyectos completos.

**En qué estoy trabajando**<br>
🏢 **[CompanyAgentsHQ](https://github.com/jossseluuu/CompanyAgentsHQ)**: una empresa formada por agentes de IA que diriges desde una oficina isométrica en tiempo real.<br>
🛫 **[openScope](https://github.com/jossseluuu/openScope)**: bots de IA que hacen de controladores aéreos, uno basado en reglas expertas y optimización y otro en aprendizaje por refuerzo.<br>
🔐 **[I-CPU](https://github.com/jossseluuu/I-CPU)**: esteganografía cifrada en C++ moderno, con estegoanálisis integrado.<br>
📡 **[HowThingsTalk](https://github.com/jossseluuu/HowThingsTalk)**: una biblioteca bilingüe sobre cómo funcionan de verdad los aparatos del día a día, con **un artículo nuevo cada día laborable**.

**Cómo trabajo**<br>
📐 **Diseño antes de programar.** Primero especificación, requisitos y decisiones de arquitectura por escrito (ADRs), para que el código tenga un objetivo claro y cada decisión quede documentada.<br>
📏 **Mido en lugar de suponer.** Mis proyectos incluyen su propia evaluación: estegoanálisis y métricas de distorsión en I-CPU, métricas de seguridad y eficiencia para los bots de openScope, control de costes en CompanyAgentsHQ.<br>
🛡️ **La seguridad es parte del producto.** Aprobaciones, escudos de seguridad, mínimo privilegio y trazabilidad forman parte del diseño desde el principio.<br>
✅ **Termino lo que empiezo.** Tests, CI, documentación e instalación con un solo comando son parte de "terminado".<br>
🗣️ **Explico con claridad.** Escribo divulgación técnica en español y en inglés cada día laborable, para principiantes y expertos a la vez.<br>
🌍 **Me adapto rápido.** Un año estudiando y trabajando en EE. UU. me enseñó a ponerme al día enseguida en equipos, culturas y códigos nuevos.

### 🚀 Proyectos destacados

**🏢 [CompanyAgentsHQ](https://github.com/jossseluuu/CompanyAgentsHQ) · Agentes de IA como una empresa real** · <sub>proyecto personal en desarrollo</sub>

Das un objetivo al **agente CEO**, que lo planifica y lo reparte entre departamentos; los supervisores revisan el trabajo y todo queda archivado y es buscable, dentro de una **oficina isométrica 2.5D** donde ves trabajar a los agentes.<br>
• **Organigrama real** con supervisión, escalado y **bandeja de aprobaciones** para acciones sensibles<br>
• **Bases de conocimiento RAG** por empresa, departamento, sala o agente, con citas de las fuentes<br>
• **Registro de auditoría encadenado con hashes**, un **agente Auditor** independiente y **presupuesto de IA por agente**<br>
• Diseñado a partir de una especificación completa: **más de 160 requisitos funcionales y 60 no funcionales**, todos medibles

**🛫 [openScope](https://github.com/jossseluuu/openScope) · Controladores aéreos con IA** · <sub>fork de código abierto · JavaScript + Python</sub>

Sobre el simulador de control aéreo **openScope** he construido **dos bots de IA que controlan todo el tráfico de un aeropuerto** (llegadas, salidas y conflictos) usando solo las órdenes que daría un controlador humano.<br>
• **Bot A**: reglas expertas y optimización (secuenciación AMAN/DMAN, vectores, esperas y resolución de conflictos), con parámetros ajustados con **CMA-ES**<br>
• **Bot B**: **aprendizaje por refuerzo (PPO)** en PyTorch con curriculum, preentrenado **imitando al Bot A (DAgger)** y exportado a **ONNX** para jugar en el navegador<br>
• Ambos sujetos a la normativa real **OACI, EASA (RECAT-EU) y FAA** y a un **escudo de seguridad** común<br>
• **Simulador sin navegador** con entorno estilo Gymnasium para Python, página de auditoría de partidas y nuevos aeropuertos: **Madrid-Barajas (LEMD)** y **Málaga (LEMG)**

**🔐 [I-CPU](https://github.com/jossseluuu/I-CPU) · Esteganografía cifrada** · <sub>criptografía aplicada · C++20</sub>

Oculta un texto o un fichero dentro de una imagen de forma que, **sin la contraseña, no se puede ni leer ni demostrar que existe**, y mide lo detectable que es el resultado.<br>
• **Tres dominios de ocultación**: bits de los píxeles (PNG, BMP…), **coeficientes DCT** de JPEG sin recomprimir e **índices de paleta** de GIF<br>
• **Argon2id + XChaCha20-Poly1305**, con posiciones derivadas de la contraseña y **cabecera cifrada**<br>
• **Estegoanálisis integrado** (chi-cuadrado, análisis RS) y métricas de distorsión (PSNR, SSIM)<br>
• **CLI con modo guiado** y **GUI web local sin conexión**; CMake, tests, CI y ADRs

**📡 [HowThingsTalk](https://github.com/jossseluuu/HowThingsTalk) · Cómo funcionan de verdad los aparatos** · <sub>divulgación técnica · ES/EN · un artículo cada día laborable</sub>

Biblioteca que explica **cómo funcionan por dentro los aparatos del día a día**: teléfonos, portátiles, auriculares, relojes, altavoces, tarjetas, bombillas y coches. Cada artículo responde a **una pregunta concreta** en **cuatro capas de profundidad**: la pregunta y su nivel, la respuesta corta, el modelo mental (y dónde se rompe la analogía) y el mecanismo técnico, con protocolos, tramas de datos, espectro de radio y números reales.

**📈 [InvestDashboard](https://github.com/jossseluuu/InvestDashboard) · Dashboard de inversiones** · <sub>full-stack · Flask + React</sub>

Seguimiento de una cartera de inversión en un solo sitio: precios en tiempo real, **multidivisa** con tipos de cambio en vivo, evolución de valor y P&L, fundamentales, valoraciones de analistas, resultados, dividendos y noticias. Incluye tareas programadas, importación/exportación CSV, **alertas semanales por Telegram** y despliegue en Railway + Vercel.

<sub>Más: 🧮 <a href="https://github.com/jossseluuu/DataStructures-Algorithms">DataStructures-Algorithms</a> (estructuras de datos desde cero en C++, con tests) · ✈️ <a href="https://github.com/jossseluuu/airline-database-project">airline-database-project</a> (modelo relacional para la operativa de una aerolínea)</sub>

</details>

---

<div align="center">

### 📫 Let's talk · Hablemos

Working on something interesting in backend, AI or security? I'd be glad to talk.<br>
¿Trabajas en algo interesante de backend, IA o seguridad? Estaré encantado de hablar.

<a href="https://www.linkedin.com/in/joseluislop/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:jossseluuu@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>

</div>
