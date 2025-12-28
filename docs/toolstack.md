\# Toolstack (final, Week 2)



\## Core

\- Python 3.10, Conda env

\- Git + GitHub (source control)

\- DVC (data versioning) with local remote (or S3 if available)

\- MLflow (experiment tracking \& basic model registry)

\- Docker (containerization)

\- FastAPI + Uvicorn (serving)

\- Streamlit (optional demo UI)

\- Hugging Face Transformers + Datasets (ASR model \& fine-tuning)

\- Whisper model (openai/whisper family or open-source replication)

\- Gensim (LDA topic modeling)

\- spaCy (NER) + Labeling tool (doccano / Label Studio)

\- ffmpeg / sox (audio processing)



\## Orchestration \& CI

\- Use DVC pipelines (`dvc.yaml`) + `dvc repro`. For CI, GitHub Actions to run unit tests and lightweight pipeline.



\## Monitoring / Observability

\- MLflow UI for metrics, model artifacts

\- Logging (structured logs for inference)



