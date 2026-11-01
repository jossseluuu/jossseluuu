<div align="center">

<img src="assets/banner.png" alt="Banner" width="100%">

# Hi, I'm José Luis López 👋

<a href="https://github.com/jossseluuu">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=58A6FF&center=true&vCenter=true&width=640&lines=Final-Year+Computer+Science+%26+Engineering+Student;Building+AgentHQ%3A+an+AI+company+run+by+agents;Backend+%E2%80%A2+Applied+AI+%E2%80%A2+Security;Open+to+internships+and+junior+roles+worldwide+%F0%9F%8C%8D" alt="Typing SVG" />
</a>

<p>
  <a href="https://www.linkedin.com/in/joseluislop/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:jossseluuu@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Status-Open_to_work-2EA043?style=for-the-badge" alt="Open to work">
  <img src="https://komarev.com/ghpvc/?username=jossseluuu&style=for-the-badge&color=0A66C2&label=PROFILE+VIEWS" alt="Profile views">
</p>

<sub>🇬🇧 English · 🇪🇸 <a href="#-versión-en-español">Versión en español</a></sub>

</div>

---

## 👨‍💻 About Me

I'm a **final-year (4th) Computer Science & Engineering student** at the **Universidad de Granada (UGR)**, Spain. I spent a semester on exchange at the **University of Montana (USA)**, where I learned to work in English, in international teams and in a very different academic culture.

I like building software that is **useful, secure and easy to reason about**, and I prefer to prove what I learn by shipping complete projects: tests, CI, documentation and architecture decisions included.

**What I'm working on**

