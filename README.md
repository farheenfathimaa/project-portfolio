# 🗂️ Farheen Fathima — Project Portfolio

> **AI/ML Engineer · LLM Applications · RAG Pipelines · MLOps**
> Production-focused engineer with hands-on experience building end-to-end ML systems, multi-agent LLM frameworks, and scalable data pipelines.

📧 farheennfathima@gmail.com &nbsp;|&nbsp; [LinkedIn](https://www.linkedin.com/in/farheenfathimaa) &nbsp;|&nbsp; [HuggingFace](https://huggingface.co/farheenfathimaa) &nbsp;|&nbsp; [GitHub](https://github.com/farheenfathimaa) &nbsp;|&nbsp; [X](https://x.com/farheenfathima_) &nbsp;

--

## 🤖 LLM, Agents & RAG

| Project | Description | Stack | Date |
|--------|-------------|-------|------|
| [legal-qa-lora-finetune](https://github.com/farheenfathimaa/legal-qa-lora-finetune) | LoRA fine-tuning of Mistral-7B on a legal Q&A instruction dataset using 4-bit NF4 quantization. Covers synthetic dataset generation, adapter training (rank=8, alpha=16 on q_proj/v_proj), MLflow experiment tracking with per-step loss curves, before/after ROUGE-L evaluation, and a FastAPI serving layer for the fine-tuned model. | Python, PyTorch, PEFT, Mistral-7B, MLflow, FastAPI | Jul 2026 |
| [FinQA-SFT-Tuner](https://github.com/farheenfathimaa/FinQA-SFT-Tuner) | End-to-end LLM alignment framework for financial QA. Two-stage training: SFT with LoRA adapters (Qwen2.5-0.5B via LLaMA Factory) → DPO alignment using a custom reward model scoring semantic accuracy (Sentence Transformers) + conciseness penalty. Includes Streamlit evaluation dashboard with glassmorphic UI, side-by-side Base/SFT/DPO comparison, and Plotly response-length charts. Containerized with Docker Compose. | Python, PyTorch, PEFT, LLaMA Factory, DPO, Streamlit, Docker | Jul 2026 |
| [VoiceDataCurator](https://github.com/farheenfathimaa/VoiceDataCurator) | Automated multilingual speech curation pipeline for 8+ languages using OpenAI Whisper; includes SNR analysis, silence/clipping detection, and configurable YAML thresholds. Published dataset on HuggingFace with quality metrics manifest. | Python, Whisper, Librosa, Streamlit, Docker | Feb 2026 |
| [urban-threadz-rag-chatbot](https://github.com/farheenfathimaa/urban-threadz-rag-chatbot) | Dual-purpose production RAG chatbot for retail with role-based access control (guest/admin). Multi-tier pipeline: multi-format ingestion → Sentence Transformer embeddings → FAISS → LLM routing (Groq + Gemini fallback). Containerized with Docker Compose. | Python, LangChain, FAISS, Groq, Gemini, Streamlit, Docker | Feb 2026 |
| [NL-to-SQL-query](https://github.com/farheenfathimaa/NL-to-SQL-query) | Converts natural language questions into SQL queries using LLMs. | Python | Mar 2026 |
| [Math-Routing-Agent](https://github.com/farheenfathimaa/Math-Routing-Agent) | Multi-agent AI system with dynamic routing logic using LangChain and Flask. Integrated OpenAI and HuggingFace providers. Built evaluation suite with 500+ test cases achieving 99%+ routing accuracy. | Python, Flask, LangChain, OpenAI, HuggingFace | Sep 2025 |
| [llm-extraction-pipeline](https://github.com/farheenfathimaa/llm-extraction-pipeline) | End-to-end RAG-like pipeline for structured financial/legal insight extraction from diverse document formats. Implemented caching and token management achieving >30% cost optimization. Containerized with Docker. | Python, Streamlit, OpenAI, Anthropic, Docker | Aug 2025 |

---

## 🔍 Search & Data Engineering

| Project | Description | Stack | Date |
|--------|-------------|-------|------|
| [pyspark-claims-anomaly-etl](https://github.com/farheenfathimaa/pyspark-claims-anomaly-etl) | Distributed ETL pipeline in PySpark processing 10M+ synthetic healthcare claims. Performs relational joins across 3 tables, window functions (rolling avg, running totals, patient ranking), and statistical anomaly detection (Z-score > 3.0 for billing fraud, payment ratio < 0.15 for underpayment). Outputs partitioned Parquet by state/claim_status. Includes a Pandas vs Spark benchmark — Pandas OOMs at 10M rows, PySpark completes in ~32s. | PySpark, Python, Pandas, Parquet, Faker | Jul 2026 |
| [GCP_ML_Pipeline](https://github.com/farheenfathimaa/GCP_ML_Pipeline) | End-to-end MLOps pipeline on GCP: BigQuery data ingestion → Vertex AI Custom Training (RandomForest, logged via Vertex AI Experiments) → model upload to GCS → Kubeflow Pipeline orchestrating model registry, endpoint creation, and deployment → Vertex AI Model Monitoring for feature skew and prediction drift. CI/CD via GitHub Actions with Workload Identity Federation — builds Docker image to Artifact Registry and submits PipelineJob on push. | GCP, Vertex AI, BigQuery, Kubeflow Pipelines, Docker, GitHub Actions | Jun 2026 |
| [aws-infra-bootstrap](https://github.com/farheenfathimaa/aws-infra-bootstrap) | Production-ready AWS infrastructure provisioned with modular Terraform — VPC (public/private subnets), ECS Fargate cluster, RDS PostgreSQL (private subnet), S3 with encryption, and CloudWatch logging. CI/CD via GitHub Actions: `terraform plan` on PRs, `terraform apply` on merge to main. Remote state managed in S3. | Terraform, AWS (ECS · RDS · S3 · VPC), GitHub Actions, Docker | May 2026 |
| [semantic-search-engine](https://github.com/farheenfathimaa/semantic-search-engine) | Semantic search with sub-second retrieval; tested across 1,000+ query-document pairs using precision@k, recall@k, and MRR. Production-ready REST API via FastAPI with <200ms response times. | FastAPI, Sentence Transformers, FAISS, Docker | Jul 2025 |
| [log_analytics_project](https://github.com/farheenfathimaa/log_analytics_project) | 3-node ELK stack on Kubernetes handling 100K+ daily log entries with auto-scaling and zero-downtime rolling updates via GitHub Actions CI/CD. Automated log classification achieving 92% anomaly detection accuracy. | Kubernetes, Docker, ELK Stack, CI/CD | Jun 2025 |

---

## 📊 Machine Learning & Data Science

| Project | Description | Stack | Date |
|--------|-------------|-------|------|
| [regional-demand-forecast-geo](https://github.com/farheenfathimaa/regional-demand-forecast-geo) | End-to-end time-series forecasting pipeline on 387 US metros using Zillow ZHVI data. Benchmarks Statsmodels + Prophet vs pooled XGBoost (18-month test, MAPE 11.4% / 13.3% / 3.1% respectively). Geospatial choropleth via GeoPandas/Folium reveals East/West divide (+0.57 longitude correlation). SHAP explainability shows lag_1/lag_3 dominate over geography. Runs on Databricks. | Python, XGBoost, Prophet, GeoPandas, SHAP, Folium | Aug 2026 |
| [intel_cv_mlops_pipeline](https://github.com/farheenfathimaa/intel_cv_mlops_pipeline) | Complete CV MLOps pipeline on the Intel Image Classification dataset (6 scene classes). Combines a Logistic Regression baseline (hand-crafted RGB + Canny edge features) with a custom 3-layer TensorFlow CNN (~77% accuracy). Served via FastAPI with dual `/predict/baseline` and `/predict/cnn` endpoints; validated with a pytest suite covering preprocessing, inference, and API endpoints. Dataset reconstructed from 8 split archives via Git. | Python, TensorFlow, Scikit-Learn, FastAPI, pytest, Jupyter | Jun 2026 |
| [Image-Classification-Object-Detection-Pipeline](https://github.com/farheenfathimaa/Image-Classification-Object-Detection-Pipeline) | Production CV pipeline combining fine-tuned ResNet-50 (88.5% validation accuracy on 37-class Oxford Pet dataset) and YOLOv5s object detection. ResNet-50 exported to ONNX Runtime for optimized inference. Served via FastAPI with single image, batch (up to 8), and detection endpoints; ~15ms GPU latency. Model weights managed via Git LFS. | PyTorch, ONNX Runtime, YOLOv5, FastAPI, Torchvision | Jun 2026 |
| [phonepe-project](https://github.com/farheenfathimaa/phonepe-project) | End-to-end data science pipeline on India's PhonePe Pulse dataset — automated JSON ETL into 9 normalized MySQL tables, 20+ EDA visualizations uncovering regional payment patterns, and XGBoost/Random Forest models predicting transaction volumes (R² ~0.97). Delivered via interactive multi-page Streamlit dashboard. | Python, XGBoost, MySQL, Streamlit, Plotly, Pandas | May 2026 |
| [real-estate-investment-advisor](https://github.com/farheenfathimaa/real-estate-investment-advisor) | End-to-end ML pipeline for Indian housing market — predicts investment viability (classification) and future price trends (regression). Trains 6 models (Random Forest, XGBoost, Logistic Regression), tracks all experiments via MLflow, and serves results through a multi-page Streamlit dashboard with live EDA and model comparison. | Python, XGBoost, Scikit-Learn, MLflow, Streamlit, Pandas | Apr 2026 |
| [mental-health-tech-eda](https://github.com/farheenfathimaa/mental-health-tech-eda) | Deep EDA on mental health in the tech workplace — 20+ visualizations (heatmaps, pairplots, stacked bars) uncovering treatment predictors. Key finding: family history + work interference are stronger indicators than age or gender. Includes stakeholder-ready PPTX report. | Python, Pandas, Matplotlib, Seaborn, Jupyter | Mar 2026 |
| [tesla-stock-price-prediction](https://github.com/farheenfathimaa/tesla-stock-price-prediction) | End-to-end TSLA stock forecasting using RNN, LSTM, and Stacked LSTM with technical indicator engineering (RSI, MACD, Bollinger Bands). Multi-horizon forecasting (1/5/10-day) with interactive Streamlit dashboard. | Python, TensorFlow, LSTM, Streamlit, Plotly | Mar 2026 |
| [flipkartProject-CSATScore](https://github.com/farheenfathimaa/flipkartProject-CSATScore) | Customer satisfaction score prediction and analysis for e-commerce using ML models. | Python, Jupyter, Scikit-Learn | Mar 2026 |

---

## 🌐 Full Stack & Web Apps

| Project | Description | Stack | Date |
|--------|-------------|-------|------|
| [ai-ticket-triage-mern](https://github.com/farheenfathimaa/ai-ticket-triage-mern) | Full-stack MERN support-ticket triage tool with an embedded LangChain agent (Groq/OpenAI) that auto-classifies tickets by category + priority and drafts a suggested first response on creation. Graceful rule-based fallback ensures the pipeline never fails without an API key. JWT auth, 29 passing Jest tests (82.5% coverage), Nginx-proxied frontend, one-command Docker Compose deploy, GitHub Actions CI. | Node.js, Express, MongoDB, React, LangChain, Groq, Docker | Aug 2026 |
| [job-application-tracker](https://github.com/farheenfathimaa/job-application-tracker) | High-performance job application tracker with full CRUD lifecycle management, instant search/filter, and dark mode UI. Includes >80% unit test coverage, OpenAPI/Swagger docs, and one-command Docker setup. | Spring Boot 3, Java 21, React, PostgreSQL, Docker | Mar 2026 |

---

## 🦀 Systems & Graph Engineering

| Project | Description | Stack | Date |
|--------|-------------|-------|------|
| [rust-graphmind](https://github.com/farheenfathimaa/rust-graphmind) | Rust CLI + axum REST API for ingesting relational CSV data into Neo4j and querying it as a graph. Supports shortest-path traversal, degree centrality, and 1–2 hop relationship queries via Cypher. Batched idempotent ingestion (624 nodes, 1998 relationships). 4 integration tests via testcontainers spinning up a real Neo4j container. Fully Dockerized with docker-compose. | Rust, axum, Neo4j, Cypher, Docker | Aug 2026 |

---

## 📈 Data Analytics & Business Intelligence

| Project | Description | Stack | Date |
|--------|-------------|-------|------|
| [NovaDash](https://github.com/farheenfathimaa/NovaDash) | End-to-end retail sales analytics for a fictional 3-year dataset. Covers KPI development, YoY revenue tracking, discount impact analysis, and regional performance. Delivers 5 dashboards across all three major BI tools. Key findings: Q4 drives 35% of annual revenue; 10%+ discounts cannibalize margins without volume gains. | Excel, Tableau, Power BI, DAX | Mar 2026 |

---

## 🧰 Tech Stack

**LLM & GenAI:** LangChain · OpenAI API · Anthropic Claude API · Groq · Gemini · FAISS · RAG · Prompt Engineering · HuggingFace Transformers · BERT

**ML/DL:** PyTorch · TensorFlow · Scikit-Learn · XGBoost · CNNs · Transfer Learning

**Production & MLOps:** Docker · FastAPI · Kubernetes · ELK Stack · CI/CD (GitHub Actions) · Streamlit

**Data & Tools:** Python · SQL · Pandas · NumPy · OpenCV · Git · Linux

---

> 💡 *This is a living index — updated as new projects are completed.*
> Full list of repositories: [github.com/farheenfathimaa](https://github.com/farheenfathimaa)
