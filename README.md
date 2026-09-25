<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=3000&pause=800&color=00E5A0&center=true&vCenter=true&width=720&lines=%24+whoami+%E2%86%92+MD+Piyal+Ahmmed;ML+Engineer+%E2%80%A2+MLOps+%E2%80%A2+LLM+Systems;Shipping+models+from+notebook+to+production;data+%E2%86%92+train+%E2%86%92+gate+%E2%86%92+deploy+%E2%86%92+monitor+%E2%86%92+retrain" alt="typing header"/>

<p>
  <a href="https://www.linkedin.com/in/md-piyal-ahmmed-bb1033205/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:piyalahmmed01@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white"/></a>
  <img src="https://img.shields.io/badge/📍_Germany-open_to_Werkstudent_%2F_Junior_roles-00E5A0?style=flat-square"/>
  <img src="https://komarev.com/ghpvc/?username=piyal21&style=flat-square&color=00E5A0&label=profile+views"/>
</p>

</div>

```python
class PiyalAhmmed:
    role       = "ML Engineer → MLOps"
    location   = "Schmalkalden, Germany 🇩🇪"
    education  = {
        "M.Sc.": "Applied Computer Science @ Hochschule Schmalkalden (ongoing)",
        "B.Sc.": "CSE @ Ahsanullah University of Science & Technology",
    }
    research   = "Mitigating Extrinsic Gender Bias for Bangla Classification — ACL 2026 Findings"
    shipped    = ["LLM + RAG systems in production", "FastAPI services", "vector search", "Dockerized ML"]
    building   = "Pünktlich — end-to-end MLOps on real Deutsche Bahn data"
    philosophy = "A model isn't done until it's versioned, monitored, and can be rolled back."
```

---

## 🚆 Currently building: `Pünktlich?`

> **Will my train leave on time?** Delay-risk predictions for German train departures, trained on ~226M historical stop events, fed by the live DB Timetables API every 15 minutes, monitored nightly against what actually happened, and retrained automatically when the world drifts. Runs on AWS serverless for **< $1/month**.

```mermaid
flowchart LR
  A["🗄️ HF + DB API"] --> B["🥉 Bronze → 🥈 Silver → 🥇 Gold<br/>Pandera contracts"]
  B --> C["🧪 Train<br/>LightGBM + calibration"]
  C --> D{"🚦 Gate<br/>beats champion<br/>& baseline?"}
  D -- yes --> E["🚀 Release<br/>S3 + SSM pointer"]
  D -- no --> R["📝 Record rejection"]
  E --> F["⚡ Serve<br/>FastAPI on Lambda"]
  F --> G["📉 Monitor<br/>drift + real outcomes"]
  G -- "3-day drift" --> C
```

<details>
<summary><b>📋 Build log</b> (updated as I ship)</summary>

| Phase | Scope | Status |
|---|---|---|
| 0 | Repo, tooling, CI skeleton, pre-commit | 🔲 |
| 1 | Historical ETL → bronze/silver/gold + data contracts | 🔲 |
| 2 | Training pipeline, MLflow tracking, promotion gate | 🔲 |
| 3 | FastAPI serving on Lambda, release + rollback | 🔲 |
| 4 | Live ingestion, nightly ETL, drift monitoring | 🔲 |
| 5 | Continuous training loop, alerting | 🔲 |
| 6 | Terraform, CD with OIDC, React frontend, public Health page | 🔲 |

</details>

### MLOps skills this project covers

| Concept | How it's done here |
|---|---|
| **Data engineering** | Medallion layers, idempotent partition overwrites, schema contracts, quarantine on failure |
| **Orchestration** | Airflow 3 TaskFlow, dynamic task mapping, deferrable sensors |
| **Experiment tracking** | MLflow runs pinned to git SHA + data snapshot hash |
| **Model registry & gating** | `@champion` / `@challenger` aliases, metric + slice gate vs. baseline |
| **Serving** | FastAPI + Mangum on Lambda, container images, hot model swap without redeploy |
| **Monitoring** | Evidently data/prediction drift, daily Brier/AUC/calibration on real labels |
| **Continuous training** | Drift flag → Airflow sensor → retrain → gate → release |
| **CI/CD** | GitHub Actions, keyless AWS auth (OIDC), smoke tests, `terraform plan` on PRs |
| **Infrastructure as Code** | Terraform modules, remote state with locking |
| **Security** | Least-privilege IAM, SSM secrets, Trivy + gitleaks + pip-audit, no pickle, SHA-256 artifact manifests |
| **Cost engineering** | Serverless only, budget alarms, S3 lifecycle rules |

---

## 🛠️ Stack

**MLOps & Infra**
<br/>
![Airflow](https://img.shields.io/badge/Airflow_3-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow_3-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Evidently](https://img.shields.io/badge/Evidently-ED0400?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-Lambda_·_S3_·_CloudFront_·_SSM_·_CloudWatch-232F3E?style=flat-square)
![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white)

**ML / DL / LLM**
<br/>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-2E8B57?style=flat-square)
![Hugging Face](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langgraph&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-FF5A50?style=flat-square)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square)

**Data & Backend**
<br/>
![Python](https://img.shields.io/badge/Python_3.12-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Pandera](https://img.shields.io/badge/Pandera-4B32C3?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)

**Quality & Security**
<br/>
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat-square&logo=ruff&logoColor=black)
![mypy](https://img.shields.io/badge/mypy-2A6DB2?style=flat-square)
![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square)
![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=uv&logoColor=white)

---

## 📌 Selected work

| Project | What's interesting about it | Stack |
|---|---|---|
| 🚆 [**Pünktlich?**](https://github.com/piyal21/puenktlich) | Closed-loop MLOps: gated releases, pointer-based rollback, drift-triggered retraining | Airflow · MLflow · Lambda · Terraform |
| 🔍 [**Document QA (RAG)**](https://github.com/piyal21/Gen-AI-Projects/tree/master) | Semantic retrieval over unstructured docs with embeddings + FAISS, LangChain chains, Streamlit UI | OpenAI · FAISS · LangChain |
| ✍️ [**LinkedIn Post Generator**](https://github.com/piyal21/Gen-AI-Projects/tree/master) | Prompt-engineered multi-variant generation with tone / length / audience controls | LLMs · Streamlit |
| 💳 [**Credit Card Fraud Detection**](https://github.com/piyal21/10MS_ML_Assessment) | Heavy class imbalance; LogReg / SVM / RF / KNN compared on precision-recall | scikit-learn |

### 📄 Research

**Mitigating Extrinsic Gender Bias for Bangla Classification Tasks** — *Findings of ACL 2026*
<br/>Joint-loss optimization to reduce gender bias in Bangla classifiers without sacrificing task accuracy.
<br/>[![arXiv](https://img.shields.io/badge/arXiv-2411.10636-B31B1B?style=flat-square&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.10636)

---

## 📊 Activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=piyal21&theme=tokyonight&hide_border=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=piyal21&layout=compact&theme=tokyonight&hide_border=true" height="165"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=piyal21&theme=tokyo-night&hide_border=true&area=true" width="95%"/>
</p>

<div align="center">
<sub><code>git commit -m "always be shipping"</code></sub>
</div>
