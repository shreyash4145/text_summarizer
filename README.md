# Text Summarizer

![Python](https://img.shields.io/badge/Python-3.6+-blue.svg)
![NLTK](https://img.shields.io/badge/NLTK-3.5-green.svg)
![Flask](https://img.shields.io/badge/Flask-2.0-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A web-based text summarization tool that uses Natural Language Processing (NLP) to generate concise summaries from large text documents.

## Features

- Extractive text summarization using NLTK
- Web interface built with Flask
- Adjustable summary ratio (control length of summary)
- Lightweight and easy to deploy
- Supports both paragraph and article-length text

## Installation

1. Clone the repository:
```bash
git clone https://github.com/shreyash4145/text_summarizer.git
cd text_summarizer
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

3. Download NLTK data:
```python
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords')"
```

## Usage

1. Run the Flask application:
```bash
python app.py
```

2. Open your web browser and navigate to:
```
http://localhost:5000
```

3. Paste your text in the input box, adjust the summary ratio if needed, and click "Summarize"

## API Usage

You can also use the summarizer as an API:

```python
import requests

url = "http://localhost:5000/summarize"
data = {
    "text": "Your long text goes here...",
    "ratio": 0.2  # Summary ratio (0-1)
}

response = requests.post(url, json=data)
print(response.json())
```

## How It Works

The summarizer uses the following NLP techniques:

1. Sentence tokenization to split text into sentences
2. Word tokenization and frequency analysis
3. Stopword removal and punctuation cleaning
4. Sentence scoring based on word frequencies
5. Selection of top-scored sentences based on the specified ratio


## Contact

Shreyash - [@shreyash4145](https://github.com/shreyash4145)

Project Link: [https://github.com/shreyash4145/text_summarizer](https://github.com/shreyash4145/text_summarizer)
```
