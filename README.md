# 📘 Retrieval-Augmented QA with TinyLLaMA and LangChain

This project demonstrates a lightweight Retrieval-Augmented Generation (RAG) pipeline using:

- 🦙 **TinyLLaMA** for local LLM inference (via `llama-cpp-python`)
- 🔗 **LangChain** for orchestration and chaining
- 📚 **FAISS** for fast vector-based document retrieval
- 🧠 **HuggingFace Embeddings** (`all-MiniLM-L6-v2`)
- 📄 Custom documents for context-aware Question Answering

---

## 🚀 Features

- ✅ Runs fully **offline** with no OpenAI API key needed
- ✅ Loads and indexes text documents from local disk
- ✅ Performs chunked text splitting and dense embedding
- ✅ Supports **natural language Q&A** over documents using a local LLM

---

## 🧱 Architecture

```plaintext
[Your Documents] → [Text Splitter] → [Embeddings] → [FAISS Index]
                                   ↓
                             [LangChain Retriever]
                                   ↓
                               [TinyLLaMA (LLM)]
                                   ↓
                              [Final Answer]
