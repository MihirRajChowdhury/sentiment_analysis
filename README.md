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
    ```
    ├── main.py             # Main script for classification
    ├── .env                # Stores your Groq API key
    🔑 Environment Setup
    Create a .env file:
    
    GROQ_API_KEY=your_groq_api_key
    Install dependencies:
    
    
    pip install langchain langchain-core langchain-community langchain-groq pydantic python-dotenv
    🚀 How It Works
    Loads the GROQ_API_KEY securely from .env.

    Defines a prompt and structured schema using pydantic.
    
    Sends user input through LangChain and receives structured classification.
    
    Outputs include sentiment, political leaning, and language.

## 🔍 Example Output

response = tagging_chain.invoke({"input": "I'm confident that President Trump's leadership will resonate with Americans..."})
print(response)
Sample Output:


{
  "sentiment": "hard",
  "political_tendency": "With trump",
  "language": "Hindi"
}

## 📌 TODOs
 Expand schema to include emotion detection

 Add multilingual support

 Create Streamlit UI for live input

 Connect to social media streams for real-time sentiment

## ⚠️ Notes
Make sure the enums in the Classification model exactly match expected model outputs.

Pydantic's validation ensures responses are well-formed and error-prone cases are caught early.

## 🤝 Contributing
Pull requests and suggestions are welcome!

## 📄 License
MIT License.
