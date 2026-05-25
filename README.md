<div align="center">

<!-- Animated Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=🛒%20ShopForge&fontSize=60&fontColor=fff&animation=twinkling&fontAlignY=35&desc=A%20Production-Grade%20Java%20E-Commerce%20Backend&descAlignY=58&descSize=18" width="100%"/>

<!-- Live Badges Row -->
<p>
  <img src="https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
</p>

<p>
  <img src="https://img.shields.io/badge/Phase-1%20%E2%80%94%20Foundation-FF6B6B?style=flat-square"/>
  <img src="https://img.shields.io/badge/Coverage-JaCoCo-45CC11?style=flat-square"/>
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Contributions-Open-orange?style=flat-square"/>
</p>

<br/>

> **A hands-on, real-world Java backend built to learn, contribute to, and eventually run in production.**  
> From DAO to microservices — one phase at a time.

<br/>

</div>

---

## 🚀 What is this?

A full-stack **Java + Spring Boot** e-commerce backend, structured like a professional project — not a tutorial throwaway. The goal is to evolve this into something:

- ⚡ **Runnable locally in under 5 minutes**
- 🧪 **Safe to contribute to** — CI enforced, no broken main
- 🏗️ **Structured like real production Java backends**
- 🛍️ **Complete** — covering the full e-commerce lifecycle end to end
- 📚 **Useful as a study resource** for system design and scalability

---

## ⚡ Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/your-org/shopforge.git
cd shopforge

# 2. Start everything with Docker Compose
docker compose up --build

# 3. Open the app
open http://localhost:8080
```

> 💡 Requires Docker Desktop. No local Java or MySQL install needed.

---

## 🗺️ Roadmap at a Glance

<div align="center">

```
Phase 1 ──────────── Phase 2 ──────────── Phase 3 ──────────── Phase 4
Foundation           E-Commerce           Production            Microservices
   ✅                   🔄                   📋                    🔭
   
