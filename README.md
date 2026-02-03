[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

# 🎓 Indic-Edge-Scribe: A Localized AI-Driven Note-Taking System for Indian English Accents

### *Accent-Tuned Edge-AI for Automated Transcription & Summarization*

**Publication Status:** `Conference Paper Accepted (IEEE Elexcom 2025)`

**Core Model Repository:** [whisper-small-indian-accent](https://github.com/omsusi/whisper-small-indian-accent)

---

## 🏗️ System Architecture

This project introduces a self-contained, offline IoT module designed to automate the capture, transcription, and summarization of classroom lectures and conferences. By leveraging **Edge-AI**, the system eliminates the need for constant cloud connectivity, ensuring data privacy and zero-latency access in resource-constrained educational environments.

### **Technical Backbone**

* **Hardware Platform:** Optimized for the **Raspberry Pi 4 Model B** (Quad-core ARM Cortex-A72 @ 1.5 GHz). The system incorporates a multi-component heat sink array to prevent thermal throttling during high-load AI inference.


* **Localized Processing:** Every phase—from audio capture via a high-quality USB directional microphone to final report generation—is performed entirely on-device.


* **Software Stack:** Built on a modular Python framework utilizing **Flask** for user interaction, **PyTorch** for model execution, and **systemd** for automated service orchestration upon boot.



---

## 🧠 Proprietary AI Pipeline

The project’s primary technical innovation is its specialized dual-model processing pipeline, engineered for high-density academic content.

### **1. Fine-Tuned Speech-to-Text (STT)**

The system utilizes a specialized variant of OpenAI’s **Whisper-small** architecture.

* **Domain Adaptation:** To address regional accent variability and technical jargon, the model was fine-tuned using the **NPTEL2020 Indian English Speech Dataset**.


* **Performance:** Empirical validation demonstrates a significant reduction in the Word Error Rate (WER) and Character Error Rate (CER) compared to pre-trained models.


* **Fine-Tuned Weights:** Accessible at [omsusi/whisper-small-indian-accent](https://github.com/omsusi/whisper-small-indian-accent).

### **2. Abstractive Summarization Engine**

Unlike traditional extractive tools, the system employs the **distilbart-cnn-12-6** model for abstractive summarization.

* **Paraphrasing Logic:** The engine paraphrases content to generate coherent, human-readable summaries that capture core concepts rather than just concatenating sentences.


* **Efficiency:** The pipeline is optimized to deliver high-quality summaries within the computational constraints of edge hardware.



---

## 📈 Enterprise & ERP Potential

While currently implemented as a student support tool, the architecture is designed with a scalable **Enterprise Resource Planning (ERP)** mindset:

* **Institutional Integration:** The modular backend is prepared for centralized institutional deployment, enabling standardized content tracking across diverse classroom sectors.


* **Data Liquidity:** Automated compilation of intelligence into structured PDF reports creates a searchable, archive-ready database of organizational knowledge.


* **Secure Command Interface:** Integrated vsftpd protocols and a localized web interface allow educators (commanders) to manage and retrieve data through a secure, multi-access interface.



---

## 📊 Performance Validation

| Metric | Pre-trained Whisper-small | **Custom-Trained Whisper-small** |
| --- | --- | --- |
| **Word Error Rate (WER)** | 1.0063 | **0.3187** |
| **Character Error Rate (CER)** | 0.8895 | **0.0897** |
| **Overall Accuracy** | 2.50% | **58.75%** |

Full evaluation metrics and methodology available in the accompanying documentation.

---

## 🚀 Future Roadmap

* **Speaker Diarization:** Multi-speaker identification for complex, interactive meeting environments.


* **Multimodal Integration:** Correlating audio data with visual triggers (lecture slides/whiteboard notes) for enriched context.


* **Inference Optimization:** Investigation into 8-bit quantization to enable zero-latency, live-stream summarization.



---

## ⚖️ Intellectual Property Notice

*Portions of this project’s implementation methodologies are currently accepted for conference publication. Proprietary code and datasets are restricted to protect intellectual property rights until official release.*

---

## 👥 Development Team & Acknowledgments

* **Lead Architect & Developer:** [Omsubhra Singha](https://www.linkedin.com/in/omsubhra-singha-30447a254/) — responsible for system engineering, full-stack implementation, and hardware-software integration.


* **Research & Strategic Planning:** [Dr. Wanbanker Khongbuh](https://scholar.google.com/citations?user=MAg8y58AAAAJ&hl=en) — provided the foundational conceptual framework and [Dr. Preetisudha Meher](https://scholar.google.com/citations?user=7LM3IXgAAAAJ&hl=en) provided the academic direction for the project.


* **Model Optimization & Logic Design:** Aman Kumar — provided technical support in fine-tuning the Whisper model and enhancing system logic flow.


* **Documentation & Research Analysts:** [Priyam Gupta](https://www.linkedin.com/in/priyam-gupta-78b542339/) & [Roshan Sahani](https://www.linkedin.com/in/roshan-sahani-b50b63278/) — led the comprehensive technical documentation and literature analysis.

