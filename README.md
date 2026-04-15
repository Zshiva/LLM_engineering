# LLM & Automation Projects (Python)

A collection of small, practical projects exploring LLM integration (Gemini / OpenAI-compatible APIs), local LLMs via Ollama, web scraping, and simple UIs (Gradio / widgets) — built as portfolio-ready demos.

## Projects

### Chatbot Assistant (Gemini + Gradio)
- Notebook: [Chatbot_Assistant/conversational_ai.ipynb](Chatbot_Assistant/conversational_ai.ipynb)
- What it does: Experiments with a conversational assistant UI using Gradio ChatInterface, calling Gemini via the OpenAI-compatible endpoint.
- Requirements: `GOOGLE_API_KEY`

### Cover Letter Generator (CV + Job Description)
- Notebook: [CoverLetterGenerator/coverlettergeneratorfromcv.ipynb](CoverLetterGenerator/coverlettergeneratorfromcv.ipynb)
- What it does: Fetches a job posting from a URL, compares it with a CV, then generates a short professional cover letter (and fit summary).
- UI: Uses Jupyter widgets for inputs (URL, CV upload/text).
- Default model setup: local Ollama OpenAI-compatible endpoint.

### Gemini Connection (API Experiments)
- Notebook: [Frontier_Connection_Gemini/gemini_connection.ipynb](Frontier_Connection_Gemini/gemini_connection.ipynb)
- What it does: Quick experiments calling Gemini models (OpenAI-compatible client) and rendering responses.
- Requirements: `GOOGLE_API_KEY`

### Gradio UI (Gemini + Simple Apps)
- Notebook: [Frontier_Connection_Gemini/gradio_ui.ipynb](Frontier_Connection_Gemini/gradio_ui.ipynb)
- What it does: Builds small Gradio demos and connects them to Gemini calls.
- Requirements: `GOOGLE_API_KEY`

### Sales Brochure Generator (Scrape → Select Links → Brochure)
- Notebook: [Sales_Brochure_Generator/brochure_generator.ipynb](Sales_Brochure_Generator/brochure_generator.ipynb)
- What it does:
	- Scrapes a company site
	- Selects relevant pages (about/careers/etc.) using an LLM
	- Builds a brochure-style markdown output
- Notes: Imports shared scraping utilities from [scraper.py](scraper.py) and uses Ollama by default.

### Web Scraper + Summarizer
- Notebook: [WebScrapper/webscrapping.ipynb](WebScrapper/webscrapping.ipynb)
- What it does: Scrapes a web page and summarizes/answers based on its contents using an LLM.

## Shared Utilities

- [scraper.py](scraper.py): Reusable scraping helpers (page text + links) built with `requests` + `beautifulsoup4`.
- [requirements.txt](requirements.txt): Python dependencies used across notebooks.

## Setup

### 1) Install dependencies

```bash
pip install -r requirements.txt
```

### 2) (Optional) Gemini API key

Some notebooks use Gemini via the OpenAI-compatible endpoint and expect an environment variable:

- `GOOGLE_API_KEY`

If you are using a `.env` file, create one at the repo root and add:

```env
GOOGLE_API_KEY=your_key_here
```

### 3) (Optional) Ollama (local LLM)

Some notebooks default to a local OpenAI-compatible endpoint:

- Base URL: `http://localhost:11434/v1`

Install and run Ollama, then ensure the referenced model is available (for example, `llama3.2`).

## How to Run

- Open any notebook (`.ipynb`) in VS Code and run cells in order.
- If you see missing package errors, re-run the dependency install step.
