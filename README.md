# DeepCite 📚🔍

**AI-powered academic research assistant that answers questions from your own documents — with citations.**

DeepCite is a Retrieval-Augmented Generation (RAG) system that lets you upload academic PDFs and ask natural language questions. Instead of hallucinated answers, you get responses grounded in your actual documents, with source references included.

## 🎥 Demo

▶️ [Watch the demo on YouTube](https://youtu.be/8-tA-PktphE?si=KjlCQCOSSPQN0SRk)
---

## ✨ Features

- 📄 **PDF Ingestion** — Upload one or multiple research papers and process them instantly
- 🔎 **Semantic Search** — Finds the most relevant passages using vector similarity, not just keyword matching
- 🤖 **LLM-Powered Answers** — Generates clear, concise responses using Google Gemini 1.5 Flash
- 📌 **Source Attribution** — Every answer is backed by citations from the source document
- 🧠 **Persistent Vector Store** — ChromaDB stores embeddings locally so you don't re-process documents every session
- 🖥️ **Clean Streamlit UI** — Simple, intuitive interface — no setup complexity for end users

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Framework | LangChain (LCEL) |
| LLM | Google Gemini 1.5 Flash |
| Vector Store | ChromaDB |
| PDF Parsing | PyMuPDF (fitz) |
| Frontend | Streamlit |
| Language | Python 3.10+ |

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/AimenSaeed/DeepCite.git
cd deepcite
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up your API key

Create a `.env` file in the root directory:
Get your free API key from [Google AI Studio](https://aistudio.google.com/).

### 5. Run the app
```bash
streamlit run app.py
```

---

## 📁 Project Structure
deepcite/
│
├── app.py                  # Streamlit frontend
├── rag_pipeline.py         # Core RAG logic (LangChain LCEL chain)
├── pdf_processor.py        # PDF loading and chunking (PyMuPDF)
├── vector_store.py         # ChromaDB setup and retrieval
├── requirements.txt
├── .env.example
└── README.md
---

## 💡 How It Works
User uploads PDF
↓
Text extracted & chunked (PyMuPDF + LangChain splitter)
↓
Chunks embedded & stored in ChromaDB
↓
User asks a question
↓
Top-k relevant chunks retrieved via semantic search
↓
Gemini 1.5 Flash generates an answer using retrieved context
↓
Answer + source citations returned to user
---

## 🔮 Roadmap

- [ ] Multi-document querying across a research library
- [ ] Chat history / conversational memory
- [ ] Export answers with citations to PDF/Word
- [ ] Support for web URLs and arXiv links
- [ ] Deployed cloud version

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📜 License

[MIT](LICENSE)

---

## 👩‍💻 Author

**Aimen** — BSSE Final Year Student | AI/ML Enthusiast  
[LinkedIn](https://linkedin.com/in/aimen-saeed) · [GitHub](https://github.com/AimenSaeed)
