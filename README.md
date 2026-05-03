# LLM Email Auto Reply System

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python)
![Gemini](https://img.shields.io/badge/Google%20Gemini-2.5%20Flash-orange?style=flat&logo=google)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-green?style=flat)
![Learning Project](https://img.shields.io/badge/Project-Learning-purple?style=flat)

A Python project I built to automatically handle customer emails using AI. It reads an email, figures out what the customer is asking about, finds the relevant product, and writes back a proper reply — all without any human involvement.

---

## What it does

- Reads customer emails from a CSV file
- Classifies each email as a **product inquiry**, **complaint**, or **other**
- Extracts the **Product ID** if mentioned in the email
- Searches for the product using exact match or **semantic search (FAISS)**
- Generates a professional reply for each email type — inquiry, complaint, or general message — using Google Gemini

---

## Tools and libraries used

| Library | Purpose |
|---|---|
| Google Gemini 2.5 Flash | Email classification and reply generation |
| FAISS | Finding the closest product when no ID is mentioned |
| Sentence Transformers | Converting text into vectors |
| Pandas | Reading CSV data |
| python-dotenv | Keeping the API key secure |

---

## How to run it

**1. Clone the repo**
```bash
git clone https://github.com/Aman132584/llm-email-auto-reply.git
cd llm-email-auto-reply
```

**2. Create and activate a virtual environment**
```bash
python -m venv venv
venv\Scripts\activate
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Add your API key**

Create a `.env` file in the root folder and add:
Get a free key at [aistudio.google.com](https://aistudio.google.com/app/apikey)

**5. Add your data files**

Place your CSV files inside a `data/` folder:
- `data/products.csv`
- `data/emails.csv`

**6. Run**
```bash
python main.py
```

---

## Project structure
```
llm-email-auto-reply/
│
├── main.py              # main pipeline
├── config.py            # loads environment variables  
├── requirements.txt     # all dependencies
├── .gitignore
│
└── data/
    ├── products.csv     # product database
    └── emails.csv       # input emails
```

## Note

This was built as a learning project to understand how LLMs can be used in real workflows. It can be improved!
