# Dean Meiring

*Data & BI Developer · SQL · Python · Automation · Machine Learning*

meiringdean2409@gmail.com | Somerset West, Cape Town, South Africa | [linkedin.com/in/deanmeiring](https://linkedin.com/in/deanmeiring) | [github.com/DeanMeiring](https://github.com/DeanMeiring)

> Phone number omitted from this public text mirror — see the PDF version if you have it, or use the email above.

## Professional Summary

Final-year Bachelor of Computing student (Data Science, 65.6% weighted average) who builds and runs real data systems, not just coursework. I work daily in SQL, Python and BI tooling as an Application Specialist, and have deployed a live ML trading-signal platform and run a 30+ experiment ML research project. I enjoy turning messy data into decisions, I'm passionate about fintech, and I'm looking for a role where I can own problems end to end. Open to relocating to the UK, UAE, Poland, Portugal or Spain.

## Key Projects

### Learned Feature Vocabularies for ML (VQ-VAE) — Research in Progress

- Testing whether short discrete "words" from a shared, frozen vocabulary can give ML models reusable context instead of hand-engineered features. Solo, ongoing project: 30+ pre-registered experiments (PyTorch, LightGBM, scikit-learn) on Telco churn, Fashion-MNIST, PEMS-BAY road traffic (325 sensors) and Telecom Italia (10,000 grid squares).
- First positive real-data result: 16 learned "profile words" per Milan grid square, built once from two weeks of raw history and reused across 4 forecasting tasks, improved a model that already had the raw data (next-day error −6%, next-hour −0.9%, all four significant). A simple hand-built feature (each square's typical value for that hour) still did better, by 3–8%, which sets the next test.
- Diagnosed why earlier versions failed: words built from the model's own 24-hour input added nothing; an audit traced the loss to the encoder's squeeze rather than the vocabulary; and equal-bytes controls showed exact recent values beat learned summaries on short-range forecasting. Stabilised residual-quantization training (a health gate, then removing a dead-code "revive" step found to trigger the breakdown).
- Compressed images to 8–49 bytes, up to 10.8x smaller than zipped pixels; the learned words beat raw pixels by about 4 points at 50 labels, and self-contained set words reached 70% word purity (up from 17% for grid words).
- Fixed each pass/fail bar in git before running and judged results by 95% confidence intervals (block-resampled for spatial data). Reported negative results as they came, including a clear fail of the project's own telecom bar and a graph-network traffic experiment that gained 3.5% from neighbours against a 5% bar.
- Built a versioned, hash-verified SQLite feature library (frozen dictionaries, messages, per-word "cards"); a class is recovered from cards alone at 76.7% accuracy. Tested Claude as a reader of the vocabulary (78.6%, all answers grounded) and found its answers came from the cards, so parked a custom reader.
- Found that retraining on a second machine gives a slightly different dictionary (60.2% vs 61.3% at 50 labels), so a dictionary is only reusable as a copied, hashed file. Working under a self-imposed 30% compute cap on CPU-only laptops.
- Code: [github.com/DeanMeiring/features-abstractions-meaning](https://github.com/DeanMeiring/features-abstractions-meaning)

### Real-Time Crypto Arbitrage & ML Price-Prediction Platform

- Designed and deployed a live trading-signal system combining triangular and cross-exchange arbitrage detection (Binance and Crypto.com APIs, WebSocket + REST) with per-asset XGBoost classifiers predicting short-term price direction, retrained daily on a rolling window of live market data.
- Actively iterating on an XGBoost price-direction model across 8 assets (130K+ candles each); current baseline model performs at chance (AUC ≈ 0.50) after rigorous cross-validation — investigating alternative feature sets (order-book/on-chain signals) and prediction horizons to find exploitable signal.
- Engineered a multi-feature model (momentum, volatility, cyclical time-of-day encoding, volume, cross-asset lag signals) and diagnosed and fixed subtle production bugs — including a silent data-mislabeling defect in target generation and a timestamp-alignment bug that broke live inference for most tracked assets — catching each with targeted before/after testing.
- Built an automated paper-trading engine with stop-loss/take-profit risk controls and a self-monitoring dashboard comparing predictions against outcomes across the tracked asset universe, separating gross performance from fee-adjusted net results.
- Integrated a Telegram bot for real-time alerts and command-driven reporting, alongside a live analytics dashboard (FastAPI, PostgreSQL, Chart.js).
- Deployed and continuously operate the system on Railway, managing scheduled retraining, database schema migrations, and safe redeploys of a stateful, always-on service.

### Mediterranean Fruit Fly Outbreak Prediction — Multi-Region ML Pipeline

- Built and evaluated XGBoost classifiers predicting Mediterranean fruit fly outbreak risk across two regions — the Western Cape (South Africa) and California — each calibrated to local climate, trap-catch, and crop-cycle data.
- Feature sets included cumulative degree-days, rainfall spikes, historical trap counts, host-crop harvest schedules, and proximity to known infestation hot spots (Western Cape), plus microclimate and quarantine-boundary features (California).
- Sourced and negotiated data access with international research bodies and industry contacts.
- Code: [github.com/DeanMeiring/Dean-Projects](https://github.com/DeanMeiring/Dean-Projects)

## Technical Skills

- **Machine Learning & Data:** pandas, NumPy, scikit-learn, XGBoost, feature engineering, model evaluation (AUC, accuracy, train/test methodology), PyTorch, LightGBM, VQ-VAE, residual quantization, graph neural networks, bootstrap confidence intervals, pre-registered evaluation
- **Languages:** Python, SQL, JavaScript, TypeScript, Java, shell/scripting
- **APIs & Integration:** REST & WebSocket APIs (Binance, Crypto.com), Google Gemini (LLM/vision), Telegram Bot API
- **Backend & Infra:** FastAPI, asyncio, REST & WebSocket APIs, Git, Railway deployment
- **Ways of working:** Agile, User Acceptance Testing, requirements gathering
- **Databases:** PostgreSQL, TimescaleDB, SQLite — relational and time-series data design
- **BI & Analytics:** Power BI, Tableau, Microsoft Excel — dashboards and reporting pipelines

## Experience

### Application Specialist (AIT Intern) | Online Intelligence
*Jan 2026 – Present*

- Write SQL queries and automation scripts that replace manual data handling on the CiiMS platform for Thompsons Security Group, with support for Clicks and EBS Security.
- Own end-to-end User Acceptance Testing for platform releases, turning client requirements into structured test coverage.
- Work with the Regional Manager on platform configuration and client reporting in enterprise BI tooling.

### Co-Founder & Data Analyst | MEIDEAN Trading (Family Business)
*Mar 2025 – Dec 2025*

- Built custom software that automated day-to-day operations and business processes.
- Delivered data analysis projects for external clients, including the Lipstar Group and Lancewood.

### Founder & Software Developer | LPSolutions
*Oct 2023 – Dec 2024*

- Ran my own software business, building custom applications for clients end to end, from requirements to delivery.
- Built an application for a construction company client.

### Software Engineering Intern (Job Shadowing) | Pragma
*Dec 2024*

- Shadowed professionals on live industry software projects, gaining hands-on exposure to real-world development practices.

### IT Support (Part-Time) | Small Start-Up
*2022*

- Provided troubleshooting and technical support in a fast-paced, dynamic environment.

## Education

**Belgium Campus iTversity — Bachelor of Computing (NQF Level 8), Data Science specialisation**
*Expected 2026*

- 4-year degree: 3 academic years plus a workplace year (internship and dissertation, in progress)
- Academic years: weighted average **65.6%** · 38 subjects passed, none failed
- Top results: Business Intelligence 84% · Innovation Management 82% · Project Management 80% · Capstone Project 76% · Database Administration 75%
- Relevant modules: Machine Learning, Statistics (3 years), Data Warehousing, Database Development, Linear Programming, Programming

## Leadership & Extracurricular

- **Esports Tournament Organiser, Belgium Campus** — Structure and run inter-university tournaments (Rocket League, Valorant, EA FC) across South African campuses, including bracket design, sponsorship strategy, and player analytics.
- **Youth Ministry Leader, Shofar Stellenbosch** (Jan 2024 – Present) — Lead a youth group; developed structured communication and mentorship skills.
- **Tanzania Mission Trip Co-Leader** (June 2024) — Coordinated a two-week international outreach team.

## Achievements & Interests

- Two Oceans Half Marathon Finisher (2023, 2024); Warrior Race (Black Level) Finisher; competitive cyclist
- Self-funded tertiary education through part-time hospitality work (Fancy Franks; Lourensford Wine Estate, 2022–2024), including leading a 22-person team at a high-profile event.
