# FAQ Chatbot 🤖

An intelligent FAQ chatbot that answers customer questions by matching user 
queries to the most relevant FAQ using natural language processing techniques.

## Overview
This chatbot uses **TF-IDF vectorization** and **cosine similarity** to understand 
user questions and retrieve the best-matching answer from a curated FAQ dataset — 
no external API or paid LLM required. Built entirely with classic NLP techniques 
to demonstrate how retrieval-based chatbots work under the hood.

## Features
- 📚 Custom FAQ dataset covering 6 categories: order tracking, cancellations, 
  returns/refunds, payments, account/security, and product availability
- 🔍 Text preprocessing and vectorization using **NLTK**
- 🎯 Query matching via **TF-IDF** + **cosine similarity**
- 💬 Interactive web interface built with **Streamlit**

## Tech Stack
- Python
- NLTK
- scikit-learn (TF-IDF, cosine similarity)
- Streamlit

## How It Works
1. User types a question into the chat interface
2. The query is preprocessed (tokenized, cleaned) using NLTK
3. TF-IDF vectorizes both the query and the FAQ dataset
4. Cosine similarity finds the closest matching FAQ
5. The chatbot returns the most relevant answer

## Getting Started
```bash
git clone <your-repo-url>
cd faq-chatbot
pip install -r requirements.txt
streamlit run app.py
```

## Dataset
The FAQ dataset (`faq_data.csv`) contains 20 curated question-answer pairs 
across common customer service categories.

## Future Improvements
- Expand the FAQ dataset with more categories
- Add fuzzy matching for typo tolerance
- Experiment with sentence embeddings (e.g., BERT) for better semantic matching
