<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.png">
  <img src="assets/banner-light.png" alt="José Luis López" width="100%">
</picture>

# José Luis López

**Computer Science & Engineering student · Universidad de Granada, Spain**<br>
<sub>AI air traffic controllers · crowd & agent simulation · steganography & metadata forensics · AI tools · bilingual technical writing</sub>

<br>

<a href="https://jossseluuu.github.io/eportfolio/"><img src="https://img.shields.io/badge/Portfolio-1A7F7A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"></a>
<a href="https://www.linkedin.com/in/joseluislop/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:jossseluuu@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://www.instagram.com/jossseluuu"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram"></a>
<a href="https://github.com/jossseluuu/jossseluuu/raw/main/assets/cv/JoseLuisLopez_CV_EN.pdf"><img src="https://img.shields.io/badge/CV-English-2EA043?style=for-the-badge&logo=readdotcv&logoColor=white" alt="CV in English"></a>
<a href="https://github.com/jossseluuu/jossseluuu/raw/main/assets/cv/JoseLuisLopez_CV_ES.pdf"><img src="https://img.shields.io/badge/CV-Español-2EA043?style=for-the-badge&logo=readdotcv&logoColor=white" alt="CV en español"></a>

<sub>**English** · [Español](#es)</sub>

</div>

---

Most of what's on this profile started with a question I couldn't let go of. How does a controller keep dozens of aircraft apart without anyone noticing? What does rush hour look like when nobody plans it and thousands of people simply decide their own day? How much can you hide inside a photo before the photo gives you away? What is a phone actually saying over the air while it sits on the table?

I answer those questions by building something, measuring how well it works and writing down what I learned along the way.

## About me

I'm in the final stretch of a **Computer Science & Engineering** degree at the **Universidad de Granada**. I spent a full academic year at the **University of Montana**, studying entirely in English and working on campus, which taught me a lot about landing somewhere unfamiliar and figuring things out quickly. Back in Granada I served as my faculty's **student delegate**: I helped bring the student council back to life, built a team around it and represented my classmates on the faculty's governing bodies.

The areas I keep coming back to are backend systems, applied AI, security and optimisation, and above all the places where they overlap. A few habits show up in almost everything I build:

- **I write the design down first.** Specifications, requirements and architecture decision records (ADRs) come before the code, especially in [CompanyAgentsHQ](https://github.com/jossseluuu/CompanyAgentsHQ), [NPC Crowd Routines](https://github.com/jossseluuu/NPC-CrowdRoutines) and [I-CPU](https://github.com/jossseluuu/I-CPU).
- **I want numbers, not impressions.** I-CPU runs steganalysis against its own output; every change to the openScope bots has to pass 30 seeded one-hour runs, and CI re-flies them every night; NPC Crowd Routines replays every saved run and checks it by checksum, and reports p50/p95/p99 tick costs; MetaSleuth was checked against hundreds of real files before its first release.
- **Safety is part of the design.** Approval steps, audit logs, safety shields and strict content policies are there from the first commit, not added later.
- **I like explaining things.** I write technical content in English and Spanish, aiming for something a beginner can follow and an expert won't wince at, and my tools explain themselves too: QuantumZero's README is a small course, and MetaSleuth ships its own guide.

---

## Selected projects

| | Project | What it is | Status |
|:-:|---|---|---|
| 🛫 | **[openScope](#openscope)** | Three AI air traffic controllers that run a whole airport, plus a copilot, voice commands and live weather, in an open-source ATC simulator | 🛠️ Working on it |
| 🏙️ | **[NPC Crowd Routines](#npccrowdroutines)** | A city of thousands of residents who each decide their own day, in a deterministic C++20 engine | 🛠️ Working on it |
| 🔐 | **[I-CPU](#i-cpu)** | Hides encrypted data inside images, then attacks its own output to measure how detectable it is | ✅ Done |
| 🔎 | **[MetaSleuth](#metasleuth)** | Shows, verifies and strips the metadata hidden in any file, fully offline | ✅ Done |
| ✦ | **[Snap Tutor](#snaptutor)** | A browser extension: snap a study question and Claude explains the answer | 🛠️ Working on it |
| ⚛️ | **[QuantumZero](#quantumzero)** | A quantum circuit simulator in C++17 that you can read line by line | 🔭 Exploring what's next |
| 🏢 | **[CompanyAgentsHQ](#companyagentshq)** | A company of AI agents you manage from an isometric office | 🛠️ Working on it |
| 📡 | **[HowThingsTalk](#howthingstalk)** | How everyday devices really work, one question per article, in Spanish and English | 📰 New article every day |
| 🚦 | **[ZeroTrace](#zerotrace)** | A bilingual cybersecurity newsletter, one concept per edition | 📰 New edition every day |

<sub>🛠️ being built right now · ✅ finished and ready to use · 🔭 working, and I'm researching where to take it · 📰 published daily. Each card below is a two-minute summary; the full story lives in each repository.</sub>

<br>

<a id="openscope"></a>

### 🛫 openScope · AI air traffic controllers

<sub>**JavaScript · Python · PyTorch · ONNX** · fork of [openscope/openscope](https://github.com/openscope/openscope): the bots, the copilot, the realism and safety layers, the weather, voice control, the headless simulator and eight airports are mine</sub>

Bots that act as the controller for an entire airport, from the first arrival to the last departure, using **only the commands a human controller has** and following real ICAO, EASA and FAA separation rules. All three see the same picture, choose from the same 66 actions, pass through one shared safety shield and are scored by one rulebook, ranked *safety → separation → procedure → efficiency*.

**Three bots, three ways of thinking**

| Bot | How it controls the airport | Where it stands |
|---|---|---|
| **A · The expert** | Hand-written rules plus planning algorithms. Every 5 seconds it predicts conflicts two minutes ahead and checks that each fix works (and doesn't create a new conflict) before giving it, orders arrivals with simulated annealing and picks the best point to join the ILS based on the terrain along the path. Every order comes with its reason. | Flying · 494 landings and 539 departures in 30 one-hour runs |
| **B · The learner** | A small transformer network (about 480,000 parameters) that first copies Bot A's decisions and then improves on its own with reinforcement learning (PPO), from light traffic to full traffic with wind and emergencies. Built to be exported to ONNX and run in the browser. | Training · it already lands 55% of what Bot A does; it needs 80% to move on to PPO |
| **C · The team** | Six specialist agents (coordinator, arrivals, ILS, tower, departures and separation), each allowed only its own kind of order. Independent supervisors grade every instruction as *good*, *doubtful* or *bad* and work out the cause of each incident. | Flying · 0 collisions and over 40,000 orders audited |

**Not just for bots: what changes for a human player**

- 🛡️ **Safety nets like the real ones:** STCA warns the controller two minutes ahead, TCAS II issues coordinated climb/descend advisories that pilots actually fly, and MSAW and APW warn about terrain and restricted areas.
- 🌦️ **Live weather:** wind that shifts and gusts, runway changes when it goes out of limits, fog with low-visibility procedures and thunderstorms that pilots ask to avoid. Type `metar` to check it.
- 🧑‍✈️ **A copilot:** it warns you, suggests orders with the reason behind them (press F4 to accept) or takes over a single aircraft or a whole sector, such as `delegate tower`.
- 🎙️ **Talk to it:** hold F2 and give instructions in real ATC phraseology, in English or Spanish; it proposes the command and waits for you to confirm.

**Eight airports built from official charts:** Madrid, Málaga, Palma, Barcelona and Bilbao from the Spanish AIP, Paris-Charles de Gaulle from the French one, and Amsterdam and Singapore rebuilt from scratch. Airspace, SIDs, STARs, terrain and traffic come from the real AIRAC data, read with my own Python tools.

**Built like a real project:** a deterministic simulator that runs faster than real time and works as a Gymnasium environment from Python; a fixed 30-run protocol that every change has to pass; a nightly CI job that re-flies the bots and opens an issue if they get worse; an airport validator; architecture decision records; and documentation written as code.

**Bot A in numbers** (30 one-hour runs across five airport setups): `~16 landings/h` · `~18 departures/h` · `~1.4 separation losses/h` · `−81% separation losses in one month`

> 🛠️ **Working on it.** Next: retraining Bot B so it also sees the weather and the safety-net alerts, test-flying the new airports and adding Geneva, Hong Kong, Osaka and Sydney, and turning Bot C's agents into fully independent programs.

▶️ **[Play it in your browser](https://jossseluuu.github.io/openScope/)** (type `bot a`, `bot c` or `copilot suggest`) &nbsp;·&nbsp; 📚 **[Read the docs](https://github.com/jossseluuu/openScope/tree/main/docs)** &nbsp;·&nbsp; 📂 **[Explore the repo](https://github.com/jossseluuu/openScope)**

<br>

<a id="npccrowdroutines"></a>

### 🏙️ NPC Crowd Routines · A city that lives its own day

<sub>**C++20 · CMake · no external dependencies** · PolyForm Noncommercial licence</sub>

Thousands of residents with personality, schedules and relationships live a full day in a procedurally generated city: they work, study, shop, meet friends and get around on foot, by bike, by car or by bus. Rush hour, parks filling up in the afternoon or the jam after an accident **aren't scripted: they emerge** from each resident's own decisions.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/NPC-CrowdRoutines/main/docs/assets/capturas/hero.png" alt="A river city with 8,000 residents at 17:38: live traffic, a fire, an accident and a street market, with the population state tree on the right" width="85%"></p>

- **Decisions you can inspect:** a utility AI with 8 needs, 12 personality traits and 48 archetypes; the inspector shows the score behind every choice a resident makes.
- **A city that reacts:** 6 city templates, 36 building types, traffic lights, congestion and buses, plus 18 event types (fires, storms, concerts…) that residents see, hear about, pass on and respond to.
- **Reproducible by design:** a single-threaded, fixed-step engine; saved runs replay and are verified by checksum.
- **Built for experiments:** a headless mode that exports telemetry, a built-in benchmark and an HTTP API to automate it all.

**In numbers:** `25,000 residents at ×520 real time on one thread` · `85 sub-states` · `27 test cases, 2,100+ assertions` · `CI on Linux & Windows`

> 🛠️ **Working on it.** Next: parallel simulation beyond 60,000 residents, a map editor in the browser and a WebAssembly demo you can open online.

📖 **[Read the wiki](https://jossseluuu.github.io/NPC-CrowdRoutines/)** &nbsp;·&nbsp; 📂 **[Explore the repo](https://github.com/jossseluuu/NPC-CrowdRoutines)**

<br>

<a id="i-cpu"></a>

### 🔐 I-CPU · Hide data in images, then try to find it

<sub>**C++20 · Argon2id · XChaCha20-Poly1305** · MIT licence</sub>

Most steganography tools stop at hiding. I-CPU hides an encrypted message or file inside an image **and then attacks its own result** with standard steganalysis, so you compare settings with numbers instead of guesses.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/I-CPU/main/docs/img/experimentos/original-frente-a-resultado.png" alt="The original image and the one carrying 12 KB of hidden data look identical; only the difference amplified ×64 reveals noise in textured areas" width="85%"></p>

- **PNG, JPEG and GIF:** pixel bits, JPEG coefficients without recompressing, and palette indices, animated GIFs included.
- **Hard to spot:** adaptive embedding that changes few samples and prefers textured areas.
- **Hard to read:** Argon2id + XChaCha20-Poly1305, with a random salt in every image.
- **Then it checks itself:** chi-square and RS analysis, plus PSNR and SSIM to measure how much the image changed.

**In numbers:** `3 hiding domains` · `68 tests` · `CI on Windows & Linux` · `fuzzing and sanitizers` · `CLI + offline web interface`

> ✅ **Done.** Finished in November 2026 and ready to use.

📂 **[Explore the repo](https://github.com/jossseluuu/I-CPU)**

<br>

<a id="metasleuth"></a>

### 🔎 MetaSleuth · What your files say about you

<sub>**Python, standard library only · C2PA verification** · GPL-3.0 licence</sub>

Drop in a photo, a document, a program or a whole folder and MetaSleuth shows what it carries besides its content: where a photo was taken, who wrote a document, whether an image declares it was made by AI. **Nothing leaves your computer.**

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/MetaSleuth/main/docs/img/01-analisis-foto.png" alt="MetaSleuth main window analysing a photo: file list, AI-trace verdict and a table of metadata fields" width="85%"></p>

- **Finds what matters:** GPS location, editing software, AI-generation traces and hidden text.
- **Verifies, not just reads:** checks C2PA content-credential signatures and says when a file was tampered with.
- **Explains and cleans:** every field is explained, and it can strip GPS or EXIF from a copy before you share it.

**In numbers:** `35+ formats` · `58 tests on Windows, macOS & Linux` · `checked against 569 real files` · `0 dependencies`

> ✅ **Done.** Finished in November 2026 and ready to use.

📂 **[Explore the repo](https://github.com/jossseluuu/MetaSleuth)**

<br>

<a id="snaptutor"></a>

### ✦ Snap Tutor · Study questions, explained

<sub>**JavaScript (Manifest V3) · Node.js · Claude API or Claude Code** · MIT licence · unofficial personal project, not affiliated with Anthropic</sub>

Press ✦ (or <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>) on a practice question and, a few seconds later, the right answer appears in the corner **with a short explanation of why**.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/extesionBrave/main/docs/img/respuesta.png" alt="Snap Tutor answering a multiple-choice biology question: the correct letter and its explanation appear in the bottom-right corner" width="85%"></p>

- **Your choice of connection:** your own API key, or your Claude account through a small local bridge that can also use your own notes.
- **Private by default:** it captures the visible tab only when you press the button.
- **Made for learning:** built for revision, explicitly not for exams.

**In numbers:** `Brave · Chrome · Edge` · `unit + end-to-end tests` · `CI and automatic releases`

> 🛠️ **Working on it.** Next: more browsers, a cleaner implementation and more ways to customise it.

📂 **[Explore the repo](https://github.com/jossseluuu/extesionBrave)**

<br>

<a id="quantumzero"></a>

### ⚛️ QuantumZero · A quantum computer you can read line by line

<sub>**C++17 · CMake · zero dependencies** · MIT licence</sub>

A state-vector simulator that keeps every amplitude of `n` qubits in memory and applies gates directly to them. Build Bell and GHZ states or your own circuit, and **watch superposition, interference and entanglement happen in the numbers**.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/QuantumZero/main/docs/images/terminal-bell.svg" alt="QuantumZero running the Bell-state demo in a terminal" width="85%"></p>

- **A README that teaches:** quantum basics in five minutes and a Bell state worked out step by step.
- **Tested from the maths up:** gate identities, the full CNOT truth table and exact amplitudes.
- **Try it live:** an interactive mode to build circuits gate by gate.

**In numbers:** `H · X · Y · Z · CNOT` · `133 checks` · `CI on Windows, Linux & macOS` · `0 dependencies`

> 🔭 **Exploring what's next.** The simulator works and is fully tested; now I'm researching how to take it further.

📂 **[Explore the repo](https://github.com/jossseluuu/QuantumZero)**

<br>

<a id="companyagentshq"></a>

### 🏢 CompanyAgentsHQ · A company of AI agents you can actually manage

<sub>**Python · FastAPI · React + TypeScript · Three.js · PostgreSQL + pgvector** · bachelor's final project · source available, all rights reserved</sub>

Multi-agent systems are usually black boxes. Here you give a goal to the CEO agent, approve its plan and **watch the team work across an isometric office**, while every action is audited and costed.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/CompanyAgentsHQ/main/docs/img/01-oficina.png" alt="CompanyAgentsHQ isometric office with eight agents in their rooms" width="85%"></p>

- **A real org chart:** managers review their team's work, and sensitive actions wait in your approval inbox.
- **Accountable by design:** a verifiable hash-chained audit log, an Auditor agent that stops loops and daily AI budgets.
- **An office you can shape:** drag rooms and furniture, decide who can enter each room, and hire from hundreds of roles.
- **Free to run:** local models through Ollama, any OpenAI-compatible server, or the Claude API with your own key.

**In numbers:** `8 starting agents` · `646 roles to hire` · `161 + 66 tracked requirements` · `tested end-to-end on an 8 GB laptop GPU`

> 🛠️ **Working on it.** Next: making each agent better on its own and the company better as a whole.

📂 **[Explore the repo](https://github.com/jossseluuu/CompanyAgentsHQ)**

<br>

<a id="howthingstalk"></a>

### 📡 HowThingsTalk · How everyday devices actually work

<sub>**Technical writing · Spanish & English** · CC BY-SA licence</sub>

One concrete question per article about the tech we use without thinking, such as [how GPS computes your position](https://github.com/jossseluuu/HowThingsTalk/blob/main/docs/EN/05_Positioning/01-HowGPSComputesYourPosition.md) or [what your ISP sees despite HTTPS](https://github.com/jossseluuu/HowThingsTalk/blob/main/docs/EN/11_PrivacyAndFootprint/02-WhatYourISPSeesDespiteHTTPS.md). Clear enough for a beginner, rigorous enough for an expert.

- **Read as deep as you like:** a one-sentence answer, an everyday analogy and where it breaks, then the real mechanism with numbers.
- **Written twice, not translated once:** every article exists in Spanish and English.
- **Timeless on purpose:** no news, reviews or buying advice; every claim backed by primary sources.

> 📰 **New article every day** since 1 November 2026.

📖 **[Start reading](https://github.com/jossseluuu/HowThingsTalk)**

<br>

<a id="zerotrace"></a>

### 🚦 ZeroTrace · Practical cybersecurity, one concept a day

<sub>**Static site with its own Python generator (standard library only) · Spanish & English** · content CC BY 4.0, code MIT</sub>

Cybersecurity for everyone, about the devices people actually use: what a thief can do with your phone after watching you type the passcode, why the cloud isn't a backup, or what a smartwatch without a passcode shows to whoever picks it up.

- **Today's status:** a traffic-light alert for actively exploited or wide-impact flaws in everyday devices, published once and kept in a public [alert log](https://jossseluuu.github.io/ZeroTrace/en/alerts.html).
- **Two reading levels:** *Basic* in a few minutes, *Deep dive* for the technical reader.
- **Right-sized advice:** impact and effort for every action, and what you **don't** need to do.
- **Sources or it didn't happen:** every fact and CVE links to a primary source, and the pages carry no cookies, trackers or third-party scripts.

> 📰 **New edition every day** since 3 November 2026.

📖 **[Read it](https://jossseluuu.github.io/ZeroTrace/en/)** &nbsp;·&nbsp; 🇪🇸 **[En español](https://jossseluuu.github.io/ZeroTrace/es/)** &nbsp;·&nbsp; 📡 **[RSS](https://jossseluuu.github.io/ZeroTrace/en/feed.xml)** &nbsp;·&nbsp; 📂 **[Explore the repo](https://github.com/jossseluuu/ZeroTrace)**

---

### 🧩 Other projects

| Project | What it is | Stack |
|---|---|---|
| 🧮 **[DataStructures-Algorithms](https://github.com/jossseluuu/DataStructures-Algorithms)** | Twenty-one classic data structures written from scratch (lists, stacks, queues, BST, AVL, heaps, trie, hash tables, sets, graphs, union-find) plus searching, six sorting algorithms, Dijkstra, Prim and Kruskal. Each has its own automatic test, with generic template versions and complexity tables. | C++ · CMake |
| ✈️ **[airbaseQueue](https://github.com/jossseluuu/airbaseQueue)** | Discrete-event simulation of the ground-phase sortie cycle at a fighter base (runway, fuel, hangar inspection, maintenance). 30 Monte Carlo replications per scenario with 95% confidence intervals, validated against Erlang-C and Little's law; it finds maintenance, not runway slots, to be the bottleneck. Streamlit dashboard and 38 tests. | Python · SimPy · Streamlit |
| 🎞️ **[AlgorithmVisualizer](https://github.com/jossseluuu/AlgorithmVisualizer)** | Step-by-step animations of seven sorting algorithms, two searches, four pathfinders (BFS, DFS, Dijkstra, A*) and five data structures. The backend runs each algorithm once and returns every snapshot, so the canvas replays them frame by frame at any speed. | Flask · React · Vite · Canvas |
| 📈 **[InvestDashboard](https://github.com/jossseluuu/InvestDashboard)** | A personal portfolio dashboard: live prices converted into seven currencies, per-asset fundamentals and news, P&L charts, and an optional weekly Telegram summary. Includes a Railway + Vercel deployment guide. | Flask · React · SQLite · Chart.js |
| ✈️ **[airline-database-project](https://github.com/jossseluuu/airline-database-project)** | Relational database design for airline operations (pilots, crew, flights, flight plans, aircraft, hangars and maintenance), with a work breakdown structure, a data-quality risk analysis and a small web front end. | MySQL · Flask · JavaScript |

---

## Tech stack

<sub>Technologies I've used in the projects above.</sub>

| Area | Tools |
|---|---|
| **Languages** | <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/C++20-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"> <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL"> |
| **Backend & data** | <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" alt="Flask"> <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white" alt="SQLAlchemy"> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis"> <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"> |
| **Frontend** | <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite"> <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white" alt="Three.js"> <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS"> <img src="https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white" alt="Chart.js"> <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"> <br><sub>Browser extensions (Manifest V3) · Tkinter desktop apps</sub> |
| **AI & ML** | <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch"> <img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white" alt="ONNX"> <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude API"> <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama"> <img src="https://img.shields.io/badge/pgvector-336791?style=flat-square&logo=postgresql&logoColor=white" alt="pgvector"> <br><sub>Reinforcement learning (PPO, DAgger) · metaheuristics (CMA-ES, simulated annealing) · multi-agent supervision · speech recognition and natural-language command parsing · RAG and embeddings · LLM agents and tool use · utility AI and A* pathfinding · agent-based crowd simulation and data-oriented design · discrete-event simulation (SimPy) and queueing theory · quantum state-vector simulation</sub> |
| **Security** | <sub>Applied cryptography (Argon2id, XChaCha20-Poly1305) · steganography and steganalysis · metadata forensics and C2PA verification · fuzzing and sanitizers · Content Security Policy · prompt-injection-aware agent design</sub> |
| **Tooling & quality** | <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"> <img src="https://img.shields.io/badge/GitHub_Pages-222222?style=flat-square&logo=githubpages&logoColor=white" alt="GitHub Pages"> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" alt="CMake"> <img src="https://img.shields.io/badge/MkDocs-526CFE?style=flat-square&logo=materialformkdocs&logoColor=white" alt="MkDocs"> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest"> <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"> |

<sub>Also used in my degree and coursework: C, Java, PHP, Bash, Django, Oracle, Power BI, Tableau and Figma; Azure AI services and Microsoft Defender XDR through Microsoft Learn; and security tools such as Wireshark, Nmap, Burp Suite and Kali Linux.</sub>

---

## GitHub activity

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/0-profile-details.svg">
  <img src="./profile-summary-card-output/github/0-profile-details.svg" alt="Contributions over time" width="100%">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/3-stats.svg">
  <img src="./profile-summary-card-output/github/3-stats.svg" alt="GitHub stats" width="49%">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/2-most-commit-language.svg">
  <img src="./profile-summary-card-output/github/2-most-commit-language.svg" alt="Most committed languages" width="49%">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/jossseluuu/jossseluuu/output/github-snake-dark.svg">
  <img src="https://raw.githubusercontent.com/jossseluuu/jossseluuu/output/github-snake.svg" alt="Contribution graph being eaten by a snake" width="100%">
</picture>

</div>

---

<a id="es"></a>

## 🇪🇸 En español

<details>
<summary><b>Leer el perfil completo en español</b></summary>
<br>

Casi todo lo que hay en este perfil empezó con una pregunta que no me podía quitar de la cabeza. ¿Cómo mantiene un controlador separados a decenas de aviones sin que nadie lo note? ¿Cómo es una hora punta que nadie planifica, cuando miles de personas simplemente deciden su propio día? ¿Cuánto se puede esconder dentro de una foto antes de que la propia foto te delate? ¿Qué está diciendo exactamente un móvil por el aire mientras descansa sobre la mesa?

Mi forma de responderlas es construir algo, medir qué tal funciona y dejar por escrito lo que aprendo por el camino.

### Sobre mí

Estoy en la recta final de **Ingeniería Informática** en la **Universidad de Granada**. Pasé un curso académico completo en la **University of Montana**, estudiando íntegramente en inglés y trabajando en el campus, algo que me enseñó mucho sobre llegar a un sitio desconocido y espabilarse rápido. En Granada fui **delegado de estudiantes** de mi facultad: ayudé a reactivar la Delegación, formé un equipo para sacarla adelante y representé a mis compañeros en los órganos de gobierno del centro.

Las áreas a las que siempre vuelvo son los sistemas backend, la IA aplicada, la seguridad y la optimización, y sobre todo los puntos donde se cruzan. Hay costumbres que se repiten en casi todo lo que hago:

- **Primero escribo el diseño.** Especificación, requisitos y registros de decisiones de arquitectura (ADR) antes del código, sobre todo en [CompanyAgentsHQ](https://github.com/jossseluuu/CompanyAgentsHQ), [NPC Crowd Routines](https://github.com/jossseluuu/NPC-CrowdRoutines) e [I-CPU](https://github.com/jossseluuu/I-CPU).
- **Quiero cifras, no impresiones.** I-CPU somete su propio resultado a estegoanálisis; cada cambio en los bots de openScope tiene que superar 30 partidas de una hora con semilla, y la CI los vuelve a volar cada noche; NPC Crowd Routines vuelve a reproducir cada partida guardada y la verifica con un checksum, y mide el coste por tick en p50/p95/p99; MetaSleuth se contrastó con cientos de archivos reales antes de su primera versión.
- **La seguridad forma parte del diseño.** Aprobaciones, registros de auditoría, escudos de seguridad y políticas de contenido estrictas están desde el primer commit, no se añaden después.
- **Me gusta explicar.** Escribo contenido técnico en español y en inglés, buscando que un principiante pueda seguirlo y que un experto no encuentre nada que corregir, y mis herramientas también se explican solas: el README de QuantumZero es un pequeño curso y MetaSleuth trae su propia guía.

### Proyectos seleccionados

| | Proyecto | Qué es | Estado |
|:-:|---|---|---|
| 🛫 | **[openScope](#es-openscope)** | Tres controladores aéreos con IA que llevan un aeropuerto entero, más copiloto, órdenes por voz y meteorología viva, en un simulador ATC de código abierto | 🛠️ Trabajando en ello |
| 🏙️ | **[NPC Crowd Routines](#es-npccrowdroutines)** | Una ciudad de miles de residentes que deciden su propio día, en un motor C++20 determinista | 🛠️ Trabajando en ello |
| 🔐 | **[I-CPU](#es-i-cpu)** | Esconde datos cifrados en imágenes y después ataca su propio resultado para medir lo detectable que es | ✅ Terminado |
| 🔎 | **[MetaSleuth](#es-metasleuth)** | Muestra, verifica y limpia los metadatos ocultos de cualquier archivo, sin conexión | ✅ Terminado |
| ✦ | **[Snap Tutor](#es-snaptutor)** | Una extensión de navegador: capturas una pregunta de estudio y Claude explica la respuesta | 🛠️ Trabajando en ello |
| ⚛️ | **[QuantumZero](#es-quantumzero)** | Un simulador de circuitos cuánticos en C++17 que se lee línea a línea | 🔭 Explorando el siguiente paso |
| 🏢 | **[CompanyAgentsHQ](#es-companyagentshq)** | Una empresa de agentes de IA que gestionas desde una oficina isométrica | 🛠️ Trabajando en ello |
| 📡 | **[HowThingsTalk](#es-howthingstalk)** | Cómo funcionan de verdad los aparatos cotidianos, una pregunta por artículo, en español e inglés | 📰 Un artículo nuevo cada día |
| 🚦 | **[ZeroTrace](#es-zerotrace)** | Un boletín bilingüe de ciberseguridad, un concepto por edición | 📰 Una edición nueva cada día |

<sub>🛠️ en desarrollo ahora mismo · ✅ terminado y listo para usar · 🔭 funciona, y estudio hacia dónde llevarlo · 📰 se publica a diario. Cada ficha es un resumen de dos minutos; la historia completa está en cada repositorio.</sub>

<a id="es-openscope"></a>

#### 🛫 openScope · Controladores aéreos con IA

<sub>**JavaScript · Python · PyTorch · ONNX** · fork de [openscope/openscope](https://github.com/openscope/openscope): los bots, el copiloto, las capas de realismo y seguridad, la meteorología, el control por voz, el simulador sin navegador y ocho aeropuertos son míos</sub>

Bots que hacen de controlador de todo un aeropuerto, desde la primera llegada hasta la última salida, usando **solo las órdenes que tiene un controlador humano** y con las normas reales de separación de OACI, EASA y FAA. Los tres ven lo mismo, eligen entre las mismas 66 acciones, pasan por un mismo escudo de seguridad y los puntúa un único reglamento ordenado como *seguridad → separación → procedimiento → eficiencia*.

**Tres bots, tres formas de pensar**

| Bot | Cómo controla el aeropuerto | En qué punto está |
|---|---|---|
| **A · El experto** | Reglas escritas a mano y algoritmos de planificación. Cada 5 segundos predice los conflictos a dos minutos vista y comprueba que cada solución funciona (y no crea un conflicto nuevo) antes de darla, ordena las llegadas con recocido simulado y elige el mejor punto para unirse al ILS según el terreno de la trayectoria. Cada orden lleva su motivo. | En vuelo · 494 aterrizajes y 539 despegues en 30 partidas de una hora |
| **B · El aprendiz** | Una pequeña red *transformer* (unos 480.000 parámetros) que primero copia las decisiones del Bot A y después mejora por su cuenta con aprendizaje por refuerzo (PPO), de poco tráfico a tráfico completo con viento y emergencias. Preparado para exportarse a ONNX y funcionar en el navegador. | Entrenando · ya aterriza el 55 % de lo que aterriza el Bot A; necesita el 80 % para pasar a PPO |
| **C · El equipo** | Seis agentes especialistas (coordinador, entradas, ILS, torre, salidas y separación), cada uno con permiso solo para su tipo de orden. Supervisores independientes califican cada instrucción como *buena*, *dudosa* o *mala* y averiguan la causa de cada incidente. | En vuelo · 0 colisiones y más de 40.000 órdenes auditadas |

**No solo para bots: lo que cambia para quien juega**

- 🛡️ **Redes de seguridad como las reales:** el STCA avisa al controlador con dos minutos de margen, el TCAS II da avisos coordinados de ascenso o descenso que los pilotos vuelan de verdad, y el MSAW y el APW avisan del terreno y de las zonas restringidas.
- 🌦️ **Meteorología viva:** viento que cambia y racheado, cambios de pista cuando se sale de límites, niebla con procedimientos de baja visibilidad y tormentas que los pilotos piden esquivar. Escribe `metar` para consultarla.
- 🧑‍✈️ **Un copiloto:** te avisa, te sugiere órdenes con su motivo (F4 para aceptar) o se encarga de un avión concreto o de un sector entero, por ejemplo con `delegate tower`.
- 🎙️ **Háblale:** mantén F2 y da instrucciones con fraseología ATC real, en español o en inglés; te propone el comando y espera a que lo confirmes.

**Ocho aeropuertos hechos a partir de las cartas oficiales:** Madrid, Málaga, Palma, Barcelona y Bilbao desde el AIP España, París-Charles de Gaulle desde el francés, y Ámsterdam y Singapur rehechos desde cero. El espacio aéreo, las SID, las STAR, el terreno y el tráfico salen de los datos AIRAC reales, leídos con herramientas propias en Python.

**Hecho como un proyecto real:** un simulador determinista que va más rápido que el tiempo real y funciona como entorno Gymnasium desde Python; un protocolo fijo de 30 partidas que debe superar cada cambio; una tarea nocturna de CI que vuelve a volar los bots y abre una issue si empeoran; un validador de aeropuertos; registros de decisiones de arquitectura; y documentación escrita como código.

**El Bot A en cifras** (30 partidas de una hora en cinco configuraciones de aeropuerto): `~16 aterrizajes/h` · `~18 despegues/h` · `~1,4 pérdidas de separación/h` · `−81 % de pérdidas de separación en un mes`

> 🛠️ **Trabajando en ello.** Lo siguiente: reentrenar al Bot B para que también vea la meteorología y las alertas de las redes de seguridad, probar en vuelo los aeropuertos nuevos y añadir Ginebra, Hong Kong, Osaka y Sídney, y convertir a los agentes del Bot C en programas del todo independientes.

▶️ **[Juégalo en el navegador](https://jossseluuu.github.io/openScope/)** (escribe `bot a`, `bot c` o `copilot suggest`) &nbsp;·&nbsp; 📚 **[Leer la documentación](https://github.com/jossseluuu/openScope/tree/main/docs)** &nbsp;·&nbsp; 📂 **[Ver el repo](https://github.com/jossseluuu/openScope)**

<a id="es-npccrowdroutines"></a>

#### 🏙️ NPC Crowd Routines · Una ciudad que vive su propio día

<sub>**C++20 · CMake · sin dependencias externas** · licencia PolyForm Noncommercial</sub>

Miles de residentes con personalidad, horarios y relaciones viven un día completo en una ciudad generada proceduralmente: trabajan, estudian, compran, quedan con amigos y se mueven a pie, en bici, en coche o en autobús. La hora punta, los parques llenándose por la tarde o el atasco tras un accidente **no están guionizados: surgen** de las decisiones de cada residente.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/NPC-CrowdRoutines/main/docs/assets/capturas/hero.png" alt="Una ciudad con río y 8.000 residentes a las 17:38: tráfico en directo, un incendio, un accidente y un mercadillo, con el árbol de estados de la población a la derecha" width="85%"></p>

- **Decisiones que se pueden inspeccionar:** una IA de utilidad con 8 necesidades, 12 rasgos de personalidad y 48 arquetipos; el inspector enseña la puntuación detrás de cada elección de un residente.
- **Una ciudad que reacciona:** 6 plantillas de ciudad, 36 tipos de edificio, semáforos, atascos y autobuses, y 18 tipos de evento (incendios, tormentas, conciertos…) que los residentes ven, oyen, se cuentan y a los que responden.
- **Reproducible por diseño:** un motor de paso fijo en un solo hilo; las partidas guardadas se reproducen y se verifican con un checksum.
- **Pensado para experimentar:** un modo sin interfaz que exporta telemetría, un benchmark integrado y una API HTTP para automatizarlo todo.

**En cifras:** `25.000 residentes a ×520 el tiempo real en un hilo` · `85 subestados` · `27 casos de prueba, más de 2.100 aserciones` · `CI en Linux y Windows`

> 🛠️ **Trabajando en ello.** Lo siguiente: simulación en paralelo para más de 60.000 residentes, un editor de mapas en el navegador y una demo en WebAssembly que se pueda abrir en línea.

📖 **[Leer la wiki](https://jossseluuu.github.io/NPC-CrowdRoutines/)** &nbsp;·&nbsp; 📂 **[Ver el repo](https://github.com/jossseluuu/NPC-CrowdRoutines)**

<a id="es-i-cpu"></a>

#### 🔐 I-CPU · Esconder datos en imágenes y después intentar encontrarlos

<sub>**C++20 · Argon2id · XChaCha20-Poly1305** · licencia MIT</sub>

La mayoría de herramientas de esteganografía se quedan en esconder. I-CPU oculta un mensaje o un fichero cifrado dentro de una imagen **y después ataca su propio resultado** con estegoanálisis estándar, para comparar ajustes con números y no a ojo.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/I-CPU/main/docs/img/experimentos/original-frente-a-resultado.png" alt="La imagen original y la que lleva 12 KB ocultos son idénticas a simple vista; solo la diferencia amplificada ×64 revela ruido en las zonas con textura" width="85%"></p>

- **PNG, JPEG y GIF:** bits de los píxeles, coeficientes de JPEG sin recomprimir e índices de paleta, GIF animados incluidos.
- **Difícil de detectar:** inserción adaptativa que cambia pocas muestras y prefiere las zonas con textura.
- **Difícil de leer:** Argon2id + XChaCha20-Poly1305, con una sal aleatoria en cada imagen.
- **Y después se pone a prueba:** análisis chi-cuadrado y RS, y PSNR y SSIM para medir cuánto ha cambiado la imagen.

**En cifras:** `3 dominios de ocultación` · `68 pruebas` · `CI en Windows y Linux` · `fuzzing y sanitizadores` · `CLI + interfaz web sin conexión`

> ✅ **Terminado.** Finalizado en noviembre de 2026 y listo para usar.

📂 **[Ver el repo](https://github.com/jossseluuu/I-CPU)**

<a id="es-metasleuth"></a>

#### 🔎 MetaSleuth · Lo que tus archivos dicen de ti

<sub>**Python, solo biblioteca estándar · verificación C2PA** · licencia GPL-3.0</sub>

Le das una foto, un documento, un programa o una carpeta entera y MetaSleuth te enseña lo que lleva además de su contenido: dónde se hizo una foto, quién escribió un documento o si una imagen declara que la generó una IA. **Nada sale de tu ordenador.**

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/MetaSleuth/main/docs/img/01-analisis-foto.png" alt="Ventana principal de MetaSleuth analizando una foto: lista de archivos, valoración de huellas de IA y tabla de campos" width="85%"></p>

- **Encuentra lo importante:** ubicación GPS, programas de edición, huellas de IA generativa y texto oculto.
- **Verifica, no solo lee:** comprueba las firmas de las credenciales de contenido C2PA y avisa si el archivo se ha manipulado.
- **Explica y limpia:** cada campo viene explicado, y puede quitar el GPS o el EXIF de una copia antes de compartirla.

**En cifras:** `35+ formatos` · `58 pruebas en Windows, macOS y Linux` · `contrastado con 569 archivos reales` · `0 dependencias`

> ✅ **Terminado.** Finalizado en noviembre de 2026 y listo para usar.

📂 **[Ver el repo](https://github.com/jossseluuu/MetaSleuth)**

<a id="es-snaptutor"></a>

#### ✦ Snap Tutor · Preguntas de estudio, explicadas

<sub>**JavaScript (Manifest V3) · Node.js · API de Claude o Claude Code** · licencia MIT · proyecto personal no oficial, sin relación con Anthropic</sub>

Pulsas ✦ (o <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>) sobre una pregunta de práctica y, en unos segundos, aparece en la esquina la respuesta correcta **con una explicación breve del porqué**.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/extesionBrave/main/docs/img/respuesta.png" alt="Snap Tutor respondiendo a una pregunta tipo test de biología: la letra correcta y su explicación aparecen en la esquina inferior derecha" width="85%"></p>

- **Tú eliges cómo conectar:** con tu propia API key o con tu cuenta de Claude a través de un pequeño servidor local que además puede usar tus apuntes.
- **Privada por defecto:** solo captura la pestaña visible cuando pulsas el botón.
- **Pensada para aprender:** para repasar, y expresamente no para exámenes.

**En cifras:** `Brave · Chrome · Edge` · `pruebas unitarias y de extremo a extremo` · `CI y versiones automáticas`

> 🛠️ **Trabajando en ello.** Lo siguiente: más navegadores, una implementación más limpia y más opciones de personalización.

📂 **[Ver el repo](https://github.com/jossseluuu/extesionBrave)**

<a id="es-quantumzero"></a>

#### ⚛️ QuantumZero · Un ordenador cuántico que se lee línea a línea

<sub>**C++17 · CMake · sin dependencias** · licencia MIT</sub>

Un simulador de vector de estado que guarda en memoria todas las amplitudes de `n` qubits y aplica las puertas directamente sobre ellas. Monta estados de Bell y GHZ o tu propio circuito y **mira cómo la superposición, la interferencia y el entrelazamiento aparecen en los números**.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/QuantumZero/main/docs/images/terminal-bell.svg" alt="QuantumZero ejecutando la demostración del estado de Bell en una terminal" width="85%"></p>

- **Un README que enseña:** fundamentos cuánticos en cinco minutos y un estado de Bell resuelto paso a paso.
- **Probado desde las matemáticas:** identidades de puertas, tabla de verdad completa de CNOT y amplitudes exactas.
- **Pruébalo en directo:** un modo interactivo para montar circuitos puerta a puerta.

**En cifras:** `H · X · Y · Z · CNOT` · `133 comprobaciones` · `CI en Windows, Linux y macOS` · `0 dependencias`

> 🔭 **Explorando el siguiente paso.** El simulador funciona y está probado a fondo; ahora estudio cómo llevarlo más lejos.

📂 **[Ver el repo](https://github.com/jossseluuu/QuantumZero)**

<a id="es-companyagentshq"></a>

#### 🏢 CompanyAgentsHQ · Una empresa de agentes de IA que de verdad puedes gestionar

<sub>**Python · FastAPI · React + TypeScript · Three.js · PostgreSQL + pgvector** · Trabajo Fin de Grado · código visible, todos los derechos reservados</sub>

Los sistemas multiagente suelen ser cajas negras. Aquí das un objetivo a la CEO, apruebas su plan y **ves al equipo trabajar por una oficina isométrica**, mientras cada acción queda auditada y con su coste.

<p align="center"><img src="https://raw.githubusercontent.com/jossseluuu/CompanyAgentsHQ/main/docs/img/01-oficina.png" alt="Oficina isométrica de CompanyAgentsHQ con ocho agentes en sus salas" width="85%"></p>

- **Un organigrama real:** los jefes revisan el trabajo de su equipo y las acciones delicadas esperan en tu bandeja de aprobaciones.
- **Responsable por diseño:** registro de auditoría encadenado y verificable, un agente Auditor que corta los bucles y presupuestos diarios de IA.
- **Una oficina a tu medida:** arrastras salas y muebles, decides quién entra en cada sala y contratas entre cientos de cargos.
- **Gratis de usar:** modelos locales con Ollama, cualquier servidor compatible con OpenAI o la API de Claude con tu clave.

**En cifras:** `8 agentes de inicio` · `646 cargos para contratar` · `161 + 66 requisitos con seguimiento` · `probado de principio a fin en una GPU de portátil de 8 GB`

> 🛠️ **Trabajando en ello.** Lo siguiente: mejorar cada agente por separado y la empresa en su conjunto.

📂 **[Ver el repo](https://github.com/jossseluuu/CompanyAgentsHQ)**

<a id="es-howthingstalk"></a>

#### 📡 HowThingsTalk · Cómo funcionan de verdad los aparatos cotidianos

<sub>**Divulgación técnica · español e inglés** · licencia CC BY-SA</sub>

Una pregunta concreta por artículo sobre la tecnología que usamos sin pensar, como [cómo calcula el GPS tu posición](https://github.com/jossseluuu/HowThingsTalk/blob/main/docs/ES/05_Geolocalizacion/01-ComoCalculaElGPSTuPosicion.md) o [por qué los móviles cambian su dirección MAC](https://github.com/jossseluuu/HowThingsTalk/blob/main/docs/ES/11_PrivacidadYHuella/01-PorQueElMovilCambiaSuDireccionMAC.md). Claro para un principiante, riguroso para un experto.

- **Lees hasta donde quieras:** una respuesta de una frase, una analogía cotidiana y dónde falla, y después el mecanismo real con números.
- **Escrito dos veces, no traducido una:** cada artículo existe en español y en inglés.
- **Atemporal a propósito:** sin noticias, reseñas ni recomendaciones de compra; cada dato respaldado por fuentes primarias.

> 📰 **Un artículo nuevo cada día** desde el 1 de noviembre de 2026.

📖 **[Empieza a leer](https://github.com/jossseluuu/HowThingsTalk)**

<a id="es-zerotrace"></a>

#### 🚦 ZeroTrace · Ciberseguridad útil, un concepto al día

<sub>**Web estática con generador propio en Python (solo biblioteca estándar) · español e inglés** · contenido CC BY 4.0, código MIT</sub>

Ciberseguridad para todos sobre los dispositivos que usamos de verdad: qué puede hacer quien te roba el móvil después de verte teclear el código, por qué la nube no es una copia de seguridad o qué enseña un reloj sin código a quien lo coja.

- **Semáforo del día:** alertas sobre fallos explotados activamente o de gran alcance en dispositivos cotidianos, publicadas una sola vez y guardadas en un [registro de alertas](https://jossseluuu.github.io/ZeroTrace/es/alertas.html) público.
- **Dos niveles de lectura:** *Básico* en pocos minutos y *A fondo* para perfiles técnicos.
- **Medidas en su justa medida:** impacto y esfuerzo de cada medida, y lo que **no** hace falta hacer.
- **Sin fuente no hay dato:** cada dato y cada CVE enlazan a una fuente primaria, y las páginas no llevan cookies, rastreadores ni scripts de terceros.

> 📰 **Una edición nueva cada día** desde el 3 de noviembre de 2026.

📖 **[Léelo](https://jossseluuu.github.io/ZeroTrace/es/)** &nbsp;·&nbsp; 🇬🇧 **[In English](https://jossseluuu.github.io/ZeroTrace/en/)** &nbsp;·&nbsp; 📡 **[RSS](https://jossseluuu.github.io/ZeroTrace/es/feed.xml)** &nbsp;·&nbsp; 📂 **[Ver el repo](https://github.com/jossseluuu/ZeroTrace)**

### 🧩 Otros proyectos

| Proyecto | Qué es | Stack |
|---|---|---|
| 🧮 **[DataStructures-Algorithms](https://github.com/jossseluuu/DataStructures-Algorithms)** | Veintiuna estructuras de datos clásicas escritas desde cero (listas, pilas, colas, ABB, AVL, montículos, trie, tablas hash, conjuntos, grafos, union-find), además de búsqueda, seis algoritmos de ordenación, Dijkstra, Prim y Kruskal. Cada una con su prueba automática, versiones genéricas con plantillas y tablas de complejidad. | C++ · CMake |
| ✈️ **[airbaseQueue](https://github.com/jossseluuu/airbaseQueue)** | Simulación de eventos discretos del ciclo de salidas en tierra de una base de cazas (pista, combustible, inspección en hangar, mantenimiento). 30 réplicas Monte Carlo por escenario con intervalos de confianza al 95 %, validada con Erlang-C y la ley de Little; concluye que el cuello de botella es el mantenimiento, no la pista. Panel en Streamlit y 38 pruebas. | Python · SimPy · Streamlit |
| 🎞️ **[AlgorithmVisualizer](https://github.com/jossseluuu/AlgorithmVisualizer)** | Animaciones paso a paso de siete algoritmos de ordenación, dos búsquedas, cuatro de caminos (BFS, DFS, Dijkstra, A*) y cinco estructuras de datos. El backend ejecuta cada algoritmo una vez y devuelve todas las instantáneas, así que el lienzo las reproduce fotograma a fotograma a cualquier velocidad. | Flask · React · Vite · Canvas |
| 📈 **[InvestDashboard](https://github.com/jossseluuu/InvestDashboard)** | Un panel personal de cartera: precios en vivo convertidos a siete divisas, fundamentales y noticias por activo, gráficas de rentabilidad y un resumen semanal opcional por Telegram. Incluye una guía de despliegue en Railway y Vercel. | Flask · React · SQLite · Chart.js |
| ✈️ **[airline-database-project](https://github.com/jossseluuu/airline-database-project)** | Diseño de una base de datos relacional para la operativa de una aerolínea (pilotos, tripulación, vuelos, planes de vuelo, aeronaves, hangares y mantenimiento), con desglose del trabajo, análisis de riesgos de calidad de datos y una pequeña web. | MySQL · Flask · JavaScript |

### Tecnologías

Las tecnologías de los proyectos anteriores aparecen en la [tabla en inglés](#tech-stack). En la carrera y en cursos también he trabajado con C, Java, PHP, Bash, Django, Oracle, Power BI, Tableau y Figma; con Azure AI y Microsoft Defender XDR a través de Microsoft Learn; y con herramientas de seguridad como Wireshark, Nmap, Burp Suite y Kali Linux.

</details>

---

<div align="center">

### Let's talk · Hablemos

Working on something in backend, AI or security? I'd be glad to hear about it.<br>
¿Trabajas en algo de backend, IA o seguridad? Me encantará que me lo cuentes.

<a href="https://jossseluuu.github.io/eportfolio/"><img src="https://img.shields.io/badge/Portfolio-1A7F7A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"></a>
<a href="https://www.linkedin.com/in/joseluislop/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:jossseluuu@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>

</div>