- 🏢 **[AgentHQ](https://github.com/jossseluuu/CompanyAgentsHQ)**, a personal project I designed and am building from scratch: a web app where you run a company staffed by AI agents (CEO, CTO, CFO…) from a live isometric office, with supervision, approvals, RAG knowledge bases and a tamper-evident audit log.
- 🔐 **[I-CPU](https://github.com/jossseluuu/I-CPU)**, an encrypted steganography tool in modern C++ with built-in steganalysis to measure how detectable each hidden message is.

**What I bring**

- ⚙️ **Backend & APIs** with Python (FastAPI, Flask, Django), PostgreSQL and Redis
- 🤖 **Applied AI**: LLM agents, tool use, RAG with pgvector, cost and safety controls
- 🛡️ **Security mindset**: applied cryptography, prompt-injection defences, least privilege, audit trails
- 🧪 **Engineering habits**: automated tests, CI, ADRs, Docker-based setups that run with one command

**What I'm looking for**

🎯 **Internships and junior roles** in backend, AI engineering or security, starting **2026–2027**. Remote or on-site, and **happy to relocate anywhere**. I speak Spanish (native) and English (professional).

<sub>Outside of code: ✈️ aviation and flight/ATC simulation · 🏋️ fitness · 🌍 travelling</sub>

---

## 🚀 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### 🏢 [AgentHQ](https://github.com/jossseluuu/CompanyAgentsHQ)
<sub>Personal project · 🚧 in active development</sub>

Run a company made of **AI agents** from a **2.5D isometric office**. Give a goal to the CEO agent and watch it plan, delegate to departments, get the work reviewed by supervisors and archive the results.

- Org chart of 8 agents with **supervision, escalation and approval inbox**
- **RAG** knowledge bases per company, department, room and agent
- **Append-only, hash-chained audit log** + an Auditor agent that flags anomalies
- **Per-agent budgets** and a daily AI spending cap
- Agents walk between rooms (A* pathfinding) to show what they're doing

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"> <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white"> <img src="https://img.shields.io/badge/PostgreSQL+pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"> <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">

</td>
<td width="50%" valign="top">

### 🔐 [I-CPU](https://github.com/jossseluuu/I-CPU)
<sub>Applied cryptography & steganography</sub>

Hide a text or a whole file inside an image so that, **without the password, it can't be read or even proven to exist**.

- **Three hiding domains**: pixel LSB (PNG, BMP…), **DCT coefficients** (JPEG, no recompression) and **palette indices** (GIF, even animated)
- **Argon2id + XChaCha20-Poly1305**; embedding positions derived from the password and an **encrypted header**
- **Built-in steganalysis** (chi-square, RS analysis) and distortion metrics (PSNR, SSIM)
- **CLI with guided mode + offline local web GUI**, CI and ADRs

<img src="https://img.shields.io/badge/C++20-00599C?style=flat-square&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white"> <img src="https://img.shields.io/badge/Cryptography-000000?style=flat-square&logo=letsencrypt&logoColor=white"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🛫 [openScope](https://github.com/jossseluuu/openScope)
<sub>Fork of an open-source ATC simulator</sub>

My own version of the **openScope** browser-based **Air Traffic Control simulator**, where I combine my passion for aviation with working on a **large, real-world JavaScript codebase** (Node build tooling, tests, GitFlow).

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"> <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white">

</td>
<td width="50%" valign="top">

### 🧮 [DataStructures-Algorithms](https://github.com/jossseluuu/DataStructures-Algorithms)
<sub>CS fundamentals</sub>

From-scratch **C++ implementations of data structures**, starting with linear structures, each one backed by its own **test suite**. Focus on memory management, complexity and clean interfaces.

<img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/Unit_tests-2EA043?style=flat-square">

</td>
</tr>
</table>

<sub>Also: 📈 <a href="https://github.com/jossseluuu/InvestDashboard">InvestDashboard</a>, a Flask + React investment portfolio dashboard with real-time prices, multi-currency FX and fundamentals.</sub>

---

## 🛠️ Tech Stack

| Area | Technologies |
|---|---|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![C++](https://img.shields.io/badge/C++20-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) |
| **Backend** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js_/_R3F-000000?style=flat-square&logo=threedotjs&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **AI / LLMs** | ![Claude API](https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white) ![RAG](https://img.shields.io/badge/RAG-6E40C9?style=flat-square) ![Agents](https://img.shields.io/badge/Multi--agent_systems-6E40C9?style=flat-square) ![Tool use](https://img.shields.io/badge/Tool_use-6E40C9?style=flat-square) |
| **Security** | ![Crypto](https://img.shields.io/badge/Argon2id_·_XChaCha20--Poly1305-000000?style=flat-square&logo=letsencrypt&logoColor=white) ![Steganalysis](https://img.shields.io/badge/Steganalysis-000000?style=flat-square) ![OWASP](https://img.shields.io/badge/OWASP_Top_10-000000?style=flat-square&logo=owasp&logoColor=white) |
| **DevOps & Quality** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white) |

---

## 📊 GitHub Stats

<div align="center">

<img src="./profile-summary-card-output/github_dark/0-profile-details.svg" alt="Profile details" width="100%">

<img src="./profile-summary-card-output/github_dark/3-stats.svg" alt="Stats" width="49%">
<img src="./profile-summary-card-output/github_dark/2-most-commit-language.svg" alt="Most committed languages" width="49%">

</div>

<sub>Cards generated daily by a GitHub Action inside this repo, so they don't depend on any external server.</sub>

---

## 🇪🇸 Versión en español

<details>
<summary><b>Haz clic para leer mi perfil completo en español</b></summary>
<br>

### 👨‍💻 Sobre mí

Soy **estudiante de último curso (4.º) de Ingeniería Informática** en la **Universidad de Granada (UGR)**. Pasé un semestre de intercambio en la **University of Montana (EE. UU.)**, donde aprendí a trabajar en inglés, en equipos internacionales y en una cultura académica muy distinta.

Me gusta construir software **útil, seguro y fácil de razonar**, y prefiero demostrar lo que aprendo con proyectos completos: con tests, integración continua, documentación y decisiones de arquitectura incluidas.

**En qué estoy trabajando**

- 🏢 **[AgentHQ](https://github.com/jossseluuu/CompanyAgentsHQ)**, un proyecto personal que he diseñado y estoy construyendo desde cero: una aplicación web para dirigir una empresa formada por agentes de IA (CEO, CTO, CFO…) desde una oficina isométrica en tiempo real, con supervisión, aprobaciones, bases de conocimiento RAG y un registro de auditoría a prueba de manipulaciones.
- 🔐 **[I-CPU](https://github.com/jossseluuu/I-CPU)**, una herramienta de esteganografía cifrada en C++ moderno con estegoanálisis integrado para medir lo detectable que es cada mensaje oculto.

**Qué aporto**

- ⚙️ **Backend y APIs** con Python (FastAPI, Flask, Django), PostgreSQL y Redis
- 🤖 **IA aplicada**: agentes con LLMs, uso de herramientas, RAG con pgvector, control de costes y de seguridad
- 🛡️ **Mentalidad de seguridad**: criptografía aplicada, defensa ante *prompt injection*, mínimo privilegio, trazabilidad
- 🧪 **Buenas prácticas**: tests automatizados, CI, ADRs y entornos con Docker que arrancan con un solo comando

**Qué busco**

🎯 **Prácticas y puestos junior** en backend, ingeniería de IA o ciberseguridad, a partir de **2026–2027**. En remoto o presencial, y con **total disposición a cambiar de ciudad o de país**. Idiomas: español (nativo) e inglés (profesional).

### 🚀 Proyectos destacados

| Proyecto | Qué es |
|---|---|
| 🏢 [**AgentHQ**](https://github.com/jossseluuu/CompanyAgentsHQ) | Proyecto personal en desarrollo. Empresa de agentes de IA con organigrama, supervisión, bandeja de aprobaciones, RAG y auditoría encadenada con hashes. FastAPI · React Three Fiber · PostgreSQL + pgvector · Redis · Claude API · Docker |
| 🔐 [**I-CPU**](https://github.com/jossseluuu/I-CPU) | Esteganografía cifrada en tres dominios (píxeles, DCT de JPEG y paleta GIF) con Argon2id + XChaCha20-Poly1305, estegoanálisis y métricas PSNR/SSIM. CLI y GUI web local. C++20 · CMake |
| 🛫 [**openScope**](https://github.com/jossseluuu/openScope) | Mi versión del simulador de control de tráfico aéreo openScope: aviación y un código JavaScript grande y real |
| 🧮 [**DataStructures-Algorithms**](https://github.com/jossseluuu/DataStructures-Algorithms) | Estructuras de datos implementadas desde cero en C++, cada una con su batería de tests |

<sub>Fuera del código: ✈️ aviación y simulación de vuelo y control aéreo · 🏋️ fitness · 🌍 viajar</sub>

</details>

---

<div align="center">

### 📫 Let's talk · Hablemos

Hiring for an internship or junior role? I'd love to hear from you on **[LinkedIn](https://www.linkedin.com/in/joseluislop/)** or by **[email](mailto:jossseluuu@gmail.com)**.

</div>
