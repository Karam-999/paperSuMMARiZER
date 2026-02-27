# paperSuMMARiZER

A local AI-powered research paper summarizer.

Paste any research paper URL and receive a clean, structured Markdown summary including title, authors, methodology, technologies, references, research gaps, and key findings, all generated locally using Ollama.

---

## Overview

This project extracts the full content of a research paper from a URL using the Jina AI Reader API and sends it to a locally running LLM via Ollama. The model processes the content and returns a well-structured Markdown summary.

## How It Works

1. A research paper URL is passed to the Jina AI Reader API.
2. The full page content is extracted using Jina ai.
3. The extracted content is sent to a local `llama3.2:3b` model running via Ollama.
4. The model generates a structured Markdown summary.


---



#### Example Output Structure

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

#### Tech Stack

- LLM: llama3.2:3b via Ollama
- Web Extraction: Jina AI Reader API
- Environment: Python
- Interface: Jupyter Notebook
- Rendering: IPython.display.Markdown

---

#### Future Improvements

- Support direct PDF upload
- Add batch processing of multiple URLs
- Improved speed
- Export summaries to PDF
- Add a simple web interface


---
### More Info

For installation instructions and additional information, visit my contribution [here](https://github.com/ed-donner/llm_engineering/tree/main/community-contributions/karam_sayed/paper-summarizer).

---
### Author
Developed by [Karam Sayed](https://github.com/Karam-999)

---

### License
MIT License
