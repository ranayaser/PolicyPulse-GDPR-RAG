# PolicyPulse-GDPR-RAG
# ⚖️ PolicyPulse — GDPR RAG Assistant

PolicyPulse is a Retrieval-Augmented Generation (RAG) application designed to analyze GDPR documents using Large Language Models (LLMs).

The system allows users to upload GDPR PDF files, retrieve semantically relevant text chunks, generate context-grounded answers, and validate response reliability using an integrated verification system.

---

# 🚀 Features

- 📄 Upload GDPR PDF documents
- 🔍 Semantic retrieval using Cosine Similarity
- 🧠 Context-aware answer generation with RAG
- 🧩 Token-based chunking for better context handling
- 🚫 Duplicate chunk filtering
- ✅ Intelligent response validation system
- 🎨 Interactive Gradio interface

---

# ✅ Verification System

The application validates generated responses using a fact-checking pipeline with 3 possible outcomes:

### VERIFIED
The generated answer is fully supported by the retrieved GDPR text.

### WARNING
Possible hallucinated or unsupported information detected.

### NOT FOUND
No strongly relevant GDPR text was retrieved.

---

# 🛠️ Tech Stack

- Python
- LangChain
- ChromaDB
- HuggingFace Embeddings
- Groq LLM
- Gradio

---

# ⚙️ How It Works

1. Upload a GDPR PDF file
2. Extract and split document text into chunks
3. Generate embeddings using HuggingFace
4. Store embeddings in ChromaDB
5. Retrieve the most semantically similar chunks
6. Generate answers using Groq LLM
7. Validate the generated response using fact checking
8. Display retrieved chunks with cosine similarity scores

---

# 🔐 Environment Variables

For security reasons, do NOT hardcode API keys directly inside the source code.

Use environment variables instead:

```python
import os
GROQ_API_KEY = os.getenv("GROQ_API_KEY")
```

Example for Google Colab:

```python
from google.colab import userdata
import os

os.environ["GROQ_API_KEY"] = userdata.get("GROQ_API_KEY")
```

---

# 📦 Installation


## Install dependencies

```bash
!pip install -qU langchain langchain-groq langchain-community langchain-text-splitters langchain-huggingface chromadb pypdf sentence-transformers gradio
```

---

# ▶️ Run the Application

```bash
python app.py
```

---

# Example Workflow

📄 Upload GDPR PDF  
⬇️  
🔍 Retrieve Relevant Chunks  
⬇️  
💡 Generate Answer  
⬇️  
✅ Validate Response Reliability

---

# 🧠 Retrieval Strategy

The retriever uses:

- Cosine Similarity
- Top-k semantic search
- Similarity threshold filtering
- Duplicate chunk removal

This helps improve retrieval quality and reduce irrelevant context.

---

# 📋 Output Includes

- Final generated answer
- Verification status
- Retrieved chunks
- Chunk IDs
- Page numbers
- Cosine similarity scores

---

# 👥 Team Members

- Ahmed El-Mokaddem (https://github.com/elmokademahmed35-netizen)
- Rahaf Ehab (https://github.com/RahafEA)
- Mahmoud khamis (https://github.com/Mahmoud70-7)
- Badr Ahmed (https://github.com/BadrWaqas)
- Hazem Mahmoud (https://github.com/Haz3m-m7hmoud)


---

# 🙏 Acknowledgment

Special thanks to our instructor Eng.Tawadros Nemer for the continuous support and guidance throughout the project.
