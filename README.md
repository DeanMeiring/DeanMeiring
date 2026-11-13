# Dean Meiring

Data & BI Developer · SQL · Python · Automation · Machine Learning — working toward data engineering and ML/AI engineering roles.

📍 Somerset West, Cape Town, South Africa
📧 meiringdean2409@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/deanmeiring) · [GitHub](https://github.com/DeanMeiring)

Full CV: [`cv/Dean_Meiring_CV.pdf`](cv/Dean_Meiring_CV.pdf) · text version: [`cv/CV.md`](cv/CV.md)

## About

Final-year Bachelor of Computing student (Data Science, 65.6% weighted average) who builds and runs real data systems, not just coursework. I work daily in SQL, Python and BI tooling as an Application Specialist, and have deployed a live ML trading-signal platform and run a 30+ experiment ML research project. I enjoy turning messy data into decisions, I'm passionate about fintech, and I'm looking for a role where I can own problems end to end.

## Key Projects

### Learned Feature Vocabularies for ML (VQ-VAE) — Research in Progress
- Solo, ongoing research: can short discrete "words" from a shared, frozen vocabulary give ML models reusable context instead of hand-engineered features? 30+ pre-registered experiments (PyTorch, LightGBM, scikit-learn) on Telco churn, Fashion-MNIST, PEMS-BAY road traffic and Telecom Italia (10,000 Milan grid squares).
- First positive real-data result: 16 learned "profile words" per grid square, built once from two weeks of raw history and reused across 4 forecasting tasks, improved a model that already had the raw data (next-day error −6%, all four tasks significant). A simple hand-built feature still did better, by 3–8%.
- Diagnosed why earlier versions failed: an audit traced the loss to the encoder rather than the vocabulary, and equal-bytes controls showed exact recent values beat learned summaries on short-range forecasting.
- Every pass/fail bar committed to git before running and judged by 95% confidence intervals (block-resampled for spatial data); negative results reported as they came.
- Images compressed to 8–49 bytes, up to 10.8x smaller than zipped pixels; learned words beat raw pixels by about 4 points at 50 labels.
- Hash-verified SQLite feature library, and Claude tested as a reader of the vocabulary (78.6%, answers grounded in word cards); its answers came from the cards, so a custom reader was parked.
- Code: [github.com/DeanMeiring/features-abstractions-meaning](https://github.com/DeanMeiring/features-abstractions-meaning)

### Real-Time Crypto Arbitrage & ML Price-Prediction Platform
- Live trading-signal system combining triangular and cross-exchange arbitrage detection (Binance and Crypto.com APIs, WebSocket + REST) with per-asset XGBoost classifiers predicting short-term price direction, retrained daily on a rolling window of live market data.
- Iterating on an XGBoost price-direction model across 8 assets (130K+ candles each); investigating alternative feature sets and prediction horizons after a chance-level baseline.
- Automated paper-trading engine with stop-loss/take-profit risk controls and a self-monitoring dashboard comparing predictions against outcomes.
- Telegram bot for real-time alerts and command-driven reporting, plus a live analytics dashboard (FastAPI, PostgreSQL, Chart.js).
- Deployed and continuously operated on Railway, including scheduled retraining, schema migrations, and safe redeploys of a stateful, always-on service.

### Mediterranean Fruit Fly Outbreak Prediction — Multi-Region ML Pipeline
- XGBoost classifiers predicting Mediterranean fruit fly outbreak risk across the Western Cape (South Africa) and California, each calibrated to local climate, trap-catch, and crop-cycle data.
- Feature sets: cumulative degree-days, rainfall spikes, historical trap counts, host-crop harvest schedules, microclimate and quarantine-boundary features.
- Sourced and negotiated data access with international research bodies and industry contacts.
- Code: [github.com/DeanMeiring/Dean-Projects](https://github.com/DeanMeiring/Dean-Projects)

## Technical Skills

- **Machine Learning & Data:** pandas, NumPy, scikit-learn, XGBoost, LightGBM, PyTorch, feature engineering, model evaluation, confidence intervals
- **Languages:** Python, SQL, JavaScript, TypeScript, Java, shell/scripting
- **APIs & Integration:** REST & WebSocket APIs (Binance, Crypto.com), Google Gemini (LLM/vision), Telegram Bot API
- **Backend & Infra:** FastAPI, asyncio, Git, Railway deployment
- **Ways of working:** Agile, User Acceptance Testing, requirements gathering
- **Databases:** PostgreSQL, TimescaleDB, SQLite
- **BI & Analytics:** Power BI, Tableau, Microsoft Excel

## Experience

- **Application Specialist (AIT Intern)**, Online Intelligence — *Jan 2026 – Present*
- **Co-Founder & Data Analyst**, MEIDEAN Trading (Family Business) — *Mar 2025 – Dec 2025*
- **Founder & Software Developer**, LPSolutions — *Oct 2023 – Dec 2024*
- **Software Engineering Intern (Job Shadowing)**, Pragma — *Dec 2024*
- **IT Support (Part-Time)**, Small Start-Up — *2022*

## Education

**Bachelor of Computing (NQF Level 8), Data Science specialisation**, Belgium Campus iTversity — *Expected 2026*

- 4-year degree: 3 academic years plus a workplace year (internship and dissertation, in progress)
- Academic years: weighted average **65.6%** · 38 subjects passed, none failed
- Top results: Business Intelligence 84% · Innovation Management 82% · Project Management 80% · Capstone Project 76% · Database Administration 75%

## Leadership & Extracurricular

- Esports Tournament Organiser, Belgium Campus
- Youth Ministry Leader, Shofar Stellenbosch (Jan 2024 – Present)
- Tanzania Mission Trip Co-Leader (June 2024)

## Achievements & Interests

- Two Oceans Half Marathon Finisher (2023, 2024); Warrior Race (Black Level) Finisher; competitive cyclist
- Self-funded tertiary education through part-time hospitality work, including leading a 22-person team at a high-profile event
