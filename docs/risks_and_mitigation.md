\# Risks and Mitigation



\## 1. Large audio data \& limited disk

\*\*Risk:\*\* AMI corpus is large; local storage may fill quickly.  

\*\*Mitigation:\*\* Use DVC to track only manifests; optionally push raw data to remote (S3/GDrive). Work on small subsets for iteration.



\## 2. Whisper fine-tuning time

\*\*Risk:\*\* Full fine-tuning is compute expensive.  

\*\*Mitigation:\*\* Start with small models (tiny/small), transfer learning, freeze layers, limit steps, and augment data instead of full training.



\## 3. NER annotation burden

\*\*Risk:\*\* Labeling action items is time-consuming.  

\*\*Mitigation:\*\* Label only 200–500 examples; use active learning and rule-based bootstrapping to reduce effort.



\## 4. Real-time pipeline complexity

\*\*Risk:\*\* True streaming ASR + inference is complex.  

\*\*Mitigation:\*\* Simulate real-time using chunked audio or streaming transcripts for demo.



\## 5. Integration complexity

\*\*Risk:\*\* Multiple components (ASR, topics, NER, API) may not integrate smoothly.  

\*\*Mitigation:\*\* Build and test each module independently; integrate incrementally with small samples.



\## 6. Time constraints

\*\*Risk:\*\* Phase I has limited weeks.  

\*\*Mitigation:\*\* Prioritize baseline end-to-end system first, then iterate on quality.



