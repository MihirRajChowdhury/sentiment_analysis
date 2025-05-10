# 🗳️ Sentiment & Political Tendency Classifier using LLaMA 3 + Groq

This project uses **LLaMA 3.1 (8B-Instant)** from [Groq](https://groq.com/) with LangChain and Pydantic to perform structured classification of text passages. It extracts **sentiment**, **political inclination**, and **language** from user opinions using a custom schema.

---

## 🧠 Features

- 🧾 Schema-based structured output using `pydantic`
- 💬 LLaMA 3 via Groq for fast inference
- 🔍 Custom extraction of:
  - **Sentiment** (hard, soft, enjoy)
  - **Political Tendency** (With Trump, With Biden, With No one)
  - **Language** (Hindi, Urdu)
- ✅ Consistent JSON-style outputs

---

## 🧰 Tech Stack

- Python 3.10+
- LangChain
- Groq API
- LLaMA 3.1 (8B-Instant)
- Pydantic for typed schema output
- dotenv for environment configuration

---

## 📁 Project Structure

```bash
.
├── main.py             # Main script for classification
├── .env                # Stores your Groq API key
