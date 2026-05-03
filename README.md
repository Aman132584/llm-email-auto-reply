# LLM Email Auto Reply System

A Python project I built to automatically handle customer emails using AI. It reads an email, figures out what the customer is asking about, finds the relevant product, and writes back a proper reply — all without any human involvement.

## What it does

- Reads customer emails from a CSV file
- Classifies each email (product inquiry, complaint, or other)
- Extracts the product ID if mentioned in the email
- Searches for the product using exact match or semantic search (FAISS)
- Generates a professional reply using Google Gemini

## Tools and libraries used

- Google Gemini 2.5 Flash — for email classification and reply generation
- FAISS — for finding the closest product when no ID is mentioned
- Sentence Transformers — to convert text into vectors
- Pandas — for reading CSV data
- python-dotenv — to keep the API key secure

## How to run it

1. Clone the repo and open it in VS Code
2. Create a virtual environment and activate it
3. Run `pip install -r requirements.txt`
4. Create a `.env` file and add your Gemini API key like this:
GEMINI_API_KEY=your_key_here
5. Add your CSV files inside a `data/` folder
6. Run `python main.py`

## Project structure
email-auto-reply/
├── main.py
├── config.py
├── requirements.txt
├── .env
├── .gitignore
└── data/
├── products.csv
└── emails.csv

## Note
This was built as a learning project to understand how LLMs can be used in real workflows.
