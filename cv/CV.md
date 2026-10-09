# Dean Meiring

*Software Developer building production ML systems — seeking Machine Learning / AI Engineering roles*

meiringdean2409@gmail.com | Somerset West, Cape Town, South Africa | [linkedin.com/in/deanmeiring](https://linkedin.com/in/deanmeiring) | [github.com/DeanMeiring](https://github.com/DeanMeiring)

> Phone number omitted from this public text mirror — see the PDF version if you have it, or use the email above.

## Professional Summary

Final-year Computer Science student (Belgium Campus, BI specialisation) who ships working ML systems, not just coursework: a real-time crypto arbitrage and price-prediction platform running live on production infrastructure, with hands-on experience integrating exchange and LLM/vision APIs. Comfortable across Python, SQL, and JavaScript/TypeScript, with hands-on experience building, deploying, and debugging live ML pipelines. Currently in a BI/Application Specialist role applying automation and data skills day-to-day, while actively moving toward a machine learning or data engineering role where I own systems end-to-end rather than support them.

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
- Achieved meaningfully better-than-chance classification performance — a clear contrast to the chance-level (AUC ≈ 0.50) result found in the crypto price-direction model above, and a useful data point on which feature domains actually carry predictive signal.
- Identified and closed a genuine research gap by combining region-specific pest biology, chill-portion phenology modelling, and ensemble ML — sourced and negotiated data access with international research bodies and industry contacts.
- Code: [github.com/DeanMeiring/Dean-Projects](https://github.com/DeanMeiring/Dean-Projects)

## Technical Skills

- **Machine Learning & Data:** pandas, NumPy, scikit-learn, XGBoost, feature engineering, model evaluation (AUC, accuracy, train/test methodology), PyTorch, LightGBM, VQ-VAE, residual quantization, graph neural networks, bootstrap confidence intervals, pre-registered evaluation
- **Languages:** Python, SQL, JavaScript, TypeScript, Java, shell/scripting
- **APIs & Integration:** REST & WebSocket APIs (Binance, Crypto.com), Google Gemini (LLM/vision), Telegram Bot API
- **Backend & Infra:** FastAPI, asyncio, Git, Railway deployment, Agile methodologies, UAT/testing
- **Databases:** PostgreSQL, TimescaleDB, SQLite — relational and time-series data design
- **BI & Analytics:** Power BI, Tableau, Microsoft Excel — dashboards and reporting pipelines

## Experience

### Application Specialist (AIT Intern) | Online Intelligence
*Jan 2026 – Present*

- Write SQL queries and custom automation scripts to streamline raw data workflows on the CiiMS platform for the Thompsons Security Group account, with secondary support for Clicks and EBS Security.
- Own end-to-end User Acceptance Testing (UAT) for platform releases, translating client requirements into structured test coverage.
- Work directly with the Regional Manager on platform configuration and client-facing reporting, building fluency in enterprise BI tooling (Business Link, RAPs).

### Co-Founder & Data Analyst | MEIDEAN Trading (Family Business)
*Mar 2025 – Jan 2026*

- Built custom software to automate operations and streamline business processes, beyond core sales activity.
- Delivered part-time data analysis projects for external clients, including a completed engagement with the Lipstar Group and ongoing work for Lancewood.
- Stepped back from day-to-day involvement in January 2026 to begin the AIT internship.

### Software Engineering Intern (Job Shadowing) | Pragma
*Dec 2024*

- Shadowed professionals on live industry software projects, gaining hands-on exposure to real-world development practices.

### IT Support (Part-Time) | Small Start-Up
*2022*

- Provided troubleshooting and technical support in a fast-paced, dynamic environment.

## Education

**Belgium Campus iTversity (NQF Level 8) — BSc Computer Science**
*Expected 2026*

- Specialisation: Business Intelligence (BI)
- Relevant coursework: Data Structures, Database Management, Data Analytics, Software Engineering

## Leadership & Extracurricular

- **Esports Tournament Organiser, Belgium Campus** — Structure and run inter-university tournaments (Rocket League, Valorant, EA FC) across South African campuses, including bracket design, sponsorship strategy, and player analytics.
- **Youth Ministry Leader, Shofar Stellenbosch** (Jan 2024 – Present) — Lead a youth group; developed structured communication and mentorship skills.
- **Tanzania Mission Trip Co-Leader** (June 2024) — Coordinated a two-week international outreach team.

## Achievements & Interests

- Two Oceans Half Marathon Finisher (2023, 2024); Warrior Race (Black Level) Finisher; competitive cyclist
- Self-funded tertiary education through part-time hospitality work (Fancy Franks; Lourensford Wine Estate, 2022–2024), including leading a 22-person team at a high-profile event.
