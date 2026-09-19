# Kartify Customer Support

AI-powered customer support assistant for order queries, built with Streamlit, LangGraph, and GPT-4o.

## Setup

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Configure API credentials

The app reads its OpenAI API key and base URL from Streamlit's secrets file. Create the file at `~/.streamlit/secrets.toml`:

```bash
mkdir -p ~/.streamlit
touch ~/.streamlit/secrets.toml
```

Add the following content, replacing the placeholders with your actual values:

(When deploying to StreamLit, enter these lines in the "secrets" section)

```toml
OPENAI_API_KEY = "sk-..."
OPENAI_API_BASE = "https://your-api-base-url"
```

- **`OPENAI_API_KEY`** — Your OpenAI (or compatible) API key.
- **`OPENAI_API_BASE`** — The base URL for the API endpoint (e.g. an Azure deployment or a custom proxy).

> **Note:** Never commit `secrets.toml` to version control. It is excluded via `.gitignore` by default when placed outside the project directory (`~/.streamlit/`).

## Running the app

```bash
streamlit run app.py
```
