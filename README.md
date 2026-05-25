# Project Roadmap

This file tracks the direction and planned improvements for this project.

**Why this exists:**
- To keep the codebase moving toward something production-ready and well-structured.
- To serve as a hands-on learning reference for real-world Java backend development.

**How to pick up work:**
- `[good first issue]` — new here? start here.
- `[help wanted]` — mid-level tasks, some context needed.
- `[advanced]` — architecture or migration heavy.
- `[discussion]` — open for proposal before any code is written.

**Status labels:**
- `Planned` — approved, not started yet.
- `In Progress` — being worked on.
- `Completed` — merged and documented.

---

## End Goal

When this roadmap is done, the project should be:
- Runnable locally in under 5 minutes.
- Safe to contribute to — no guessing, no broken main branch.
- Structured the way a professional Java backend project actually looks.
- Complete enough to demonstrate the full e-commerce lifecycle end to end.
- Useful as a study resource for system design and scalability concepts.

---

## What This Project Won't Do

- Migrate to a different backend framework (Quarkus, Micronaut, etc.).
- Replace JSP views with a React/Vue frontend as part of this roadmap.

The goal is to evolve and improve what's here — not rewrite from scratch.

---

## Phase 1 — Foundation First

**Timeline:** Current focus (weeks 0–8)
**Goal:** Make this reliable to run, easy to contribute to, and stable enough to build on.

### Bugs & Stability
- Resolve high-impact open bugs from existing issues. `[help wanted]`
- Standardize error handling across controllers and services. `[help wanted]`
- Clean up dead code and inconsistent naming. `[help wanted]`

### Developer Setup
- Docker Compose config for one-command local startup (app + MySQL). `[help wanted]`
- GitHub Actions CI — run `mvn clean verify` on every PR. `[help wanted]`
- Issue and PR templates under `.github/`. `[good first issue]`
- `CONTRIBUTING.md` covering branch naming, commits, and local setup. `[good first issue]`
- Checkstyle integration in build and CI. `[help wanted]`
- Separate config profiles for dev, test, and prod. `[help wanted]`

### Platform Upgrade
- Upgrade to Java 17 + Spring Boot 3.x. `[advanced]`
- Migrate `javax.*` to `jakarta.*`. `[help wanted]`
- Verify Hibernate, security, and plugin compatibility after migration. `[advanced]`

### Testing
- Unit tests for all service classes with JUnit 5 + Mockito. `[good first issue]`
- Controller tests using `@WebMvcTest`. `[help wanted]`
- JaCoCo coverage report + README badge. `[good first issue]`
- DAO-level tests using Testcontainers MySQL. `[advanced]`

### Phase 1 Done When:
- A new contributor can clone and run the app by following the README alone.
- Every PR triggers automated build and test checks.
- Core modules have baseline test coverage.
- Main branch stays green for 30 days straight.

---

## Phase 2 — Complete the E-Commerce Flow

**Timeline:** After Phase 1 stabilizes (weeks 8–16)
**Goal:** Build a real, end-to-end shopping experience — not just a skeleton.

### Cart & Checkout
- Full cart lifecycle: add, update, remove, clear. `[help wanted]`
- Checkout flow with order placement and confirmation page. `[advanced]`
- Order status transitions: created → paid → shipped → delivered / canceled. `[help wanted]`

### Architecture
- Global exception handler for controllers and services. `[help wanted]`
- Pagination + sorting for product and customer listings. `[good first issue]`
- Database migrations with Flyway. `[help wanted]`
- Structured logging with SLF4J and consistent log levels. `[help wanted]`

### Product Features
- Image upload (multipart) with local storage + cloud-ready abstraction. `[advanced]`
- Product search by name and category. `[good first issue]`
- Out-of-stock handling — disable add-to-cart when quantity is 0. `[good first issue]`

### Auth & User Enhancements
- Password reset via time-limited token. `[advanced]`
- Email verification on registration. `[advanced]`
- Remember-me login. `[help wanted]`
- Multiple shipping addresses per user. `[help wanted]`

