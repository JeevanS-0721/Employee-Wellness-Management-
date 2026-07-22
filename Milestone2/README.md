# 🌿 Mood Mentor: Employee Wellness NLP Pipeline (Milestone 2)

**Author:** Jeevan  
**Project:** Employee Wellness Management Analytics  

## 📌 Overview
This milestone focuses on the core **Natural Language Processing (NLP) Pipeline** and the **Wellness Chatbot**. The goal of this pipeline is to take raw, messy employee feedback (like survey responses or direct messages) and transform it into clean, analyzable data to understand employee sentiment and emotional well-being. 

We built a complete, multilingual pipeline that can handle complex inputs—including mixed languages (like English and Kannada), emojis, and formatting errors—and output precise emotional analytics.

---

## ⚙️ The NLP Preprocessing Pipeline (Step-by-Step)
To get accurate analytics, employee text goes through a rigorous cleaning and analysis process:

1. **Text Normalization (`ftfy`):** Fixes broken encoding and weird characters so the text is readable by the machine.
2. **Emoji Translation (`emoji`):** Converts emojis into text (e.g., 😞 becomes "disappointed face") so the AI doesn't lose the emotional context.
3. **Language Detection & Translation (`langdetect` & `deep-translator`):** Automatically detects if the feedback is in a regional language (like Kannada) and seamlessly translates it to English for consistent processing.
4. **Data Cleaning (`re`):** Uses regular expressions to strip out unnecessary URLs, special characters, and numbers.
5. **Tokenization & Stop-word Removal (`spacy` & `stopwordsiso`):** Breaks the sentences down into individual words (tokens) and filters out common but meaningless words (like "the", "and", "is").
6. **Lemmatization (`spacy`):** Reduces words to their base root (e.g., converting "stressing" and "stressed" into simply "stress") to group similar feedback together.

---

## 🧠 AI-Powered Analysis
Once the text is completely clean, it is passed into two distinct AI models for evaluation:

* **Sentiment Analysis (`vaderSentiment`):** Scores the text to determine if the overall tone is **Positive**, **Negative**, or **Neutral**.
* **Emotion Classification (BERT):** Uses a Hugging Face Transformer model (`bhadresh-savani/bert-base-go-emotion`) to detect specific underlying emotions like *joy, sadness, anger, or stress*.

---

## 💬 The Wellness Chatbot (`Qwen2.5-0.5B-Instruct`)
Integrated into the customized green-gradient dashboard is an AI-powered Wellness Chatbot designed to provide immediate support to employees. 
* **Conversational AI:** Provides helpful, empathetic wellness tips based on user prompts.
* **Crisis Intervention Trigger:** The chatbot includes a hardcoded safety mechanism. If it detects severe distress or crisis keywords, it immediately bypasses standard responses and provides emergency intervention resources and HR contacts.

---

## 🚀 Features & Usage
The Streamlit dashboard allows for two ways to process data:
* **Direct Text Input:** For quick, real-time testing of single messages (supports mixed languages and emojis).
* **Batch File Upload:** Users can upload `.csv` or `.txt` files containing hundreds of feedback entries, and the pipeline will process all of them at once, returning visual data charts.

---

s
