# 📰 Newslyzer: News Research Tool 📈

Newslyzer is an AI-powered news research tool built using [LangChain](https://www.langchain.com/), [Streamlit](https://streamlit.io/), [FAISS](https://github.com/facebookresearch/faiss), and [Together AI](https://www.together.ai/). It allows users to input news article URLs, automatically extracts and processes content, and provides intelligent answers with source references.

## 🚀 Features

- 🔗 Input up to **3 news URLs** directly from the sidebar.
- 📄 Automatically **loads and splits** the content into manageable chunks.
- 🧠 Uses **Sentence-Transformers** for embedding generation.
- 📚 Stores embeddings in a **FAISS vector store**.
- 🤖 Uses **Mistral-7B-Instruct-v0.1** via **Together API** for answering questions.
- 🔍 Supports **retrieval-based question answering** with source citations.
- 💾 Caches FAISS index for faster querying.

## 🧰 Tech Stack

| Tool              | Purpose                                               |
|-------------------|-------------------------------------------------------|
| Streamlit         | Interactive UI                                        |
| LangChain         | LLM orchestration and RetrievalQA chains              |
| Together AI       | LLM API (Mistral-7B-Instruct-v0.1)                    |
| FAISS             | Vector similarity search                              |
| HuggingFace       | Text embeddings (`all-MiniLM-L6-v2`)                  |
| Python            | Core programming language                             |

## 🏗️ Project Structure

```
├── secret_key.py                 # Stores Together API Key
├── app.py                        # Main Streamlit application
├── requirements.txt              # Python dependencies
└── faiss_store_together.pkl      # Saved FAISS index (generated after processing URLs)
```

## 🔐 Setup Your API Key

Create a file named `secret_key.py` and add the following line:

```python
Together_key = "your_together_api_key_here"
```

You can get your API key from [Together.ai](https://www.together.ai/).

## 💻 How to Run

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/Newslyzer-LLM-Rag-Project.git
cd Newslyzer-LLM-Rag-Project
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Add your Together API Key**

Create `secret_key.py`:

```python
Together_key = "your_together_api_key_here"
```

4. **Run the app**

```bash
streamlit run app.py
```

## 🧪 How It Works

1. Enter up to 3 news article URLs in the sidebar.
2. Click **"Process URLs"**:
   - Loads and parses article content using `UnstructuredURLLoader`.
   - Splits content using `RecursiveCharacterTextSplitter`.
   - Generates embeddings via `HuggingFaceEmbeddings`.
   - Stores vectors using `FAISS` and saves as a pickle file.
3. Enter your **question** in the main input box.
4. The app runs a **RetrievalQAWithSourcesChain**, and returns:
   - 🧠 A direct answer
   - 📚 Sources used for the answer

## 📌 Example Models & Components

- **Embedding Model**: `sentence-transformers/all-MiniLM-L6-v2`
- **LLM Model**: `mistralai/Mistral-7B-Instruct-v0.1` via Together API

## 📂 Sample Questions

Try asking:
- *"What is the main point of the article?"*
- *"What did the government announce?"*
- *"Summarize the article in 3 bullet points."*

## 🛠️ Troubleshooting

- Ensure all URLs are valid and accessible.
- If FAISS index isn’t generated, make sure the URL content loads correctly.
- Debug logs can be enabled using:

```python
import logging
logging.basicConfig(level=logging.DEBUG)
```

## 📃 License

MIT License. See `LICENSE` file for details.

## 🙌 Credits

- [LangChain](https://github.com/langchain-ai/langchain)
- [Together AI](https://www.together.ai/)
- [Sentence Transformers](https://www.sbert.net/)
- [FAISS](https://github.com/facebookresearch/faiss)
- [Streamlit](https://streamlit.io/)

## 🌐 Author

Made with ❤️ by [jubairt](https://github.com/jubairt)
