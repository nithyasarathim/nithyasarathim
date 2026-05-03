<!--
╔══════════════════════════════════════════════════════════════════════════════╗
║   NITHYASARATHI M — GitHub Profile README                                  ║
║   © 2025 Nithyasarathi M. All rights reserved.                             ║
║   Written and designed personally by the author.                           ║
╚══════════════════════════════════════════════════════════════════════════════╝
-->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0ea5e9&height=280&section=header&text=Nithyasarathi%20M&fontSize=72&fontColor=ffffff&fontAlignY=42&desc=Full%20Stack%20Web%20Developer%20%7C%20Student%20Mentor%20%7C%20CSE%20Final%20Year&descSize=16&descAlignY=60&descColor=bae6fd&animation=fadeIn&stroke=0&strokeWidth=0" width="100%" alt="Nithyasarathi M" />

</div>

<br/>

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=0EA5E9&center=true&vCenter=true&width=700&lines=Final+Year+CSE+Student+%26+Full+Stack+Builder.;Exploring+Multi-tenant+Architectures+%26+Gateways.;Knight+Rank+on+LeetCode+%7C+Problem+Solver.;Helping+peers+grow+at+the+Center+of+Excellence.;Building+Auth+Systems+and+Scalable+Web+Apps.)](https://git.io/typing-svg)

</div>

<br/>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%40nithyasarathim-0ea5e9?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0c4a6e)](https://www.linkedin.com/in/nithyasarathim)&nbsp;
[![LeetCode](https://img.shields.io/badge/LeetCode-Knight%20%F0%9F%8F%85-0ea5e9?style=for-the-badge&logo=leetcode&logoColor=white&labelColor=0c4a6e)](https://www.leetcode.com/u/nithyasarathim)&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-%40nithyasarathim-0ea5e9?style=for-the-badge&logo=github&logoColor=white&labelColor=0c4a6e)](https://www.github.com/nithyasarathim)&nbsp;
[![Email](https://img.shields.io/badge/Gmail-contact.nithyasarathi-0ea5e9?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0c4a6e)](mailto:contact.nithyasarathi@gmail.com)

</div>

---

<br/>

## ◈ &nbsp;Who I Am

<img align="right" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs?username=nithyasarathim&layout=compact&theme=transparent&title_color=0ea5e9&text_color=cbd5e1&bg_color=0f172a&border_color=1e3a5f&border_radius=10&langs_count=7&hide=html" height="140" alt="Top Languages" />

I'm a final-year Computer Science student and a full-stack engineer who spends a lot of time thinking about _how systems hold together_ — not just whether the code runs.

The questions I keep coming back to are infrastructure-level ones: how a session token moves through Redis without becoming a liability, why an authorization-code flow is meaningfully safer than handing a client a password, where the right boundary is when splitting a service. These aren't academic interests — they pushed me toward building actual systems rather than accumulating tutorials.

Outside engineering, I teach. Every weekend session I run at the Center of Excellence forces me to re-examine something I thought I already understood. Mentoring is the most honest form of self-assessment I've found.

<br clear="right"/>

---

<br/>

## ◈ &nbsp;Tech Stack

```
Languages    →   C · C++ · Java · JavaScript (ES6+) · TypeScript
Frontend     →   React · Next.js · Vite · Tailwind CSS · HTML5 · CSS3
Backend      →   Node.js · Express 5 · Microservices · REST
Databases    →   MongoDB · Mongoose · Redis · SQL
Auth         →   JWT · SSO (Auth Code Flow) · HMAC SHA-256 · HTTP-only Cookies
Tooling      →   Git · Docker · SonarCloud · ImageKit · VS Code
Core CS      →   OOP · DBMS · Operating Systems · Computer Networks
```

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-0ea5e9?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-0ea5e9?style=flat-square&logo=javascript&logoColor=white)
![React](https://img.shields.io/badge/React-0ea5e9?style=flat-square&logo=react&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-0ea5e9?style=flat-square&logo=next.js&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-0ea5e9?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express%205-0ea5e9?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-0ea5e9?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-0ea5e9?style=flat-square&logo=redis&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind%20CSS-0ea5e9?style=flat-square&logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-0ea5e9?style=flat-square&logo=docker&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-0ea5e9?style=flat-square&logo=vite&logoColor=white)
![Git](https://img.shields.io/badge/Git-0ea5e9?style=flat-square&logo=git&logoColor=white)

</div>

---

<br/>

## ◈ &nbsp;Featured Work

<br/>

> [!NOTE]
>
> ### 🔐 &nbsp;OneAuth — First-Party SSO Platform
>
> _Three services. One identity layer. Zero password leaks to downstream products._

The idea was straightforward: instead of every product I build owning its own login screen, session logic, and password storage — pull all of that into a dedicated platform any product can delegate to. What came out was a three-service system built around an authorization-code flow. Client applications get a signed JWT they can trust without ever handling a credential directly.

<br/>

**Flow at a glance:**

```
Client App  →  OneAuth Portal  →  Session Check  →  Validate client_id & redirect URI
           →  Auth Code in Redis (60s TTL)  →  Product backend exchanges for JWT
           →  /sso/userinfo returns verified identity
```

> The product backend never touches a password. The session lives in Redis via an HTTP-only cookie — revoke the Redis key and the session is gone, everywhere, instantly.

<br/>

---

### &nbsp;&nbsp;&nbsp;&nbsp;📦 &nbsp;OneAuth API

> [!IMPORTANT]
> **Identity authority** — sessions, SSO, user profiles, avatar storage

<div align="center">

[![Quality Gate](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Reliability](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Maintainability](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=bugs)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-api&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-api)

</div>

<br/>

`Express 5` &nbsp;·&nbsp; `MongoDB / Mongoose` &nbsp;·&nbsp; `Redis` &nbsp;·&nbsp; `JWT` &nbsp;·&nbsp; `ImageKit CDN` &nbsp;·&nbsp; `TypeScript`

<br/>

**Architecture decisions worth explaining:**

> [!TIP]
> **Two-layer session model** — The cookie carries a token string. Redis carries the ground truth. Logout is a Redis key deletion — instant, and complete. The `sessionValidator` middleware confirms the Redis entry on every protected request. No stale-cookie attack surface.

> [!TIP]
> **Per-route rate limiting** — Every endpoint has a deliberate middleware stack sized to its risk: `requestLogger → rateLimiter(n) → authenticator → sessionValidator → controller`. Avatar upload allows 2 requests per window. Profile read allows 60. One number for everything is a lazy default I chose not to make.

> [!TIP]
> **Exact-match SSO allowlists** — Redirect URIs and client IDs are validated against environment-level CSV variables. No wildcards. An unrecognized redirect URI gets a hard reject before an authorization code is ever generated — preventing open-redirect vulnerabilities at the boundary, not in application logic.

> [!TIP]
> **Fail-fast startup** — `configs/env.ts` validates every required environment variable at boot time. The server refuses to start rather than run silently with a broken configuration.

<div align="center">

[![→ View Repository](https://img.shields.io/badge/%E2%86%92%20OneAuth%20API%20Repository-0ea5e9?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nithyasarathim/OneAuth-api)

</div>

<br/>

---

### &nbsp;&nbsp;&nbsp;&nbsp;📦 &nbsp;OneMail API

> [!IMPORTANT]
> **Stateless OTP delivery microservice** — HMAC-signed, replay-resistant

<div align="center">

[![Quality Gate](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Reliability](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Maintainability](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=bugs)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneMail-api&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneMail-api)

</div>

<br/>

`Express 5` &nbsp;·&nbsp; `Nodemailer / SMTP` &nbsp;·&nbsp; `HMAC SHA-256` &nbsp;·&nbsp; `Winston` &nbsp;·&nbsp; `TypeScript`

<br/>

This service exists because authentication and email delivery have no business being in the same codebase. OneAuth generates and verifies OTPs. OneMail receives a signed request, validates it, renders an HTML template, and dispatches via SMTP. That is the full scope of its responsibility.

> [!WARNING]
> **Security model:** A `to:otp:timestamp` payload signed with HMAC SHA-256 against a shared secret. OneMail regenerates the digest on arrival and compares using `crypto.timingSafeEqual`. Production replay window is **two minutes** — anything older returns `410 Gone`. The service holds **zero state**: no database, no user records, no sessions.

<div align="center">

[![→ View Repository](https://img.shields.io/badge/%E2%86%92%20OneMail%20API%20Repository-0ea5e9?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nithyasarathim/OneMail-api)

</div>

<br/>

---

### &nbsp;&nbsp;&nbsp;&nbsp;📦 &nbsp;OneAuth Client

> [!IMPORTANT]
> **React 19 SPA** — Shared authentication portal for all SSO-connected products

<div align="center">

[![Quality Gate](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Reliability](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Maintainability](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=bugs)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=nithyasarathim_OneAuth-client&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=nithyasarathim_OneAuth-client)

</div>

<br/>

`React 19` &nbsp;·&nbsp; `Vite` &nbsp;·&nbsp; `TypeScript` &nbsp;·&nbsp; `Axios` &nbsp;·&nbsp; `React Router`

<br/>

The codebase is organized by workflow, not by layer. Login, registration, profile, and SSO each own their components, API calls, validators, and types — kept together where they're actually used.

> [!TIP]
> A `GlobalAPIWatcher` registers an Axios response interceptor at startup: any `401` from anywhere in the app routes the user to login cleanly, original path preserved in a `?redirect=` query param. One centralized escape hatch instead of handling session expiry in every component.

<div align="center">

[![→ View Repository](https://img.shields.io/badge/%E2%86%92%20OneAuth%20Client%20Repository-0ea5e9?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nithyasarathim/OneAuth-client)

</div>

<br/>

---

### 📋 &nbsp;DSA Roadmap — 200+ Curated Problems

> [!NOTE]
> **A structured path through Data Structures and Algorithms. Every problem is there for a reason.**

Most DSA resources overwhelm before they orient. This sheet takes the opposite approach — a handpicked set of 200+ problems organized by topic, difficulty, and priority, designed to build intuition progressively rather than just grow a solved count.

I built it because I needed it first. Then peers kept asking for it.

<div align="center">

[![LeetCode Knight](https://img.shields.io/badge/LeetCode%20Rank-Knight%20%F0%9F%8F%85-0ea5e9?style=for-the-badge&logo=leetcode&logoColor=white)](https://www.leetcode.com/u/nithyasarathim)&nbsp;&nbsp;
[![→ View DSA Roadmap](https://img.shields.io/badge/%E2%86%92%20View%20DSA%20Roadmap-0ea5e9?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nithyasarathim)

</div>

---

<br/>

## ◈ &nbsp;GitHub Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=nithyasarathim&show_icons=true&title_color=0ea5e9&icon_color=38bdf8&text_color=cbd5e1&bg_color=0f172a&border_color=1e3a5f&border_radius=10&include_all_commits=true&count_private=true&rank_icon=github" height="180" alt="GitHub Stats" />
&nbsp;&nbsp;
<img src="https://github-readme-streak-stats.herokuapp.com/?user=nithyasarathim&ring=0ea5e9&fire=38bdf8&currStreakLabel=0ea5e9&sideLabels=cbd5e1&dates=64748b&background=0f172a&border=1e3a5f&border_radius=10&stroke=1e3a5f" height="180" alt="Streak Stats" />

</div>

<br/>

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=nithyasarathim&bg_color=0f172a&color=cbd5e1&line=0ea5e9&point=38bdf8&area=true&area_color=0c4a6e&hide_border=false&border_color=1e3a5f&radius=8" width="96%" alt="Contribution Graph" />

</div>

---

<br/>

## ◈ &nbsp;Experience

> [!NOTE]
>
> ### 🏢 &nbsp;Presidio Solutions &nbsp;·&nbsp; _Top 10 of 1000+ participants_

The selection itself was a filter. Working there changed how I think about code — from _"does it run"_ to _"does it belong in a team's codebase six months from now."_ Version control discipline, RAG pipeline integration, DevOps basics, and working inside an opinionated review culture. The kind of things that don't show up in coursework but define professional engineering.

<br/>

> [!NOTE]
>
> ### 🏢 &nbsp;Quantumpulse Technologies &nbsp;·&nbsp; _Full Stack Development Intern_

Contributed to a Learning Management System — MERN stack, responsive design, standard practices. Useful for learning what it looks like to extend an existing codebase responsibly rather than starting from scratch.

---

<br/>

## ◈ &nbsp;Beyond the Code

> [!TIP]
> **🎓 Student Mentor — Center of Excellence, Full Stack Development**
>
> I design learning roadmaps and run weekend sessions on Express, Tailwind, and full-stack patterns for students just getting started. The reason I keep doing it is partly selfish — teaching is the fastest way to find the gaps in what I thought I understood.

<br/>

> [!TIP]
> **🛠️ Mentoring Club**
>
> Built an internal real-time tracking tool that replaced spreadsheets for monitoring participation and soft-skill progress across 100+ students. It came from a genuine gap, not a project idea.

<br/>

> [!TIP]
> **📌 Placement Coordinator**
>
> Organized drives, managed communication between companies and students, and helped peers navigate recruitment. The unglamorous coordination work that makes hiring seasons function.

---

<br/>

## ◈ &nbsp;Let's Talk

Systems design, authentication architecture, full-stack engineering — these are the kinds of conversations I genuinely enjoy. If you're building something interesting or want to collaborate, reach out.

<div align="center">

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0ea5e9?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nithyasarathim)&nbsp;
[![Email](https://img.shields.io/badge/Gmail-0ea5e9?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contact.nithyasarathi@gmail.com)&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-0ea5e9?style=for-the-badge&logo=github&logoColor=white)](https://www.github.com/nithyasarathim)&nbsp;
[![LeetCode](https://img.shields.io/badge/LeetCode-0ea5e9?style=for-the-badge&logo=leetcode&logoColor=white)](https://www.leetcode.com/u/nithyasarathim)

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,2,5,30&height=130&section=footer&animation=fadeIn" width="100%" alt="footer" />

<sub>Written and designed by Nithyasarathi M &nbsp;·&nbsp; © 2025 All rights reserved</sub>

</div>
