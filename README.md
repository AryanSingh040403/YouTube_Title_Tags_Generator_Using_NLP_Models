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



## Setup Instructions

