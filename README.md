# 🚀 LLM SQL Evaluation — Text-to-SQL Engine for ESPN Cricinfo

An LLM evaluation project focused on building and evaluating a Text-to-SQL system for cricket-related data. The goal is to understand how effectively Large Language Models (LLMs) translate natural-language questions into SQL queries and produce accurate database results.

The project explores model selection and task-specific evaluation using practical engineering considerations such as accuracy, latency, and inference cost.

## 🎯 Project Objectives

- Convert natural-language questions into SQL queries.
- Explore LLMs for structured data querying.
- Evaluate generated SQL using database results rather than relying only on exact SQL string matching.
- Build a Golden Dataset of representative cricket-related questions.
- Compare candidate models based on accuracy, response time, and cost.
- Understand the challenges of deploying LLM-powered applications in production.

## ✨ Key Features

- **Text-to-SQL:** Translate natural-language questions into SQL.
- **LLM Integration:** Use OpenRouter to access supported language models.
- **Custom Evaluation:** Evaluate model-generated SQL against expected database results.
- **Golden Dataset:** Use a collection of test questions to assess performance.
- **Cost-Aware Model Selection:** Consider inference costs alongside accuracy and latency.
- **Configurable API Access:** Store API credentials in environment variables.

## 🛠️ Technology Stack

- Python
- Large Language Models (LLMs)
- OpenRouter API
- SQL and relational databases
- LangChain integration
- Git and GitHub

*The exact models, database engine, and additional dependencies depend on the implementation in this repository.*

## 📋 Prerequisites

Before running the project, make sure you have:

- Python 3.12 or a compatible version.
- Git installed.
- An OpenRouter account and API key.
- The dependencies required by the project.

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/siddhant754962/llm-sql-eval.git
cd llm-sql-eval
```

### 2. Create a virtual environment

**Windows PowerShell:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, you can use the environment's Python executable directly.

### 3. Install dependencies

If the repository contains `requirements.txt`:

```powershell
python -m pip install -r requirements.txt
```

If the project uses `pyproject.toml` instead, follow its documented installation procedure.

### 4. Configure environment variables

Create a `.env` file in the project root:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
```

Replace the placeholder with your actual API key.

**Security:** Never commit `.env` or publish API keys to GitHub. Add `.env` to `.gitignore`.

### 5. Run the application

If `main.py` is the project's entry point:

```powershell
python main.py
```

Follow the instructions displayed in the terminal. Any additional database setup or dataset preparation should be completed according to the project code.

## 🔬 Evaluation Methodology

The project explores a task-specific evaluation workflow:

1. **Define requirements:** Establish budget and response-time constraints.
2. **Select candidate models:** Filter models according to cost, availability, latency, and expected performance.
3. **Prepare a Golden Dataset:** Collect representative natural-language questions and their expected database results.
4. **Generate SQL:** Ask each candidate model to translate
