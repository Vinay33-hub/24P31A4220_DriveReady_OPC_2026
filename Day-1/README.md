# 🍰 AI Bakery Assistant – Sweet Crumbs Home Bakery

An AI-powered customer support assistant built using **LangChain, Groq API, and LLM technology** to handle customer queries for Sweet Crumbs Home Bakery.

The assistant provides polite, concise, and context-aware responses while following predefined business rules. It also explores prompt-injection detection using Meta's Llama Prompt Guard.

## 🚀 Project Overview

The AI Bakery Assistant is designed to simulate a virtual customer support representative for a home bakery. It helps customers get information about bakery services, ordering requirements, eggless cake availability, and other bakery-related queries.

## ✨ Key Features

- **AI-Powered Conversations:** Generates natural-language responses using Groq-hosted LLMs.
- **LangChain Integration:** Uses LangChain's ChatGroq interface for LLM communication.
- **Custom System Instructions:** Configured with bakery-specific information and response guidelines.
- **Order Information:** Informs customers about the 24-hour advance ordering requirement.
- **Eggless Options:** Provides information about eggless versions of all cakes.
- **Controlled Responses:** Maintains polite responses within 60 words.
- **Prompt Injection Detection:** Integrates Llama Prompt Guard to explore detection of potentially malicious instructions.
- **Secure API Configuration:** Retrieves the Groq API key through Google Colab Secrets.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | LLM integration framework |
| Groq API | LLM inference |
| GPT-OSS-120B | Conversational AI model |
| Llama Prompt Guard 2 | Prompt-injection detection |
| Google Colab | Development environment |

## ⚙️ How It Works

1. The customer submits a question.
2. The question is passed to the LangChain-powered assistant.
3. The system instructions provide bakery-specific context.
4. The Groq-hosted language model processes the query.
5. The assistant generates a polite response following the configured rules.
6. Llama Prompt Guard is separately invoked to examine a potentially unsafe prompt.

## 📂 Project Structure

```text
AI-Bakery-Assistant/
│
├── task_1.py
├── README.md
└── requirements.txt
```

## 🔧 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/AI-Bakery-Assistant.git
```

### 2. Install Dependencies

```bash
pip install langchain-groq groq
```

### 3. Configure Groq API Key

Get your API key from [Groq Console](https://console.groq.com/).

For Google Colab:
- Open the Secrets tab.
- Add a secret named `Groq_API`.
- Paste your Groq API key.
- Enable notebook access to the secret.

### 4. Run the Project

Open `task_1.py` in Google Colab and execute the cells.

## 💡 Example Customer Queries

```python
ask("What is the cost of cupcakes?")
ask("How far is your bakery from my place?")
ask("Give me all the information about your bakery.")
```

**Note:** The current implementation does not contain actual pricing, location, or complete bakery information. The assistant should communicate when such information is unavailable rather than inventing answers.

## 🔐 Security & Responsible AI

This project demonstrates the use of system instructions and Llama Prompt Guard for exploring prompt-injection detection.

The Prompt Guard component is currently a separate model invocation and is not yet integrated into the main customer-query pipeline.

## 🎯 Project Objectives

- Understand practical LLM integration using Groq.
- Explore LangChain for conversational AI development.
- Implement custom system prompts.
- Understand prompt-injection risks.
- Build a practical AI-powered customer support application.

## 🔮 Future Enhancements

- Integrate a real bakery product and pricing database.
- Add order placement and tracking functionality.
- Implement a complete prompt-injection protection pipeline.
- Build a Streamlit-based chatbot interface.
- Add conversation memory.
- Integrate WhatsApp customer support.

## 👨‍💻 Author

**Vinay Gadapa**

B.Tech – Computer Science and Engineering  
Specialization: Artificial Intelligence & Machine Learning

---

⭐ If you find this project interesting, consider giving this repository a star!
