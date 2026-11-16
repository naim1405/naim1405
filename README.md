<div align="center">

# Md Naimuzzaman

**Backend engineer** · BSc CSE @ RUET (2027) · Co-founder @ DeveloFirm

<a href="https://linkedin.com/in/naim14"><img src="https://img.shields.io/badge/LinkedIn-naim14-0A66C2?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAyNCAyNCc%2BPHRpdGxlPkxpbmtlZEluPC90aXRsZT48cGF0aCBmaWxsPSd3aGl0ZScgZD0nTTIwLjQ0NyAyMC40NTJoLTMuNTU0di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzctMS44NTItMy4wMzctMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2N0g5LjM1MVY5aDMuNDE0djEuNTYxaC4wNDZjLjQ3Ny0uOSAxLjYzNy0xLjg1IDMuMzctMS44NSAzLjYwMSAwIDQuMjY3IDIuMzcgNC4yNjcgNS40NTV2Ni4yODZ6TTUuMzM3IDcuNDMzYTIuMDYyIDIuMDYyIDAgMDEtMi4wNjMtMi4wNjUgMi4wNjQgMi4wNjQgMCAxMTIuMDYzIDIuMDY1em0xLjc4MiAxMy4wMTlIMy41NTVWOWgzLjU2NHYxMS40NTJ6TTIyLjIyNSAwSDEuNzcxQy43OTIgMCAwIC43NzQgMCAxLjcyOXYyMC41NDJDMCAyMy4yMjcuNzkyIDI0IDEuNzcxIDI0aDIwLjQ1MUMyMy4yIDI0IDI0IDIzLjIyNyAyNCAyMi4yNzFWMS43MjlDMjQgLjc3NCAyMy4yIDAgMjIuMjI1IDB6Jy8%2BPC9zdmc%2B" alt="LinkedIn: naim14" /></a>
<a href="mailto:naim.baijid@gmail.com"><img src="https://img.shields.io/badge/naim.baijid@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email: naim.baijid@gmail.com" /></a>
<img src="https://img.shields.io/badge/Rajshahi%2C%20Bangladesh-4B5563?style=flat-square&logo=googlemaps&logoColor=white" alt="Location: Rajshahi, Bangladesh" />

</div>

I build backends that hold up under real users and occasionally go one layer deeper — down to a kernel in C and Assembly. Most of what's here started as a problem I watched someone actually struggle with.

