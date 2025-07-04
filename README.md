# SuperEasy 100% Local RAG with Ollama + Email RAG

### by [@AsterioAstrixx](https://github.com/AsterioAstrixx)

![LLAMA 3 2](https://github.com/user-attachments/assets/e459834b-bb99-46b0-a4c6-77516f745366)

> Fully local. Privacy-first. Personalized AI with your own documents and emails.

---

## What is this?

A lightweight, production-ready Retrieval-Augmented Generation (RAG) pipeline:

- Uses LLAMA 3 via Ollama (fully offline)
- Supports `.pdf`, `.txt`, `.json` documents
- RAG on your personal Gmail inbox
- Includes a custom fine-tuned model (`ankur`) with Alpaca-style instruction tuning for personality-aware responses

---

## Local RAG Setup (Docs-based)

1. **Clone the repository**

   ```bash
   git clone https://github.com/AsterioAstrixx/easy-local-rag.git
   cd easy-local-rag
   ```

2. **Install Python dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Install Ollama**

   [https://ollama.com/download](https://ollama.com/download)

4. **Pull the required models**

   ```bash
   ollama pull llama3
   ollama pull mxbai-embed-large
   ```

5. **[Optional but Powerful] Create Your Own Personality-Based Model**

   - I created a model called `ankur` using a custom prompt file (Alpaca-style JSON)
   - This file describes my personality, temperature, and contextual behavior
   - Command used:

     ```bash
     ollama create ankur -f Model
     ```

   - You can customize this file and pre-inject your own context
   - In the scripts, model usage is set by:

     ```python
     parser.add_argument("--model", default="ankur", help="Ollama model to use (default: ankur)")
     ```

     Change `"ankur"` to `"llama3"` or any other model if needed.

6. **Upload your documents**

   ```bash
   python upload.py
   ```

7. **Run RAG with query rewriting**

   ```bash
   python localrag.py
   ```

8. **Run RAG without query rewriting**

   ```bash
   python localrag_no_rewrite.py
   ```

---

## Email RAG Setup

Chat with your own inbox—locally.

1. **Add your email credentials in `.env`**

   (For Gmail, use an App Password. You can find tutorials online.)

2. **Download emails**

   ```bash
   python collect_emails.py
   ```

3. **Run Email RAG**

   ```bash
   python emailrag2.py
   ```

---

## Model Customization Tips

- You can modify the model file (`Model`) in Alpaca format:

  ```json
  {
    "instruction": "You are Ankur, an empathetic and curious AI...",
    "input": "",
    "output": "Sure! Let me help you with that..."
  }
  ```

- Add multiple entries to shape how your model behaves in various scenarios.
- Once ready, run:

  ```bash
  ollama create ankur -f Model
  ```

---

## My YouTube Channel

Watch demos, dev logs, and tutorials:
[https://youtube.com/@ankurmajumdar7383?si=qPgD5R0avnY7SMha](https://youtube.com/@ankurmajumdar7383?si=qPgD5R0avnY7SMha)
