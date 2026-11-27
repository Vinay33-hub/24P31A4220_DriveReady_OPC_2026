# 🍰 Sweet Crumbs – AI Bakery Chatbot

An intelligent, LLM-powered bakery chatbot built using Python, Groq API, and LangChain. Designed to automate customer interactions, answer bakery-related queries, provide menu information, calculate order prices, and maintain conversational context.

---

## 🚀 Project Overview

**Sweet Crumbs AI Bakery Chatbot** is a conversational AI assistant developed for Sweet Crumbs Home Bakery.

The chatbot uses Large Language Models (LLMs) to understand customer queries and generate friendly, context-aware responses. It follows predefined business instructions, provides accurate menu information, and maintains conversation history to improve customer interactions.

The project also explores prompt security using Meta Llama Prompt Guard to identify potentially malicious prompts.

## ✨ Key Features

- 🤖 **AI-Powered Conversations:** Generates natural responses using Groq-powered LLMs.
- 🧠 **Prompt Engineering:** Uses structured system prompts to control chatbot behavior.
- 💬 **Conversational Memory:** Maintains customer interactions using conversation history.
- 🍰 **Menu Information:** Provides bakery products and their prices.
- 💰 **Price Calculation:** Calculates total prices based on products and quantities.
- 🛡️ **Prompt Security:** Experiments with Meta Llama Prompt Guard for prompt injection detection.
- 🌐 **Multilingual Responses:** Supports English and Telugu response instructions.
- 📋 **Business Rule Enforcement:** Follows bakery policies, including 24-hour advance ordering and eggless cake availability.
- ⚡ **Error Handling:** Handles API rate limits and connection failures.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Groq API | LLM inference |
| LangChain | LLM integration |
| GPT-OSS-120B | Conversational AI |
| GPT-OSS-20B | Chatbot implementation |
| Llama Prompt Guard 2 | Prompt security testing |
| Google Colab | Development environment |

## 🏗️ Project Architecture

```text
             Customer
                 |
                 v
          User Query Input
                 |
                 v
          Prompt Engineering
                 |
                 v
          Conversation History
                 |
                 v
             Groq API
                 |
                 v
            LLM Model
                 |
          +------+------+
          |             |
          v             v
     AI Response   Price Calculator
          |             |
          +------+------+
                 |
                 v
          Customer Response
```

## 📂 Project Structure

```text
Sweet-Crumbs-AI-Chatbot/
│
├── task_2.ipynb       # Main project notebook
│
└── README.md          # Project documentation
```

## 🍰 Bakery Menu

The chatbot is configured with the following sample menu:

| Product | Price |
|---|---:|
| Plum Cake | ₹500 |
| Chocolate Cake | ₹650 |
| Cupcake | ₹80 |

**Business Rules:**
- Orders require at least 24 hours' advance notice.
- All cakes have eggless versions.
- Delivery times are not promised without confirmation.

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Sweet-Crumbs-AI-Chatbot.git
```

### 2. Navigate to the Project Directory

```bash
cd Sweet-Crumbs-AI-Chatbot
```

### 3. Install Dependencies

```bash
pip install langchain-groq groq openai
```

### 4. Configure Groq API Key

1. Visit [Groq Console](https://console.groq.com/).
2. Create an account and generate an API key.
3. Open Google Colab.
4. Navigate to the Secrets section.
5. Add a secret named `GROQ_API_KEY`.
6. Enable notebook access to the secret.

**Important:** Never upload your API key or other sensitive credentials to GitHub.

### 5. Run the Project

Open `task_2.ipynb` using Google Colab and execute the notebook cells sequentially.

## 💻 Sample Interaction

**Example 1: Greeting**

```text
You: Hi

Bot: Hello! I'm from Sweet Crumbs Home Bakery.
May I know your name and what cake you'd like?
```

**Example 2: Bakery Menu**

```text
You: Can you show me the menu?

Bot:
- Plum Cake – ₹500
- Chocolate Cake – ₹650
- Cupcake – ₹80

All cakes have eggless versions.
Orders require 24-hour notice.
```

**Example 3: Price Calculation**

```text
You: What is the price of 6 cupcakes?

Bot: Total for 6 cupcakes: ₹480
```

**Example 4: Business Rules**

```text
You: Can I get my order in 5 hours?

Bot: We bake each cake to order and require
at least 24 hours' notice.
```

## 🧠 Concepts Demonstrated

- Large Language Models (LLMs)
- Generative AI
- Prompt Engineering
- Conversational AI
- Prompt Injection Detection
- API Integration
- Conversation History Management
- Python Function Decorators
- Exception Handling
- Basic Business Logic Implementation

## 🔮 Future Enhancements

- Integrate automatic LLM tool calling for price calculations.
- Develop a web-based chatbot interface.
- Integrate WhatsApp customer support.
- Implement database integration for customer orders.
- Add online ordering and payment functionality.
- Improve prompt injection detection and security.
- Add customer order tracking.

## 🎯 Project Objective

The primary objective is to demonstrate how Generative AI and Large Language Models can be applied to real-world business scenarios to automate customer interactions and improve customer support.

## 👨‍💻 Author

**Vinay Gadapa**

B.Tech – Computer Science and Engineering  
Specialization: Artificial Intelligence & Machine Learning

- Project: Sweet Crumbs – AI Bakery Chatbot

---

## ⭐ Support

If you find this project interesting, consider giving this repository a ⭐ star.

**Built with Python, Generative AI, and Groq.**
