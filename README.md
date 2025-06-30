# SuperEasy 100% Local RAG with Ollama + Email RAG

![LLAMA 3 2](https://github.com/user-attachments/assets/e459834b-bb99-46b0-a4c6-77516f745366)

### Setup
1. git clone https://github.com/AllAboutAI-YT/easy-local-rag.git
2. cd dir
3. pip install -r requirements.txt
4. Install Ollama (https://ollama.com/download)
5. ollama pull llama3 (etc)
6. ollama pull mxbai-embed-large
7. run upload.py (pdf, .txt, JSON)
8. run localrag.py (with query re-write)
9. run localrag_no_rewrite.py (no query re-write)

### Email RAG Setup
1. git clone https://github.com/AllAboutAI-YT/easy-local-rag.git
2. cd dir
3. pip install -r requirements.txt
4. Install Ollama (https://ollama.com/download)
5. ollama pull llama3 (etc)
6. ollama pull mxbai-embed-large
7. set YOUR email logins in .env (for gmail create app password (video))
9. python collect_emails.py to download your emails
10. python emailrag2.py to talk to your emails

### My YouTube Channel
https://youtube.com/@ankurmajumdar7383?si=qPgD5R0avnY7SMha

### What is RAG?
RAG is a way to enhance the capabilities of LLMs by combining their powerful language understanding with targeted retrieval of relevant information from external sources often with using embeddings in vector databases, leading to more accurate, trustworthy, and versatile AI-powered applications
Read More about that here - https://codingscape.com/blog/rag-101-what-is-rag-and-why-does-it-matter
![image](https://github.com/user-attachments/assets/54ced9cf-5a44-4e9a-a20b-61453e012872)

### What is Ollama?
Ollama is an open-source platform that simplifies the process of running powerful LLMs locally on your own machine, giving users more control and flexibility in their AI projects. https://www.ollama.com
