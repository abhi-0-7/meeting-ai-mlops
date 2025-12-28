**# Compute Plan**



**## Local Development**

**- \*\*Machine:\*\* Windows 11 laptop with NVIDIA GeForce RTX 4060 Laptop GPU**

**- \*\*Environment:\*\* Conda (Python 3.10), PyTorch with CUDA**

**- \*\*Use:\*\* All experiments, preprocessing, and baseline model training.**



**## ASR Training Strategy**

**- Prefer GPU-based fine-tuning for Whisper models.**

**- Start with \*\*whisper-tiny or whisper-small\*\* for fast iteration.**

**- Fine-tune on a representative subset of AMI (1–5 hours audio).**

**- Log all runs to MLflow.**



**## Fallback (if GPU unavailable)**

**- Use tiny models (`whisper-tiny`, `tiny.en`).**

**- Simulate fine-tuning with very few steps or adapter-style tuning.**

**- Rely more on pre-trained checkpoints.**



**## Final Demo Serving**

**- Export trained models.**

**- Serve via FastAPI on CPU (acceptable latency for demo).**

**- GPU can be used locally if available.**



**## Example Compute Budget**

**- \*\*Local GPU (RTX 4060):\*\***

  **- Preprocessing: minutes**

  **- ASR fine-tuning (tiny/small): ~1–3 hours on subset**

  **- LDA + NER: minutes**

**- \*\*Cloud GPU (if needed):\*\***

  **- T4 / RTX 30/40 / A100: few hours for larger models.**



**## Storage**

**- Local disk for active work.**

**- DVC remote (optional S3/GDrive) for backup and sharing.**



