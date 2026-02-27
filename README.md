# paper-summarizer

A local AI-powered research paper summarizer.

Paste any research paper URL and receive a clean, structured Markdown summary — including title, authors, methodology, technologies, references, research gaps, and key findings — all generated locally using Ollama.

---

## Overview

This project extracts the full content of a research paper from a URL using the Jina AI Reader API and sends it to a locally running LLM via Ollama. The model processes the content and returns a well-structured Markdown summary.

---

## How It Works

1. A research paper URL is passed to the Jina AI Reader API.
2. The full page content is extracted.
3. The extracted content is sent to a local `llama3.2:3b` model running via Ollama.
4. The model generates a structured Markdown summary.
5. The result is rendered using `IPython.display.Markdown`.

---

## Installation

### Prerequisites

- Python 3.10 or higher
- Ollama installed and running locally
- A Jina AI API key (free tier available)

### Clone the Repository

```bash
git clone https://github.com/Karam-999/paperSuMMARiZER.git
cd paperSuMMARiZER
```

### Create Virtual Environment

```bash
python -m venv .venv
```

Activate the environment:

Windows:

```bash
.venv\Scripts\activate
```

macOS / Linux:

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Pull Required Model

Make sure Ollama is running:

```bash
ollama pull llama3.2:3b
```

### Configure API Key

Create a `.env` file in the project root and add:

```
JINA_API_KEY=your_jina_api_key_here
```

---

## Usage

Open the notebook:

```
paperSUMMARiZER.ipynb
```

Inside the notebook, set your target research paper URL:

```python
paper_url = "https://your-research-paper-url-here"
display_summary(paper_url)
```

Run all cells to generate the structured summary.

---

## Example Output Structure

The generated output includes:

- Title
- Abstract
- Introduction
- Methods
- Key Technologies
- Results
- Discussion
- Research Gaps
- References
- Structured comparison tables (if applicable)

---

## Tech Stack

- LLM: llama3.2:3b via Ollama
- Web Extraction: Jina AI Reader API
- Environment: Python
- Interface: Jupyter Notebook
- Rendering: IPython.display.Markdown

---

## Future Improvements

- Support direct PDF upload
- Add batch processing of multiple URLs
- Export summaries to Markdown or PDF
- Add a simple web interface

---

## License

MIT License