### API Docs
- Swagger UI / OpenAPI 3 integration. `[good first issue]`

### Phase 2 Done When:
- Full purchase flow works from browsing to order creation.
- Errors and pagination are handled across major flows.
- DB migrations are version-controlled and repeatable.

---

## Phase 3 — Production Patterns

**Timeline:** After Phase 2 is feature-complete (weeks 16–28)
**Goal:** Introduce the patterns that separate hobby projects from production systems.

### Performance & Caching
- Add DB indexes and document query plans for hot paths. `[help wanted]`
- Redis caching for read-heavy endpoints. `[advanced]`
- Connection pool tuning + endpoint benchmarking. `[help wanted]`

### Concurrency Control
- Optimistic locking for inventory update conflicts. `[advanced]`
- Pessimistic locking demo with documented tradeoffs. `[advanced]`

### Search
- Elasticsearch for full-text product search. `[advanced]`
- SQL search fallback for local environments. `[help wanted]`

### Design Patterns
- Strategy pattern for payment options (COD, mock card, mock UPI). `[advanced]`
- Factory pattern for discounts and coupon logic. `[advanced]`

### Observability
- Spring Boot Actuator endpoints (health, metrics, info). `[good first issue]`
- Prometheus + Grafana via Docker Compose profile. `[advanced]`
- Logback JSON structured logging. `[help wanted]`

### Phase 3 Done When:
- At least one concurrency strategy is live in the inventory path.
- Search works in both DB-fallback and Elasticsearch modes.
- Metrics are visible and graphable.

---

## Phase 4 — Microservices & System Design

**Timeline:** Long-term (28+ weeks)
**Goal:** Show how to decompose this monolith — without breaking the monolith as a learning resource.

### Decomposition Guide
- Write a service boundary plan: user, product, order, notification. `[discussion]`
- Document monolith vs microservices tradeoffs with real examples. `[discussion]`

### Event-Driven Architecture
- Kafka-based order events with subscribers. `[advanced]`
- Demonstrate eventual consistency and retry patterns. `[advanced]`

### Phase 4 Done When:
- Architecture docs clearly show boundaries and communication patterns.
- At least one event-driven workflow is implemented and tested end to end.

---

## Ongoing Maintenance (All Phases)

This runs in parallel — doesn't wait for feature work.

### Automation
- Dependabot for `pom.xml` dependency updates. `[good first issue]`
- Stale bot for inactive issues/PRs. `[good first issue]`
- PR size labeler (S/M/L). `[good first issue]`

### Documentation
- `docs/adr/` for architecture decisions. `[good first issue]`
- `docs/architecture.md` with Mermaid component diagram. `[good first issue]`
- `SECURITY.md` with responsible disclosure info. `[good first issue]`
- Learning path guide: DAO → Service → Controller → View. `[good first issue]`

---

## Labels to Use

```
roadmap/phase-1     roadmap/phase-2     roadmap/phase-3     roadmap/phase-4
good first issue    help wanted         advanced            discussion
blocked             priority/high       priority/medium     priority/low
```

---

## Contribution Guide by Level

**New contributor**
→ Pick a `good first issue` from Phase 1. Open a draft PR early and ask questions.

**Regular contributor**
→ Take on `help wanted` items from the active phase. Tests, docs, and migration notes should be in the same PR.

**Maintainer**
→ Keep labels and phase board up to date. Reject feature PRs that skip tests or documentation.

---

## PR Checklist

Before a PR is ready to merge:
- [ ] CI passes (build + tests green)
- [ ] Tests cover the changed behavior
- [ ] Scope is focused — no mega PRs
- [ ] Docs updated if behavior or setup changed
- [ ] Rollback notes included for risky changes

---

## What to Work on Right Now

If you want to contribute today, these are the top 5 priorities:

1. Docker Compose local setup
2. GitHub Actions CI on pull requests
3. `CONTRIBUTING.md` + issue/PR templates
4. Baseline service and controller tests
5. Java 17 + Spring Boot 3 migration spike
