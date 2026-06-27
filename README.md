# 📄 PDF RAG Chatbot using LangChain, ChromaDB & Google Gemini

> A beginner-friendly Retrieval-Augmented Generation (RAG) project that demonstrates how Large Language Models can answer questions from PDF documents using semantic search instead of relying solely on their pre-trained knowledge.

---

# 🚀 Demo Architecture

> Replace the placeholder below with your generated architecture image.

```markdown
<p align="center">
  <img src="assets/rag_architecture.png" alt="RAG Pipeline Architecture" width="100%">
</p>
```

---

# ✨ Features

* 📄 PDF Document Processing
* ✂️ Intelligent Text Chunking
* 🧠 Gemini Embeddings
* 🗂️ ChromaDB Vector Store
* 🔍 Semantic Similarity Search
* 🤖 Context-aware Answers using Gemini 3.1 Flash Lite
* ⚡ Built with LangChain
* 🔐 Environment Variable Support
* 📓 Interactive Jupyter Notebook

---

# 🏗️ How It Works

```text
                PDF Document
                     │
                     ▼
             Load PDF Content
                     │
                     ▼
      RecursiveCharacterTextSplitter
                     │
                     ▼
          Create Overlapping Chunks
                     │
                     ▼
      Gemini Embedding Model (Embedding-001)
                     │
                     ▼
         Store Embeddings in ChromaDB
──────────────────────────────────────────────
             User asks a Question
                     │
                     ▼
          Embed User Question
                     │
                     ▼
       Chroma Similarity Search (Top-K)
                     │
                     ▼
      Retrieve Relevant Document Chunks
                     │
                     ▼
      Gemini 3.1 Flash Lite LLM
                     │
                     ▼
      Context-Aware Grounded Response
```

---

# 🛠️ Tech Stack

| Category        | Technology                     |
| --------------- | ------------------------------ |
| Language        | Python                         |
| Framework       | LangChain                      |
| LLM             | Gemini 3.1 Flash Lite          |
| Embeddings      | Gemini Embedding-001           |
| Vector Database | ChromaDB                       |
| Chunking        | RecursiveCharacterTextSplitter |
| Environment     | python-dotenv                  |
| Package Manager | uv                             |
| Development     | Jupyter Notebook               |

---

# 📂 Project Structure

```text
.
├── chroma_db/
├── docs/
├── .env.example
├── .gitignore
├── .python-version
├── 1.0_Rag_with_own_text.ipynb
├── 2.0_Rag_with_PDF.ipynb
├── main.py
├── pyproject.toml
├── uv.lock
└── README.md
```

---

# ⚙️ Installation

## Clone the Repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git

cd <repository-name>
```

## Install Dependencies

```bash
pip install uv
```

```bash
uv sync
```

## Activate Virtual Environment

### Windows

```bash
.venv\Scripts\activate
```

### Linux / macOS

```bash
source .venv/bin/activate
```

---

# 🔑 Environment Variables

Create a `.env` file in the project root. Take a look at .env.example

```env
GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
```

You can obtain your API key from **Google AI Studio**.

---

# ▶️ Running the Project

Launch Jupyter Notebook

```bash
jupyter notebook
```

or

```bash
jupyter lab
```

Open and execute the notebooks sequentially.

* **1.0_Rag_with_own_text.ipynb** — Learn the fundamentals of RAG using a simple text document.
* **2.0_Rag_with_PDF.ipynb** — Build a complete PDF-based Retrieval-Augmented Generation pipeline.

---

# 🧠 Understanding the RAG Pipeline

### Step 1 — Load Documents

The PDF is loaded and converted into text.

### Step 2 — Split into Chunks

Large documents are divided into smaller overlapping chunks using `RecursiveCharacterTextSplitter`.

### Step 3 — Generate Embeddings

Each chunk is converted into a dense vector representation using **Gemini Embedding-001**.

### Step 4 — Store in ChromaDB

The embeddings and document metadata are stored in ChromaDB for efficient similarity search.

### Step 5 — User Query

The user's question is embedded using the same embedding model.

### Step 6 — Semantic Retrieval

ChromaDB retrieves the most semantically relevant chunks.

### Step 7 — Response Generation

The retrieved context is passed to **Gemini 3.1 Flash Lite**, which generates a grounded answer.

---

# 📈 Future Improvements

* 🌐 Streamlit Web Application
* 📚 Multiple PDF Support
* 📄 Source Citations
* 💬 Conversational Memory
* ⚡ Streaming Responses
* 🔍 Hybrid Search
* 📊 Similarity Scores
* 🧠 Reranking
* 🐳 Docker Support
* ☁️ Cloud Deployment

---

# 🤝 Contributing

Contributions, suggestions, and improvements are always welcome.

Feel free to fork the repository and open a pull request.

---

# ⭐ Support

If you found this project helpful, consider giving it a **⭐** on GitHub.

It helps others discover the project and encourages future development.

---

# 📬 Connect With Me

If you'd like to discuss AI, RAG systems, or GenAI, feel free to connect with me on LinkedIn.

Happy Building! 🚀
