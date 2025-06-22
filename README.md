# 📰 Newslyzer: News Research Tool 📈

Newslyzer is an AI-powered news research tool built using [LangChain](https://www.langchain.com/), [Streamlit](https://streamlit.io/), [FAISS](https://github.com/facebookresearch/faiss), and [Together AI](https://www.together.ai/). It allows users to input news article URLs, automatically extracts and processes content, and provides intelligent answers with source references.

## ✨ Features

- Input up to **3 news URLs** directly from the sidebar.
- Automatically **loads and splits** the content into manageable chunks.
- Uses **Sentence-Transformers** for embedding generation.
- Stores embeddings in a **FAISS vector store**.
- Uses **Mistral-7B-Instruct-v0.1** via **Together API** for answering questions.
- Supports **retrieval-based question answering** with source citations.
- Caches FAISS index for faster querying.

## 🧰 Tech Stack

| Tool              | Purpose                                               |
|-------------------|-------------------------------------------------------|
| Streamlit         | Interactive UI                                        |
| LangChain         | LLM orchestration and RetrievalQA chains              |
| Together AI       | LLM API (Mistral-7B-Instruct-v0.1)                    |
| FAISS             | Vector similarity search                              |
| HuggingFace       | Text embeddings (`all-MiniLM-L6-v2`)                  |
| Python            | Core programming language                             |

## 🙌 Credits

- [LangChain](https://github.com/langchain-ai/langchain)
- [Together AI](https://www.together.ai/)
- [Sentence Transformers](https://www.sbert.net/)
- [FAISS](https://github.com/facebookresearch/faiss)
- [Streamlit](https://streamlit.io/)

## ✅ Conclusion

Newslyzer is a lightweight yet powerful AI-driven research assistant for analyzing news articles. By combining the power of modern LLMs, semantic search, and an intuitive UI, it enables users to extract meaningful insights and answers from any article on the internet. Whether you're a researcher, journalist, or curious reader, Newslyzer offers a fast, accurate, and interactive way to understand the news better.