**Right now:** building [market-mind](https://github.com/naim1405/market-mind), an AI copilot for Bangladeshi F-commerce sellers, and looking for backend / applied-AI engineering roles.

---

<!--
  Badge note: shields.io no longer ships a LinkedIn glyph (logo=linkedin silently renders
  nothing), so the LinkedIn badge embeds its own SVG as a base64 data URI. That is why
  that one URL is ~830 chars long. Don't "clean it up" to logo=linkedin — the icon vanishes.
-->

## 🚀 Featured

### [neoRMS](https://github.com/naim1405/neoRMS-backend) — multi-tenant restaurant platform
Backend for a 6-service platform, coordinated as a git-submodule monorepo. **13 modules over a 23-entity Prisma schema** covering orders, inventory, tables, coupons, payments, and AI-scored reviews.

What's interesting in the code: tenant isolation enforced as a per-request middleware that re-verifies user→tenant membership against Postgres — and the **same guard extended to the Socket.IO handshake**, which is where most multi-tenant systems quietly leak. Three role-scoped namespaces (waiter / chef / customer) push order state over rooms. SSLCommerz checkout with a deliberately unauthenticated server-to-server `IPN` callback and server-side verification.

`TypeScript` `Express` `Prisma` `PostgreSQL` `Socket.IO` · *Brain Station 23 industrial attachment*

### [VisionGuard.ai](https://github.com/naim1405/visionguard) — real-time shoplifting detection
Camera feeds streamed over WebRTC to a live Next.js dashboard, with alerts pushed over persistent WebSockets. Server GPU cost cut by moving person detection client-side and chaining **YOLO** with an **STG-NF** pose-anomaly model; Telegram alerting plus heartbeat-based reconnect for unreliable networks.

**SOLVIO AI Hackathon 2025 — 1st Runner-Up** out of 20 finalist teams.

`Python` `PyTorch` `aiortc` `Next.js`

### [nullOS](https://github.com/naim1405/nullOS) — x86 kernel from scratch
A 32-bit kernel written from nothing in C and Assembly: bootloader → protected mode, higher-half memory layout, GDT, IDT, PIC remapping, IRQ-driven keyboard and serial drivers, page table mappers. Currently at a booting higher-half kernel; memory management and scheduling are next.

`C` `x86 Assembly` `QEMU` `Makefile`

---

## 🧰 More projects

| Project | What it is |
|---|---|
| [**rlvr**](https://github.com/naim1405/rlvr) | LLM post-training pipeline — LoRA SFT → GRPO/RLVR, with **7 hand-written reward verifiers** and a reward-soundness audit (exact rational comparison, constraint-satisfaction scoring, output-form checks) after finding that naive equivalence scoring let an unevaluated restatement of the prompt earn full marks. `Python` `PyTorch` `NeMo` |
| [**QueueStorm-Investigator**](https://github.com/naim1405/QueueStorm-Investigator) | Fintech support copilot: batched Gemini calls with per-response routing, a **per-API-key Redis sliding-window rate limiter with dead-key cooldown**, Prometheus metrics, and hard-coded safety rails that refuse to promise refunds or solicit OTP/PIN. `TypeScript` `Redis` `Gemini` |
| [**true-recall**](https://github.com/naim1405/true-recall) | Per-monitor focus switching for Windows, niri-style: tray icon, global hotkey manager, INI config, shortcut-conflict detection. MIT licensed. `C++` `Win32` `CMake` |
| [**tempCheck-compiler**](https://github.com/naim1405/tempCheck-compiler) | Flex/Bison compiler for a temperature-monitoring DSL — lexer and parser done, symbol table and type checking in progress, TAC and codegen planned. `C` `Flex` `Bison` |
| [**phone-price-prediction**](https://github.com/naim1405/phone-price-prediction) | scikit-learn pipeline + Gradio UI for device price-range classification. `Python` `scikit-learn` |
| [**dotfiles**](https://github.com/naim1405/dotfiles) | Linux / Hyprland / Neovim setup and install scripts. `Lua` `Shell` |

---

## 🛠️ Stack

| | |
|---|---|
| **Languages** | TypeScript · JavaScript · Python · C · C++ · x86 Assembly · SQL |
| **Backend** | Node.js · Express · FastAPI · PostgreSQL · MongoDB · Redis · Socket.IO · Prisma |
| **Frontend / Mobile** | React · React Native · Expo · Next.js · Tailwind CSS |
| **Infra & tooling** | Docker · Linux · Git · GitHub Actions (CI/CD) · pytest · WebSockets · WebRTC · QEMU |

---

## 🏆 Recognition

- **ITEE Fundamental IT Engineer (FE)** — ranked **1st in Bangladesh**, ITPEC, Aug 2024
- **SOLVIO AI Hackathon 2025** — 1st Runner-Up (20 finalist teams), Sheba Platform Ltd
- **University Innovation Hub Program** — 1st Place, RUET; pre-seed funding for Bebsapati

---

## 💼 Currently

Co-founder at **DeveloFirm**, where we built **Bebsapati**, a multi-tenant SaaS for SMEs — **900+ owner accounts registered** through paid campaigns, with an active panel of users driving weekly feedback and iteration.

Open to **backend and applied-AI engineering roles**. Reach me at [naim.baijid@gmail.com](mailto:naim.baijid@gmail.com) or on [LinkedIn](https://linkedin.com/in/naim14).
