# André Martinelli

I build production software by directing AI coding agents, and I hold them to an
engineering process I designed myself.

Based in Dublin. Italian and Brazilian citizen. Native Portuguese, working
English.

---

### Nest Reef — a marine aquarium platform, live at [nestreef.com](https://nestreef.com)

Designed, built and operated end to end. The repository is private, but here is
what is in it, measured rather than estimated:

| | |
|---|---|
| API routes | 73 |
| Screens | 40 |
| Automated tests | 363 — 295 backend integration, 55 end-to-end in headless Chromium, 13 Python |
| Database migrations | 49, all additive |
| Merged pull requests | 273 |
| Third-party runtime dependencies | 0 |

Cloudflare Workers · Cloudflare D1 · vanilla JavaScript PWA · Tailwind · esbuild
· GitHub Actions · Playwright · Capacitor (iOS) · Stripe · Apple IAP · ESP-IDF (C)

The whole system — interface and API — is served from a **single Cloudflare
Worker on one origin**, so there is no CORS layer and no second service to
operate. Continuous delivery runs the full suite on every merge, deploys only if
it is green, then verifies the live health endpoint returned 200. Schema
migrations are deliberately kept **out** of that pipeline: they touch real user
data, so they run as an explicit human-approved step.

I am happy to walk through any part of it, or give read access on request.

---

### [job-collector](https://github.com/martinellibrs93/job-collector) — public

A daily job collector and ranker. Reads about 5,000 listings from 11 public APIs
in ten seconds, scores each against a configurable profile, and returns a short
list with the reasoning attached. Zero runtime dependencies, 81 tests.

The tests were **verified by mutation** — critical paths broken on purpose to
check the suite catches it. One mutation revealed a test that passed for the
wrong reason; it was rewritten. That story is in
[`docs/DECISIONS.md`](https://github.com/martinellibrs93/job-collector/blob/main/docs/DECISIONS.md),
along with the reasoning behind every other design choice.

---

### How I work

- **I direct, review and own.** Agents write most of the code; the architecture, the review, the release decision and the consequences are mine.
- **Tests come before refactors**, and every fix is proven by breaking it first — I confirm the new test fails without the fix before shipping the fix.
- **Decisions are written down with their reasoning**, in the repository, so the "why" outlives the conversation that produced it.
- **I can name my systems' weaknesses.** Being able to say precisely where something is weak is, I think, the point.

---

Before software, twelve years in specialty coffee — Brazilian Latte Art Champion
(ACBB, 2014) and 9th at the World Latte Art Championship in Melbourne. I moved
into software because I kept running into things I wanted to exist and could not
find. So I started building them.
