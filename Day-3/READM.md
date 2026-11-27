# 🌾 Agricultural Products AI Assistant

An AI-powered agricultural products assistant built using **Python, LangChain, and Groq LLM**. It helps customers get information about agricultural products, sample prices, and basic product-related queries through natural language conversations.

## 🚀 Project Overview

The Agricultural Products AI Assistant is designed to simplify customer interactions for agricultural product stores. Customers can ask questions about products and their sample prices in English or Telugu.

The assistant provides friendly responses, maintains conversation history, and uses predefined product information to answer customer queries.

## ✨ Features

- **AI-Powered Conversations:** Answers customer questions using Groq LLM.
- **Product Information:** Provides basic information about agricultural products.
- **Sample Price Details:** Shares predefined demonstration prices.
- **Telugu & English Support:** Responds in the customer's language.
- **Conversation Memory:** Maintains chat history during the session.
- **CSV-Based Testing:** Evaluates assistant responses using predefined test cases.
- **LangChain Integration:** Uses prompts, chains, output parsers, and agents.

## 🛠️ Technologies Used

- Python
- LangChain
- LangChain-Groq
- Groq API
- Google Colab
- CSV

## 🌱 Sample Agricultural Products & Prices

| Product | Sample Price (per kg) |
|---|---:|
| Rice | ₹60 |
| Wheat | ₹35 |
| Maize | ₹30 |
| Onion | ₹40 |
| Tomato | ₹30 |

**Note:** These prices are illustrative demonstration values, not real-time market prices. Actual prices may vary depending on market, quality, season, and location.

## 📂 Project Structure

```text
Agricultural-Products-AI-Assistant/
│
├── agricultural_products_ai_assistant.ipynb
├── tests.csv
└── README.md
```

## ⚙️ Installation & Setup

### 1. Install Required Libraries

```python
!pip install -q langchain langchain-groq
```

### 2. Configure Groq API Key

1. Visit [Groq Console](https://console.groq.com/keys).
2. Create your API key.
3. In Google Colab, open **Secrets**.
4. Add a secret named `GROQ_API_KEY`.
5. Enable notebook access to the secret.

### 3. Initialize the Groq Model

```python
from google.colab import userdata
import os
from langchain_groq import ChatGroq

os.environ["GROQ_API_KEY"] = userdata.get("GROQ_API_KEY")

llm = ChatGroq(
    model="openai/gpt-oss-20b",
    temperature=0.3
)
```

### 4. Run the Notebook

Open `agricultural_products_ai_assistant.ipynb` in Google Colab and execute the cells sequentially.

## 💬 Example Questions

```text
1. What agricultural products do you sell?
2. What is the sample price of rice?
3. What is the price of wheat?
4. Do you have maize?
5. Are these live market prices?
6. బియ్యం ధర ఎంత?
7. గోధుమల ధర ఎంత?
```

## 🧪 Testing

The project includes a CSV-based testing system to evaluate the assistant's responses.

**Test file:** `tests.csv`

The CSV contains:
- Customer questions
- Expected keywords in the assistant's responses

The testing function checks whether the expected keyword is present and displays the test results.

Example output:

```text
PASS | What is the sample price of rice?
PASS | What is the sample price of wheat?

5/5 passed (100%)
```

*Actual results depend on the model's responses.*

## 🔮 Future Enhancements

- Real-time agricultural market price integration.
- Live product availability checking.
- Database integration for product management.
- WhatsApp chatbot integration.
- Voice-based customer interaction.
- Weather-based agricultural information.

## 👨‍💻 Author

**Vinay Gadapa**

B.Tech – Computer Science and Engineering  
Specialization: Artificial Intelligence & Machine Learning

## 📜 License

This project is created for educational and demonstration purposes.
