# 🏥 Adverse Medical Event Prediction from Phone Calls

> **AI-powered system to detect and predict adverse medical events from patient-nurse phone conversations in real-time**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Hackathon](https://img.shields.io/badge/Hackathon-2026-orange.svg)]()

## 🎯 Problem Statement

Millions of conversations happen daily between medical agents/nurses and patients. Often, subtle indications of adverse events go unnoticed—events that could lead to serious complications if not identified quickly. 

**This system automatically identifies and flags potential adverse events from recorded phone conversations, enabling rapid intervention and better patient outcomes.**

## 🚀 Key Features

- ⚡ **Real-time Detection**: Identifies 7 categories of medical adverse events
- 🎯 **Multi-label Classification**: Detects multiple concurrent issues
- 📊 **Risk Scoring**: Assigns severity levels (CRITICAL, HIGH, MODERATE, LOW, NONE)
- 🚀 **Fast Inference**: ~0.5s per conversation using Groq's LPU technology
- 🧠 **Context-Aware**: Understands patient responses vs. doctor questions

## 📊 Adverse Event Categories

| Category | Description | Risk Weight |
|----------|-------------|-------------|
| 🚨 **Emergency** | Urgent situations requiring immediate care | 1.0 |
| 🤧 **Allergic Reaction** | Allergic responses, breathing difficulties | 0.9 |
| 🦠 **Infection** | Signs of infection, fever | 0.85 |
| 💊 **Medication Error** | Wrong dose, missed medication | 0.8 |
| 📉 **Symptom Worsening** | Patient condition deteriorating | 0.7 |
| 🤢 **Side Effects** | Medication-induced symptoms | 0.5 |
| ❌ **Non-Compliance** | Not taking meds as prescribed | 0.4 |

## 🛠️ Installation

```bash
# Clone repository
git clone https://github.com/GarvitK13/Adverse-Medical-Event-Prediction-VibeCoders-.git
cd Adverse-Medical-Event-Prediction-VibeCoders-

# Create virtual environment
python -m venv .venv
.venv\Scripts\activate  # Windows
# source .venv/bin/activate  # Linux/Mac

# Install dependencies
pip install -r requirements.txt

# Set up API key
copy .env.example .env
# Edit .env and add your Groq API key
```

### Get Groq API Key (Free!)
1. Visit https://console.groq.com/
2. Sign up for free
3. Create API key
4. Add to `.env`: `GROQ_API_KEY=your_key_here`

## 📈 Dataset

- **Source**: [MTS_Dialogue-Clinical_Note](https://huggingface.co/datasets/har1/MTS_Dialogue-Clinical_Note)
- **Size**: 1,301 patient-nurse dialogues
- **Adverse Events**: 384 (29.5%)
- **Labeling**: Groq API (Llama 3.1-8b-instant)

## 🎯 Performance

| Metric | Value |
|--------|-------|
| Speed | ~0.4s per dialogue |
| Processing | ~10 min for 1,301 samples |
| Cost | ~$0.03 total (nearly free!) |
| Accuracy | Context-aware LLM classification |

## 🔮 Future Plans

- [ ] Audio processing with Deepgram/Whisper
- [ ] Fine-tune Bio-ClinicalBERT for faster inference
- [ ] Real-time dashboard
- [ ] REST API for EMR integration
- [ ] Mobile app for nurses

## ⚠️ Security

**Never commit API keys!** Use `.env` file (git-ignored):
```
GROQ_API_KEY=your_key_here
```

## 👥 Team VibeCoders

Built for Hackathon 2026 🚀

## 📧 Contact

GitHub: [@GarvitK13](https://github.com/GarvitK13)

---
⭐ Star if useful! Built with ❤️ for patient safety