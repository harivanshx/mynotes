

- Real-time prediction API
- Ensemble of XGBoost + LightGBM (weighted average)
- SHAP explanations returned with every prediction
- FastAPI backend
- React dashboard
- Dockerized
- Deployed on AWS EC2
- Focus on reducing false negatives (recall optimization)


churn-project/
├── data/
├── notebooks/                  # exploration
├── src/
│   ├── preprocessing/
│   ├── models/
│   ├── api/                    # FastAPI
│   └── shap_explainer.py
├── dashboard/                  # React app
├── docker/
│   ├── api.Dockerfile
│   └── nginx.Dockerfile
├── scripts/                    # training pipeline
├── tests/
├── requirements.txt
├── train.py
├── docker-compose.yml
└── README.md




### 6-Week Step-by-Step Plan

#### Week 1 – Data & Baseline Model

Goal: Get a working model with good recall

|Day|Task|
|---|---|
|1-2|Get dataset (recommended public datasets below) → Telco Customer Churn (Kaggle) → IBM Watson Telco Churn (very common) → Bank Customer Churn (Kaggle)|
|3-4|Exploratory Data Analysis + feature engineering (tenure bins, total charges, service counts, etc.)|
|5-6|Build baseline XGBoost with class weights / scale_pos_weight to reduce false negatives|
|7|Simple LightGBM model → weighted ensemble (e.g., 0.6 XGBoost + 0.4 LightGBM) that maximizes recall @ precision threshold|

Deliverable: Notebook with ~80–85% recall and ensemble beating single models

#### Week 2 – Advanced Modeling + SHAP

Goal: Final model + explanations

|Day|Task|
|---|---|
|1-2|Hyperparameter tuning (Optuna or Hyperopt) with objective = recall|
|3|Train final ensemble (save both models + weights)|
|4-5|Train SHAP explainer → Use shap.TreeExplainer for both models → Pre-compute background dataset (100–500 samples) → Create a function that returns weighted SHAP values|
|6-7|Build prediction function that returns: { "churn_probability": 0.78, "prediction": "Churn", "shap_values": [...], "shap_expected_value": 0.12 }|

Deliverable: model/final_ensemble.pkl + shap_explainer.py working locally

#### Week 3 – FastAPI Backend + Real-time Inference

Goal: Production API

|Day|Task|
|---|---|
|1-2|Set up FastAPI project (src/api/main.py)|
|3|Create /predict endpoint that: → Validates input with Pydantic → Preprocesses → Loads models & explainer → Returns prediction + SHAP (base64 plot optional)|
|4|Add health check, versioning, logging|
|5|Write unit tests (pytest) for preprocessing & prediction|
|6-7|Dockerize the API ```docker|

Test locally with:

Bash

```
uvicorn src.api.main:app --reload
curl -X POST with sample JSON → get SHAP JSON back
```

#### Week 4 – React Dashboard

Goal: Beautiful real-time dashboard

| Day | Task                                                                                                                                                                                                    |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Create React app (create-react-app or Vite)                                                                                                                                                             |
| 2-3 | Customer lookup page: enter customer ID → call FastAPI → show: • Churn probability gauge • Prediction tag (Churn / No Churn) • SHAP force plot or waterfall (use react-shap or generate PNG on backend) |
| 4   | Dashboard with top 10 high-risk customers (mock or real)                                                                                                                                                |
| 5   | Add global SHAP summary (bar plot of feature importance)                                                                                                                                                |
| 6-7 | Make it responsive + dark mode (optional but looks pro)                                                                                                                                                 |

You can return SHAP plot as base64 PNG from FastAPI or use JSON + shap.plots in JS.

#### Week 5 – Docker Compose + Full Local Deployment

Goal: Run everything locally with one command

Create docker-compose.yml:

YAML

```
version: '3.8'
services:
  api:
    build: ./docker
    ports:
      - "8000:80"
    volumes:
      - ./model:/app/model
  dashboard:
    build: ./dashboard
    ports:
      - "3000:80"
    environment:
      - REACT_APP_API_URL=http://localhost:8000
