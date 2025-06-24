# 📚 MultiPDF Chat App

Interact with multiple PDF documents using natural language queries. This application enables you to ask questions about the contents of uploaded PDF files, 
and it returns accurate responses by leveraging a powerful language model from OpenAI.

## 🚀 Features

- 🗂 Load and process **multiple PDF files**
- 🧠 Ask **natural language questions**
- 🔍 Retrieves relevant answers using **semantic similarity**
- 📎 Simple UI powered by **Streamlit**
- 🔐 Uses **OpenAI API** for intelligent responses

---

## 🧠 How It Works

```mermaid
flowchart TD
    A[Upload PDFs] --> B[Extract Text]
    B --> C[Chunk Text]
    C --> D[Generate Embeddings (OpenAI)]
    E[Ask Question] --> F[Create Query Embedding]
    D --> G[Similarity Search]
    F --> G
    G --> H[Select Relevant Chunks]
    H --> I[Generate Response (OpenAI)]
````

---

## 🛠️ Installation

1. **Clone the repository**:

```bash
git clone https://github.com/your-username/multipdf-chat-app.git
cd multipdf-chat-app
```

2. **Install the required dependencies**:

```bash
pip install -r requirements.txt
```

3. **Set up your OpenAI API key**:

Create a `.env` file in the root directory and add your API key:

```
OPENAI_API_KEY=your_secret_api_key
```

## 💡 Usage

1. **Run the app using Streamlit**:

```bash
streamlit run app.py
```

2. **Load your PDF documents** using the UI.

3. **Ask questions** about the content in plain English.

4. The app will display responses based on the semantic meaning of your question and the PDF content.

---

## 📂 Project Structure

```
multipdf-chat-app/
├── app.py                 # Streamlit application entry point
├── main.py                # Core logic (if used separately)
├── requirements.txt       # Python dependencies
├── .env                   # Your OpenAI API key (do NOT share this)
├── README.md              # Project documentation
└── /your_pdf_files        # PDF files loaded by the user
```

---

## 📋 Requirements

* Python 3.8+
* `openai`
* `streamlit`
* `PyPDF2` or `pdfplumber`
* `langchain`
* `faiss-cpu` or `chromadb` (for embedding search)

All required packages are listed in `requirements.txt`.

---

## 🔐 Important

> Do NOT commit your `.env` file or share your API keys publicly.

To ensure `.env` is never tracked by Git, make sure it’s in your `.gitignore` file:



