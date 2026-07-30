# Pranav Auti

Hoboken, NJ · USA — Graduate Assistant at Stevens Institute of Technology, previously at Tychee and EquityFx.

I write software for things where being wrong is expensive — trade reconciliation, payment rails, clinical risk scores. Right now I'm on the new-grad/internship interview loop, which is the actual reason [AppTracker](https://job-tracker-rho-five.vercel.app) below exists: I got tired of losing track of my own applications, so I built a tracker with a Kanban pipeline and gamified it hard enough that I keep opening it.

[pranavauti2003@gmail.com](mailto:pranavauti2003@gmail.com) · [linkedin.com/in/pranav-auti](https://www.linkedin.com/in/pranav-auti)

---

### building in the open right now

**[Trade Settlement & Reconciliation Engine](https://github.com/Pranav2112/trade-reconciliation-engine)** — two independent trade feeds (an internal book of record and a counterparty feed) get reconciled; anything that doesn't match becomes a "break," and an ML scorer ranks each break by anomaly severity. Phase 1 of 5, tracked in the repo itself:

- [x] Phase 1 — Postgres schema + Spring Boot matching logic against sample data, unit tests
- [ ] Phase 2 — Kafka (KRaft) + Docker Compose, Python feed generator, idempotent consumer
- [ ] Phase 3 — REST API for breaks + React dashboard + JWT auth
- [ ] Phase 4 — anomaly scoring service, severity surfaced in the UI
- [ ] Phase 5 — CI across every service, architecture diagram, seed script, demo walkthrough

**[Concurrent Resource Booking Platform](https://github.com/Pranav2112/Concurrent-Resource-Booking-Platform)** — the whole point of this one is a single bug: two people click "book" on the same slot in the same millisecond, and a naive read-then-write flow lets both win. Fixed it with row-level pessimistic locking (`SELECT ... FOR UPDATE`) inside a transaction boundary, then load-tested it — 20 simultaneous booking requests, 1 success, 0 conflicts, every run.

---

### shipped

**[AppTracker](https://job-tracker-rho-five.vercel.app)** — job/internship tracker with a 12-stage Kanban board, a scraper that auto-fills company/role/salary from a pasted Greenhouse, Lever, or Ashby URL with no paid API behind it, and an XP/streak/achievement system that exists purely so I don't ghost my own job search. React 18, TypeScript, Supabase, Vite.

**[FlashBet Protocol](https://github.com/Pranav2112/flashbet-monad)** — built in ~24 hours at Monad NYC. Live on-chain YES/NO prediction markets on real sports moments; since there's no live feed to hook into at a hackathon, a scripted Brazil–Argentina match generates real events (penalties, corners) and people bet real testnet MON on them through MetaMask, then claim against contracts actually deployed on [Monad testnet](https://testnet.monadexplorer.com). Solidity, Next.js 14, wagmi v2, a Node.js oracle running the match.

**[AvaxPay](https://avax-pay.vercel.app)** — a Stripe-shaped payment processor for Avalanche: deeplink checkout, subscriptions, mock USDC/USDT settlement, contracts live on Fuji testnet. [Demo video here](https://youtu.be/SzBH74kJ_Pw). Solidity, Next.js.

**[FinSight AI](https://github.com/Pranav2112/finsight-ai)** — type a ticker, get a real research report back: a year of OHLCV via `yfinance`, volatility and max-drawdown risk metrics, MA20/50/200 + RSI14, and a rule-based bull/neutral/bear call with reasons attached. No LLM in the loop, no invented numbers. Next.js, FastAPI, pandas/NumPy.

**[SmartFinance](https://github.com/Pranav2112/smartfinance)** — personal finance tracker, run as an actual Scrum project over 4 sprints for a grad Agile Methods course: budget thresholds with live alerts, savings goals, 6-month spend trends, an admin view across users. React, Node/Express, PostgreSQL.

**[MaternaSense](https://github.com/Pranav2112/maternasense)** — clinical decision-support tool for early preeclampsia risk screening, built around evidence-based risk stratification for maternal care planning. React, Python, scikit-learn.

---

### stack, roughly in order of how often I reach for it

`TypeScript` `Python` `React` `Next.js` `FastAPI` `Java / Spring Boot` `PostgreSQL` `Supabase` `Solidity` `Docker` `Kafka` `AWS`

---

<img src="https://github-readme-stats.vercel.app/api?username=Pranav2112&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" height="165" /> <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Pranav2112&layout=compact&theme=tokyonight&hide_border=true" height="165" />

If you're hiring for SWE / ML / fintech, or want to talk about any of the above — [email me](mailto:pranavauti2003@gmail.com).
