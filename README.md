# Brochure Generator Using LLMs

This project automates the creation of company brochures by analyzing live content from a company's website using language models such as OpenAI’s `gpt-4o-mini` and Ollama’s `llama3.2`.

## Features

- **Web Scraping**: Extracts clean, readable text and outbound links from the landing page and subpages using BeautifulSoup.
- **Link Filtering**: Uses a language model to identify relevant subpages (e.g., "About", "Careers") for brochure content.
- **Content Aggregation**: Compiles selected content into a single input prompt.
- **Brochure Generation**: Sends compiled data to an LLM, which returns a structured brochure in Markdown format.
- **Streaming Output (optional)**: Provides live output in a typewriter-style display.

Supports both OpenAI and Ollama-based pipelines.

## Use Cases

Generate brochures for:
- Customers
- Investors
- Job candidates

Useful for marketing, HR, and business development.

## Installation

```bash
pip install requests beautifulsoup4 openai python-dotenv
```

## Requirements

- OpenAI API key (`.env` file with `OPENAI_API_KEY`)
- Ollama installed and running locally (for `llama3.2`)

## Usage

### Using OpenAI
```python
create_brochure("HuggingFace", "https://huggingface.co")
```

---

## Using  LLaMA 3.2:
```bash
ollama run llama3.2
create_brochure("HuggingFace", "https://huggingface.co")
```

---

## With Streaming Output
```bash
stream_brochure("HuggingFace", "https://huggingface.co")
```

---

## Example Output
```bash
# HuggingFace Brochure

Welcome to HuggingFace — a leading AI company...

-  Partnerships with top research labs
-  Careers focused on open-source innovation
-  Global community of developers
```

---
## Prompts & Customization
You can easily change the tone (formal, fun, casual) by modifying the system_prompt in the code.


