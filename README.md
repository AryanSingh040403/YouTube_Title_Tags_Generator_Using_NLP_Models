# YouTube Title & Tags Generator

I built this pipeline to automate the boring part of YouTube uploads: writing titles and tags. Instead of agonizing over SEO manually or guessing what keywords work, I fine-tuned a few Transformer models to analyze the transcript and generate the metadata automatically.

## How It Works

The system uses an ensemble of three specific models to handle different parts of the metadata generation:

* **BART:** Handles the heavy lifting for text summarization to generate a relevant title.
* **T5:** Digs through the content to extract specific keywords and generate tags.
* **DistilBERT:** Classifies the video into the correct category (Tech, Education, Gaming, etc.).

Everything is wrapped in a simple Streamlit interface so you don't have to run inference scripts manually every time.

## Features

* Generates titles based on video transcripts/summaries.
* Suggests 5–10 relevant tags.
* Classifies videos into standard YouTube categories.
* Simple web UI built with Streamlit.

## Project Structure

```text
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
```

## Setup Instructions

1. Install dependencies
Run this in your terminal:
pip install -r requirements.txt

2. (Optional) Re-train models
If you want to improve performance on your specific niche, open the training notebooks inside /scripts/ to fine-tune each model on your own dataset.

3. Run the Streamlit app
streamlit run app.py

Example Output
Generated Title: "How AI Is Changing Content Creation in 2025"

Generated Tags: ["AI", "machine learning", "YouTube automation", "content tools"]

Predicted Category: Technology

## Roadmap

[ ] Add support for longer video transcripts (currently limited by BART token size).

[ ] Improve tag relevance for non-English videos.

[ ] Dockerize the application for easier deployment.

## Author

Built by - Aryan Singh
I am a Machine Learning Engineer and Deep Learning researcher with a deep enthusiasm for NLP. I'm passionate about building practical systems that bridge the gap between complex research and real-world utility.
HuggingFace - https://huggingface.co/aryan0404
email - aryansingh20030404@gmail.com
Linkdin - www.linkedin.com/in/aryan-singh-9aa715292
HuggingFace - aryansingh0404
Twitter - 
Built using Hugging Face Transformers and KeyBERT.
