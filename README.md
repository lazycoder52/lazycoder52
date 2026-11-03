# Aditya

Software and applied-AI engineering student at IIT Kharagpur. I build tested, measured systems: real-time backends, LLM tooling with evaluation, and forecasting pipelines.

## Projects

- [BidStream](https://github.com/lazycoder52/bidstream): Real-time auction engine with pessimistic row locking (`SELECT ... FOR UPDATE`), atomic idempotency keys, BullMQ delayed jobs plus a SKIP LOCKED sweeper, and multi-instance WebSocket synchronization.
  - **Stack**: TypeScript, NestJS, Express, Socket.IO, PostgreSQL 16, Redis 7, BullMQ, Prisma, React 19, Docker
  - **Metric**: Sustained 515.2 req/s with 0 database invariant violations under a 500-VU bidding storm (measured on a shared 2-vCPU GitHub Actions runner).
- [Analytics Copilot](https://github.com/lazycoder52/analytics-copilot): Guarded natural-language-to-SQL assistant and offline-reproducible evaluation harness over Parquet demand planning aggregates.
  - **Stack**: Python, DuckDB, sqlglot, FastAPI, Pydantic, Wilson score interval evaluation harness
  - **Metric**: 28/40 (70%, 95% CI 55-82%) strict execution accuracy, Groq gpt-oss-120b; 11 of 12 misses were column-projection differences.
- [Fertilizer Recommendation Service](https://github.com/lazycoder52/fertilizer): Agronomic fertilizer recommendation service with a tuned Random Forest classifier, TreeSHAP local feature attribution, and Pydantic v2 validation contracts.
  - **Stack**: Python, Scikit-learn, Random Forest, TreeSHAP, Optuna, Pydantic v2, Flask, Docker
  - **Metric**: 98.71% Top-1 accuracy and 0.9431 Macro-F1 on a 620-sample holdout (synthetic benchmark dataset with generation artifacts, not validated on real farm data).
- [Grocery Demand Planner](https://github.com/lazycoder52/grocery-demand-planner): End-to-end grocery demand forecasting and periodic (R,S) replenishment simulation across 54 stores and 33 product families on public Corporación Favorita data.
  - **Stack**: Python, LightGBM, DuckDB, Pandas, NumPy, Streamlit
  - **Metric**: Reduces walk-forward forecast error from 16.33% to 13.49% WAPE across a 5-fold rolling-origin backtest (public Kaggle Corporación Favorita historical data).
- [Collaborative Whiteboard](https://github.com/lazycoder52/collaborative-whiteboard): Real-time collaborative whiteboard extending an AlgoZenith canvas tutorial base with an append-only delta streaming protocol, debounced persistence, and per-user undo/redo.
  - **Stack**: React 18, HTML5 Canvas, Rough.js, perfect-freehand, Node.js, Express, Socket.IO, MongoDB, Zod
  - **Metric**: 97.38% wire data reduction and 66.00% network event reduction compared to monolithic full-canvas broadcasts (synthetic 200-point stroke benchmark).

## Skills and Tools

- **Languages & Runtimes**: TypeScript, JavaScript (Node.js), Python, SQL
- **Frameworks & Libraries**: NestJS, Express, FastAPI, Flask, React, Socket.IO, BullMQ
- **Data & Persistence**: PostgreSQL, Redis, DuckDB, MongoDB, Prisma ORM, Pandas, NumPy
- **Machine Learning & AI**: LightGBM, Scikit-learn, TreeSHAP, Optuna, sqlglot
- **Testing & Infrastructure**: Docker, Vitest, Jest, Pytest, Playwright, k6, GitHub Actions CI, Zod, Pydantic v2
