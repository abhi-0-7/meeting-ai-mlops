\# Acceptance Criteria \& Success Metrics



\## Acceptance criteria (must pass)

1\. \*\*Transcript quality:\*\* WER <= 25% on held-out AMI test split (baseline). Better if <= 15% on clear meetings.

2\. \*\*Topic discovery:\*\* Coherence (c\_v) >= 0.40 for chosen number of topics (or subjectively high topic interpretability).

3\. \*\*NER action items:\*\* Entity extraction F1 >= 0.60 on annotated test set (TASK/ASSIGNEE/DEADLINE).

4\. \*\*End-to-end demo:\*\* Upload meeting audio → API returns JSON with transcript, topics, action items, executive summary.

5\. \*\*MLOps:\*\* Data versioning with DVC, experiments tracked in MLflow; reproducible pipeline (`dvc repro` or single script) that runs end-to-end (on a small sample).



\## Evaluation metrics (quantitative)

\- ASR: WER (primary), CER (secondary)

\- NER: Precision, Recall, F1 (per label + micro/macro)

\- Topics: Coherence (c\_v), and manual inspection of top-words

\- Summarization (if implemented): ROUGE-1/2/L

\- System: latency for inference (per-minute audio), pipeline reproducibility time



\## Non-functional

\- Reproducible: `conda env` + `requirements.txt` + `dvc` stage

\- Documented: README + project doc

\- Demo: Provide small web endpoint locally (FastAPI) that processes one audio file