```

Now docker-compose up --build runs everything.

#### Week 6 – AWS EC2 Deployment + Polish

|Day|Task|
|---|---|
|1|Launch EC2 (t3.medium or t3.large recommended) – Ubuntu 22.04|
|2|Install Docker + Docker Compose|
|3|Copy code + models via git or scp|
|4|Run docker-compose in production mode (with nginx reverse proxy optional)|
|5|Set up security group: ports 80, 443, 22|
|6|Add free SSL with Let’s Encrypt (certbot) or use AWS ACM + load balancer (optional)|
|7|Monitoring: add simple Prometheus + Grafana container (optional) Write final README + record 2-min demo video|

### Final Bonus Touches (if you have time)

- Add Redis cache for repeated customer lookups
- Batch prediction endpoint
- Model drift detection script (runs weekly)
- Send Slack/Email alert when high-value customer > 70% churn prob

### Recommended Public Dataset (quick start)

[https://www.kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (Already clean, perfect size ~7k rows)

### Summary – You will have at the end of 6 weeks:

- A real-time churn API reducing false negatives by ~25–30%
- Beautiful SHAP explanations in the response
- Professional React dashboard
- Fully dockerized & deployed on AWS EC2
- Something 100% portfolio-worthy (exactly what you wrote in your bullet points)### 6-Week Step-by-Step Plan

#### Week 1 – Data & Baseline Model

Goal: Get a working model with good recall

|Day|Task|
|---|---|
|1-2|Get dataset (recommended public datasets below) → Telco Customer Churn (Kaggle) → IBM Watson Telco Churn (very common) → Bank Customer Churn (Kaggle)|
|3-4|Exploratory Data Analysis + feature engineering (tenure bins, total charges, service counts, etc.)|
|5-6|Build baseline XGBoost with class weights / scale_pos_weight to reduce false negatives|
|7|Simple LightGBM model → weighted ensemble (e.g., 0.6 XGBoost + 0.4 LightGBM) that maximizes recall @ precision threshold|

Deliverable: Notebook with ~80–85% recall and ensemble beating single models

#### Week 2 – Advanced Modeling + SHAP

Goal: Final model + explanations

|Day|Task|
|---|---|
|1-2|Hyperparameter tuning (Optuna or Hyperopt) with objective = recall|
|3|Train final ensemble (save both models + weights)|
|4-5|Train SHAP explainer → Use shap.TreeExplainer for both models → Pre-compute background dataset (100–500 samples) → Create a function that returns weighted SHAP values|
|6-7|Build prediction function that returns: { "churn_probability": 0.78, "prediction": "Churn", "shap_values": [...], "shap_expected_value": 0.12 }|

Deliverable: model/final_ensemble.pkl + shap_explainer.py working locally

#### Week 3 – FastAPI Backend + Real-time Inference

Goal: Production API

|Day|Task|
|---|---|
|1-2|Set up FastAPI project (src/api/main.py)|
|3|Create /predict endpoint that: → Validates input with Pydantic → Preprocesses → Loads models & explainer → Returns prediction + SHAP (base64 plot optional)|
|4|Add health check, versioning, logging|
|5|Write unit tests (pytest) for preprocessing & prediction|
|6-7|Dockerize the API ```docker|

Test locally with:

Bash

```
uvicorn src.api.main:app --reload
curl -X POST with sample JSON → get SHAP JSON back
```

#### Week 4 – React Dashboard

Goal: Beautiful real-time dashboard

|Day|Task|
|---|---|
|1|Create React app (create-react-app or Vite)|
|2-3|Customer lookup page: enter customer ID → call FastAPI → show: • Churn probability gauge • Prediction tag (Churn / No Churn) • SHAP force plot or waterfall (use react-shap or generate PNG on backend)|
|4|Dashboard with top 10 high-risk customers (mock or real)|
|5|Add global SHAP summary (bar plot of feature importance)|
|6-7|Make it responsive + dark mode (optional but looks pro)|

You can return SHAP plot as base64 PNG from FastAPI or use JSON + shap.plots in JS.

#### Week 5 – Docker Compose + Full Local Deployment

Goal: Run everything locally with one command

Create docker-compose.yml:

YAML

```
version: '3.8'
services:
  api:
    build: ./docker
    ports:
      - "8000:80"
    volumes:
      - ./model:/app/model
  dashboard:
    build: ./dashboard
    ports:
      - "3000:80"
    environment:
      - REACT_APP_API_URL=http://localhost:8000
```

Now docker-compose up --build runs everything.

#### Week 6 – AWS EC2 Deployment + Polish

|Day|Task|
|---|---|
|1|Launch EC2 (t3.medium or t3.large recommended) – Ubuntu 22.04|
|2|Install Docker + Docker Compose|
|3|Copy code + models via git or scp|
|4|Run docker-compose in production mode (with nginx reverse proxy optional)|
|5|Set up security group: ports 80, 443, 22|
|6|Add free SSL with Let’s Encrypt (certbot) or use AWS ACM + load balancer (optional)|
|7|Monitoring: add simple Prometheus + Grafana container (optional) Write final README + record 2-min demo video|

### Final Bonus Touches (if you have time)

- Add Redis cache for repeated customer lookups
- Batch prediction endpoint
- Model drift detection script (runs weekly)
- Send Slack/Email alert when high-value customer > 70% churn prob

### Recommended Public Dataset (quick start)

[https://www.kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (Already clean, perfect size ~7k rows)

### Summary – You will have at the end of 6 weeks:

- A real-time churn API reducing false negatives by ~25–30%
- Beautiful SHAP explanations in the response
- Professional React dashboard
- Fully dockerized & deployed on AWS EC2
- Something 100% portfolio-worthy (exactly what you wrote in your bullet points)
- 