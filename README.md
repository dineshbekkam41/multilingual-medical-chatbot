# multilingual-medical-chatbot
Multilingual Medical Chatbot using Sarvam-2B + LoRA + mBART translation


# 🏥 Multilingual Medical Chatbot

A medical Q&A chatbot that understands and responds in **5 languages**:

🇺🇸 English | 🇮🇳 हिंदी | 🇮🇳 తెలుగు | 🇮🇳 தமிழ் | 🇮🇳 ಕನ್ನಡ

---

## 🧠 Architecture
- **Base Model:** `sarvamai/sarvam-2b-v0.5` — natively trained on Indian languages
- **Fine-Tuning:** LoRA (r=16, α=32) via PEFT
- **Translation:** `facebook/mbart-large-50-many-to-many-mmt` for Indian language data
- **Quantization:** 4-bit NF4 via bitsandbytes — runs on free T4 GPU
- **UI:** Gradio chat interface with auto language detection

## 📦 Datasets Used
| Dataset | Language | Rows Used |
|---------|----------|-----------|
| `ruslanmv/ai-medical-chatbot` | English | 1,500 |
| `lavita/medical-qa-datasets` (health_advice) | English | 500 |
| `lavita/medical-qa-datasets` (mediqa) | English | 300 |
| Translated via mBART-50 | Hindi, Telugu, Tamil, Kannada | 800 |



## 📁 Files
| File | Description |
|------|-------------|
| `multilingual_medical_chatbot_v8.ipynb` | Main Colab notebook |
| `MedicalChatbot_Presentation.pptx` | Project presentation slides |

## ⚙️ Requirements
```
transformers==4.46.3
accelerate==1.1.1
bitsandbytes>=0.45.2
peft==0.13.2
trl==0.8.6
sentencepiece
datasets
gradio
```

## ⚠️ Disclaimer
Educational prototype only. Always consult a licensed doctor.
```


```
multilingual-medical-chatbot/
├── README.md                              ← project description + colab button
├── multilingual_medical_chatbot_v8.ipynb  ← main notebook
└── MedicalChatbot_Presentation.pptx       ← slides
