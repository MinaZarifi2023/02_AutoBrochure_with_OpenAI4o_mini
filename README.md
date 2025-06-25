# 🧠 Brochure Generator Using LLMs
his project automates the creation of professional company brochures by analyzing live content from a company's website using LLMs like OpenAI's `gpt-4o-mini` and Ollama's `llama3.2`.

✅ Key Features:
1. Web Scraping: Uses BeautifulSoup to extract clean, readable text (excluding code, images, scripts, etc.) and outbound links from the landing page and subpages.

2. Smart Link Filtering: Uses a language model (GPT-4o-mini via OpenAI or LLaMA 3.2 via Ollama) to select the most relevant subpages (like "About", "Careers", etc.) to include in the brochure.

3. Content Compilation: Gathers all relevant content into a single prompt input for brochure generation.

4. Brochure Generation: Sends the collected data to an LLM, which generates a well-structured brochure in Markdown format.

5. Streaming Output (Optional): Includes optional live streaming of the output in a typewriter-style animation for better UX.

Supports both OpenAI and LLaMA pipelines for flexibility.

---

## 🚀 Use Case
Generate high-quality brochures for:
- Customers
- Investors
- Job candidates

Ideal for marketing, HR, and business development teams.

---

## 🛠 Features

- 🌐 **Website Scraping**: Extracts the company’s landing page text and key subpages.
- 🔗 **Link Relevance Detection**: Uses LLMs to identify pages like "About", "Careers", or "Company".
- 🧠 **LLM Integration**:
  - OpenAI (`gpt-4o-mini`)
  - Ollama (`llama3.2`)
- 📄 **Markdown Output**: Generates clear, readable brochures.
- 🖥 **Streaming Output**: (Optional) Live display for user-friendly interaction.

---

## 📦 Dependencies

```bash
pip install requests beautifulsoup4 openai python-dotenv
```

You also need:

- An OpenAI API Key (.env file with OPENAI_API_KEY)

- Ollama installed and running locally (for LLaMA 3.2)

---

# ⚙️ Usage

## 📌 Using OpenAI:
```bash
create_brochure("HuggingFace", "https://huggingface.co")
```

---

## 📌 Using  LLaMA 3.2:
```bash
ollama run llama3.2
create_brochure("HuggingFace", "https://huggingface.co")
```

---

## 🖋 Streamed Output
```bash
stream_brochure("HuggingFace", "https://huggingface.co")
```

---

## 🧪 Example Output
```bash
# HuggingFace Brochure

Welcome to HuggingFace — a leading AI company...

- 🤝 Partnerships with top research labs
- 💼 Careers focused on open-source innovation
- 🌍 Global community of developers
```

---
## 🧠 Prompts & Customization
You can easily change the tone (formal, fun, casual) by modifying the system_prompt in the code.