Stable · Tested      Full Cart Flow       Redis · Search        Kafka · Events
CI · Docker          Auth · Orders        Observability         Service Boundaries
Java 17 Upgrade      Swagger Docs         Caching & Locks       Decomp Guide
```

</div>

---

## 📦 Phase 1 — Foundation *(Active)*

> **Goal:** Make this reliable to run, easy to contribute to, stable enough to build on.

| Area | Task | Difficulty | Status |
|------|------|------------|--------|
| 🐛 **Stability** | Resolve high-impact open bugs | `help wanted` | Planned |
| 🐛 **Stability** | Standardize error handling across controllers | `help wanted` | Planned |
| 🐛 **Stability** | Clean up dead code and inconsistent naming | `help wanted` | Planned |
| 🐳 **Dev Setup** | Docker Compose — one-command local startup | `help wanted` | **In Progress** |
| ⚙️ **Dev Setup** | GitHub Actions CI on every PR | `help wanted` | **In Progress** |
| 📝 **Dev Setup** | Issue & PR templates under `.github/` | `good first issue` | Planned |
| 📝 **Dev Setup** | `CONTRIBUTING.md` — branches, commits, setup | `good first issue` | Planned |
| 🔍 **Dev Setup** | Checkstyle integration in build + CI | `help wanted` | Planned |
| 🔍 **Dev Setup** | Separate config profiles: dev / test / prod | `help wanted` | Planned |
| ☕ **Platform** | Upgrade to Java 17 + Spring Boot 3.x | `advanced` | Planned |
| ☕ **Platform** | Migrate `javax.*` → `jakarta.*` | `help wanted` | Planned |
| ☕ **Platform** | Verify Hibernate, security, plugin compatibility | `advanced` | Planned |
| 🧪 **Testing** | Unit tests — all service classes (JUnit 5 + Mockito) | `good first issue` | Planned |
| 🧪 **Testing** | Controller tests using `@WebMvcTest` | `help wanted` | Planned |
| 🧪 **Testing** | JaCoCo coverage report + README badge | `good first issue` | Planned |
| 🧪 **Testing** | DAO-level tests with Testcontainers MySQL | `advanced` | Planned |

**✅ Phase 1 is done when:**
- A new contributor can clone → run by following the README alone
- Every PR triggers automated build + test checks
- Core modules have baseline test coverage
- `main` stays green for 30 straight days

---

## 🛍️ Phase 2 — E-Commerce Flow

> **Goal:** A real, end-to-end shopping experience — not just a skeleton.

<details>
<summary><b>Click to expand Phase 2 tasks</b></summary>

| Area | Task | Difficulty |
|------|------|------------|
| 🛒 **Cart** | Full lifecycle: add, update, remove, clear | `help wanted` |
| 🛒 **Cart** | Checkout flow with order placement + confirmation | `advanced` |
| 🛒 **Cart** | Order status: created → paid → shipped → delivered | `help wanted` |
| 🏗️ **Arch** | Global exception handler | `help wanted` |
| 🏗️ **Arch** | Pagination + sorting for products & customers | `good first issue` |
| 🏗️ **Arch** | Database migrations with Flyway | `help wanted` |
| 🏗️ **Arch** | Structured logging with SLF4J | `help wanted` |
| 📦 **Products** | Image upload (multipart) + cloud-ready abstraction | `advanced` |
| 📦 **Products** | Product search by name and category | `good first issue` |
| 📦 **Products** | Out-of-stock handling — disable add-to-cart at 0 qty | `good first issue` |
| 🔐 **Auth** | Password reset via time-limited token | `advanced` |
| 🔐 **Auth** | Email verification on registration | `advanced` |
| 🔐 **Auth** | Remember-me login | `help wanted` |
| 🔐 **Auth** | Multiple shipping addresses per user | `help wanted` |
| 📄 **Docs** | Swagger UI / OpenAPI 3 integration | `good first issue` |

</details>

---

## ⚙️ Phase 3 — Production Patterns

> **Goal:** Patterns that separate hobby projects from production systems.

<details>
<summary><b>Click to expand Phase 3 tasks</b></summary>

| Area | Task | Difficulty |
|------|------|------------|
| 🚀 **Performance** | DB indexes + query plan documentation | `help wanted` |
| 🚀 **Performance** | Redis caching for read-heavy endpoints | `advanced` |
| 🚀 **Performance** | Connection pool tuning + benchmarking | `help wanted` |
| 🔒 **Concurrency** | Optimistic locking for inventory conflicts | `advanced` |
| 🔒 **Concurrency** | Pessimistic locking demo with tradeoff docs | `advanced` |
| 🔎 **Search** | Elasticsearch for full-text product search | `advanced` |
| 🔎 **Search** | SQL search fallback for local environments | `help wanted` |
| 🎨 **Patterns** | Strategy pattern — payment options (COD, card, UPI) | `advanced` |
| 🎨 **Patterns** | Factory pattern — discounts and coupon logic | `advanced` |
| 📊 **Observability** | Spring Boot Actuator: health, metrics, info | `good first issue` |
| 📊 **Observability** | Prometheus + Grafana via Docker Compose | `advanced` |
| 📊 **Observability** | Logback JSON structured logging | `help wanted` |

</details>

---

## 🌐 Phase 4 — Microservices & System Design

> **Goal:** Show how to decompose this monolith — without breaking it as a learning resource.

<details>
<summary><b>Click to expand Phase 4 tasks</b></summary>

| Area | Task | Difficulty |
|------|------|------------|
| 📐 **Design** | Service boundary plan: user / product / order / notification | `discussion` |
| 📐 **Design** | Monolith vs microservices tradeoffs with real examples | `discussion` |
| 📨 **Events** | Kafka-based order events with subscribers | `advanced` |
| 📨 **Events** | Eventual consistency + retry patterns demo | `advanced` |

</details>

---

## 🔁 Ongoing Maintenance

> Runs in parallel across all phases.

| Area | Task | Difficulty |
|------|------|------------|
| 🤖 **Automation** | Dependabot for `pom.xml` updates | `good first issue` |
| 🤖 **Automation** | Stale bot for inactive issues/PRs | `good first issue` |
| 🤖 **Automation** | PR size labeler (S / M / L) | `good first issue` |
| 📚 **Docs** | `docs/adr/` architecture decision records | `good first issue` |
| 📚 **Docs** | `docs/architecture.md` with Mermaid component diagram | `good first issue` |
| 📚 **Docs** | `SECURITY.md` with responsible disclosure info | `good first issue` |
| 📚 **Docs** | Learning path: DAO → Service → Controller → View | `good first issue` |

---

## 🏁 Top 5 Priorities Right Now

```
┌────┬──────────────────────────────────────────┐
│ #1 │ 🐳  Docker Compose local setup            │
│ #2 │ ⚙️  GitHub Actions CI on pull requests    │
│ #3 │ 📝  CONTRIBUTING.md + issue/PR templates  │
│ #4 │ 🧪  Baseline service and controller tests │
│ #5 │ ☕  Java 17 + Spring Boot 3 migration     │
└────┴──────────────────────────────────────────┘
```

---

## 🤝 How to Contribute

**New here?**
→ Pick a `good first issue` from Phase 1. Open a draft PR early — questions welcome.

**Regular contributor?**
→ Take on `help wanted` items from the active phase. Tests, docs, and migration notes belong in the same PR.

**Maintainer?**
→ Keep labels and the phase board up to date. Reject feature PRs that skip tests or documentation.

### PR Checklist

Before marking a PR ready to merge:

- [ ] CI passes — build + tests green
- [ ] Tests cover the changed behavior
- [ ] Scope is focused — no mega PRs
- [ ] Docs updated if behavior or setup changed
- [ ] Rollback notes included for any risky changes

---

## 🏷️ Labels

```
roadmap/phase-1     roadmap/phase-2     roadmap/phase-3     roadmap/phase-4
good first issue    help wanted         advanced            discussion
blocked             priority/high       priority/medium     priority/low
```

---

## 📂 Project Structure

```
shopforge/
├── src/
│   ├── main/
│   │   ├── java/com/shopforge/
│   │   │   ├── controller/       # Spring MVC controllers
│   │   │   ├── service/          # Business logic
│   │   │   ├── dao/              # Data access layer
│   │   │   ├── model/            # JPA entities
│   │   │   └── config/           # App configuration
│   │   └── resources/
│   │       ├── application.yml
│   │       └── templates/        # JSP views
│   └── test/                     # JUnit 5 tests
├── docs/
│   ├── adr/                      # Architecture decisions
│   └── architecture.md
├── .github/
│   ├── workflows/                # CI pipelines
│   └── ISSUE_TEMPLATE/
├── docker-compose.yml
├── CONTRIBUTING.md
└── pom.xml
```

---

## 🎯 End Goal

When this roadmap is complete, the project will be:

| ✅ | What |
|----|------|
| ⚡ | Runnable locally in under 5 minutes |
| 🔒 | Safe to contribute to — no guessing, no broken main |
| 🏗️ | Structured like a real professional Java backend |
| 🛍️ | Complete — covering the full e-commerce lifecycle |
| 📚 | Useful as a study resource for system design and scalability |

> **What this project won't do:**
> - Migrate to a different backend framework (Quarkus, Micronaut, etc.)
> - Replace JSP views with a React/Vue frontend
>
> The goal is to evolve and improve what's here — not rewrite from scratch.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" width="100%"/>

**Built with ☕ Java · 🌱 Spring Boot · ❤️ Open Source**

*Star ⭐ the repo if this helped you learn something.*

</div>
