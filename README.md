# Henrique Coelho

Backend engineer and published researcher. Building production systems and doing applied research in computer vision and ML since age 15.

Currently working full-time at **BioWatts** (Cascavel, BR) designing a CPQ system for photovoltaic project dimensioning — from domain architecture to event-driven infrastructure.

---

## Published Research

Three papers published at SBC-indexed conferences between 2023 and 2025, with a consistent research thread: assistive eye-control technology for people with severe motor disabilities.

---

### [Domótica Assistiva com Controle Ocular para Inclusão de Deficientes Tetraplégicos](https://doi.org/10.5753/latinoware.2023.236535)
**Latinoware 2023 — XX Congresso Latino-Americano de Software Livre e Tecnologias Abertas (SBC)**
🏆 **Best Short Paper Award**
*Published October 2023 — age 15*

Eye-blink controlled home automation system for people with quadriplegia. EAR (Eye Aspect Ratio) computed via Dlib 68-point facial landmark model, thresholded to detect voluntary blinks and trigger IoT device control. Modular Observer Pattern architecture for extensibility. Low-cost solution targeting autonomy in daily life tasks.

DOI: `10.5753/latinoware.2023.236535` · Pages 170–173

---

### [Detecção de Piscadas Baseada em Aprendizado de Máquina para Controle de Dispositivos por Pessoas com Deficiência Motora Severa](https://sol.sbc.org.br/index.php/latinoware/article/view/40979)
**Latinoware 2025 — XXI Congresso Latino-Americano (SBC)**
*Published 2025 — age 17*

Evolution of the 2023 system: replaced fixed EAR threshold with ML classifiers trained on physiological data from 7 volunteers (~100k labeled frames at 15fps). Compared Decision Tree, KNN, Logistic Regression, and Random Forest across two feature extraction strategies (raw EAR vs. 19 MediaPipe facial keypoints). Leave-One-Out cross-validation for generalization across individuals. Random Forest achieved **F1: 0.998** vs. fixed-threshold baseline **F1: 0.919**.

---

### Ciência de Dados Aplicada: Um Estudo Guiado por Desafios do Kaggle
**SCIENTIF VI — IFPR, 2025**

Applied OSEMN lifecycle across two supervised learning tasks:
- Bank churn prediction (classification): CatBoost, Grid Search, AUC-ROC **88.4% on Kaggle leaderboard** — 2% below the 2-year-old top solution using advanced ensemble methods
- House price regression: Random Forest, **R²: 0.8875**, ranked 2,185/5,280 on Kaggle with a conservative numeric-only baseline

---

## What I'm building at BioWatts

**CPQ System — Solar Energy Dimensioning Platform**

A configurable quoting and dimensioning engine for photovoltaic projects, built from the ground up with end-to-end ownership.

- **Django + PostgreSQL** — domain modeling, ORM, migrations, configurable business rule engine
- **RabbitMQ + Celery** — async task processing, Celery Beat scheduled jobs, worker fleet monitored with Flower
- **Outbox Pattern** — transactional event publishing with at-least-once delivery guarantees
- **Docker + Nginx + TLS** — containerized deployment, reverse proxy, production infrastructure
- **Third-party integrations** — reverse engineering undocumented distributor REST endpoints, web scraping pipelines, automated query automation against internal APIs
- **Document generation** — transforming dimensioner output into formal proposal and budget documents
- **CRM integration** *(in progress)* — decoupled via event contracts

Key engineering challenges: isolating volatile third-party contracts from the core domain model; building a configurable rules engine adjustable by non-technical users; ensuring delivery guarantees across the async pipeline.

---

## Stack

```
Languages     Python, SQL
Backend       Django, Django REST Framework, Celery, Celery Beat
Messaging     RabbitMQ, Outbox Pattern
Database      PostgreSQL
DevOps        Docker, Docker Compose, Nginx, TLS, GitHub Actions
Testing       pytest, Django test client
ML / CV       Scikit-learn, OpenCV, MediaPipe, Dlib
Data          Pandas, NumPy, Seaborn, Matplotlib
Tooling       Flower, Poetry, Git
Other         API reverse engineering, web scraping, PDF generation
```

---

## Other

**OBI 2023** — 2× finalist, Brazilian Informatics Olympiad (programming track)

---

## Currently deepening

- RabbitMQ internals — AMQP delivery guarantees, DLQ strategies, consumer prefetch tuning
- Distributed systems fundamentals — consistency models, failure modes, CAP trade-offs
- System design patterns — CQRS, Saga, circuit breaker

---

## Contact

- LinkedIn: [linkedin.com/in/coelhovsk](https://linkedin.com/in/coelhovsk)
- Email: henriquecoelhodossantos2007@gmail.com
- Location: Cascavel, Paraná — Brazil
