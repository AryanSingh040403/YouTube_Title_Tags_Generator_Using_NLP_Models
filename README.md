
# 🎬 YouTube Title & Tags Generator using NLP

A deep learning powered system that automatically generates catchy video titles and SEO-optimized tags for YouTube videos based on their transcript or summary.

---

## 🧠 Project Overview

This project fine-tunes three Transformer models:
- **BART** → Summarization & Title Generation
- **T5** → Keyword & Tag Generation
- **DistilBERT** → Category Classification

These models are combined into one end-to-end pipeline and deployed with a Streamlit app.

---

## 🚀 Features
- Automatically generates attractive YouTube titles
- Suggests 5–10 SEO-friendly tags
- Classifies videos into relevant categories
- Streamlit-based web interface
- Built using Hugging Face Transformers and KeyBERT

---

## 📁 Project Structure

YouTube_Title_Tags_Generator/
├── data/
│   └── data.csv
├── models/
│   ├── bart-title/
│   ├── t5-tags/
│   ├── distilbert-category/
│   └── label_encoder.pkl
├── scripts/
│   ├── 01_preprocessing.ipynb
│   ├── 02_train_bart.ipynb
│   ├── 03_train_t5.ipynb
│   ├── 04_train_distilbert.ipynb
│   └── 05_inference_pipeline.ipynb
├── app.py
├── requirements.txt
└── README.md

---

## ⚙️ Setup Instructions

### Step 1: Install dependencies
Run this in your terminal:
    pip install -r requirements.txt

### Step 2: (Optional) Re-train models
Open the training notebooks inside `/scripts/` to fine-tune each model.

### Step 3: Run the Streamlit app
    streamlit run app.py

---

## 💡 Example Output
Generated Title: "How AI Is Revolutionizing Content Creation in 2025"  
Generated Tags: ["AI", "machine learning", "YouTube automation", "content tools"]  
Predicted Category: Technology

---

## 👨‍💻 Author
**Aryan Singh**  
AIML Engineer | Deep Learning Researcher | ML | NLp Enthusiast  
📧 your-aryansingh20030404@gmail.com


---

## 🙌 Acknowledgements
- Hugging Face Transformers  
- KeyBERT  
- Streamlit
