\# Requirements



\## Functional Requirements

1\. System shall accept meeting audio (.wav) as input.

2\. System shall generate speaker-labeled transcripts.

3\. System shall discover discussion topics from transcripts.

4\. System shall extract action items with TASK, ASSIGNEE, DEADLINE.

5\. System shall generate an executive summary.

6\. System shall expose an API endpoint to process a meeting and return JSON output.

7\. System shall allow batch/offline processing for experiments.



\## Non-Functional Requirements

1\. Reproducibility: pipeline must be reproducible via DVC.

2\. Traceability: all experiments logged in MLflow.

3\. Scalability: design should support larger datasets/models.

4\. Usability: simple CLI/API for demo.

5\. Performance: baseline inference should process 1 minute of audio within a few minutes.

6\. Maintainability: modular code structure with clear separation of concerns.

7\. Portability: system should run via Docker container.



