# AgriFresh Order Agent 🌾

An AI agent built with **LangChain** and **Groq** that helps customers of an agricultural products store. It answers sample price questions, checks store hours, and logs confirmed orders to a **Google Sheet**.

> **Note:** All prices and opening hours are **sample demonstration values**, not live market rates.

## Features

- **Price lookup:** calculates the total for a quantity (in kg) of rice, wheat, maize, onion or tomato.
- **Store hours:** returns sample opening hours for any day of the week.
- **Order logging:** saves confirmed orders (name, product, quantity, pickup date, total) to Google Sheets.
- **Input validation:** a Pydantic `Order` model rejects unknown products and invalid quantities.
- **Conversation memory:** remembers earlier messages in the chat.
- **Bilingual replies:** answers in English or Telugu, matching the customer.
- **Safe behavior:**
  - Never invents products or prices.
  - Says "I'll check the latest rate with the seller" for anything unlisted.
  - Never promises delivery (pickup only).

## Sample Products (per kg)

| Product | Price (Rs) |
|---------|-----------|
| Rice    | 60 |
| Wheat   | 35 |
| Maize   | 30 |
| Onion   | 40 |
| Tomato  | 30 |

## Tech Stack

- Python 3
- [LangChain](https://python.langchain.com/) (`create_agent`, tools)
- [Groq](https://groq.com/) via `langchain-groq` (model: `openai/gpt-oss-20b`)
- [gspread](https://docs.gspread.org/) for Google Sheets
- Pydantic for order validation
- Google Colab (notebook environment)

## How It Works

```
Customer message
      │
      ▼
  LangChain Agent (Groq LLM + system prompt)
      │  decides which tool to call
      ├── get_price(product, qty_kg)   → total price
      ├── is_open(day)                 → opening hours
      └── log_order(name, product,     → validates with Pydantic,
                    qty_kg, date)        saves row to Google Sheet
      │
      ▼
 Friendly reply (under 60 words)
```

## Setup

1. **Get a Groq API key** from [console.groq.com](https://console.groq.com/).
2. Open `task_4_agriculture.ipynb` in **Google Colab**.
3. Add your key as a Colab secret named `GROQ_API_KEY` (key icon in the left sidebar) and enable notebook access.
4. Run the cells in order. When prompted, sign in with your Google account so the agent can create and write to the "AgriFresh Orders" sheet.

## Usage

Call the `chat()` function:

```python
print(chat("Are you open on friday? How much are 5 kg of rice?"))
print(chat("I'm Siddu. Please order 3 kg onion for 6 Dec at 10 am."))
print(chat("What products do you have?"))
print(chat("Do you have mangoes?"))
```

Confirmed orders appear as new rows in the Google Sheet:

| name | product | qty_kg | pickup_date | total |
|------|---------|--------|-------------|-------|
| Siddu | onion | 3 | 6 Dec at 10 am | 120 |

## Project Structure

```
.
├── task_4_agriculture.ipynb   # Agent notebook (setup, tools, agent, chat)
└── README.md
```

## Security

- Never commit your `GROQ_API_KEY` or Google credentials. Keep them in Colab Secrets.
- Clear notebook outputs before pushing if they contain private sheet links.


## License

This project is for learning and demonstration purposes.
