# my-rag-from-scratch
Learning RAG from scratch

Setup Commands -
uv init
uv venv
.venv\Scripts\activate
uv add ipykernel
uv add -r requirements.txt

# 🚀 My RAG From Scratch

**A hands-on journey to understanding and building Retrieval-Augmented Generation (RAG) systems from scratch using Python.**

This repository documents my learning journey as I explore the fundamentals of RAG, understand its individual components, and gradually work towards building a complete RAG pipeline.

The goal is not just to use existing frameworks, but to understand what's happening behind the scenes at every stage.

---

## 📖 What is RAG?

**Retrieval-Augmented Generation (RAG)** is a technique that enhances Large Language Models (LLMs) by providing them with relevant external information before generating a response.

Instead of relying entirely on the knowledge learned during training, a RAG system retrieves relevant information from an external knowledge source and uses it as context to generate more accurate and relevant answers.

### Why RAG?

- Provides LLMs with access to external and domain-specific knowledge.
- Helps reduce hallucinations by grounding responses in retrieved information.
- Allows knowledge to be updated without retraining the LLM.
- Enables question-answering over custom documents and datasets.

---

## 🎯 Learning Roadmap

This repository is organized as a step-by-step learning journey.

### Current Progress

- [x] Understanding the fundamentals of RAG
- [x] Setting up the Python development environment using UV
- [x] Working with Jupyter Notebooks in VS Code
- [x] Understanding document loading and PDF reading

*More topics and implementations will be added as the learning journey progresses.*

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Primary programming language |
| UV | Python project and dependency management |
| Jupyter Notebook | Interactive learning and experimentation |
| VS Code | Development environment |
| LangChain | Framework for working with LLM applications and document processing |
| PyPDF | PDF reading and text extraction |
| PyMuPDF | PDF processing and text extraction |
| Sentence Transformers | Text embedding models |
| FAISS | Vector similarity search |
| ChromaDB | Vector database |

*Note: The tools listed above are project dependencies and technologies being explored. Not all are necessarily covered in the current notebooks.*

---

## 📂 Project Structure

```text
my-rag-from-scratch/
│
├── data/
│   └──                 # Documents and other learning resources
│
├── notebook/
│   └──                 # Jupyter notebooks for learning and experimentation
│
├── src/
│   └── my_rag_from_scratch/
│                       # Python source code
│
├── .gitignore
├── .python-version
├── LICENSE
├── README.md
├── pyproject.toml
├── requirements.txt
└── uv.lock
```

---

## ⚙️ Environment Setup

This project uses **UV** for Python package and virtual environment management.

### Prerequisites

Make sure you have the following installed:

- [Python 3.12 or newer](https://www.python.org/downloads/)
- [UV](https://docs.astral.sh/uv/getting-started/installation/)
- [Visual Studio Code](https://code.visualstudio.com/)

Verify your installations:

```powershell
python --version
uv --version
```

### 1. Clone the Repository

```bash
git clone https://github.com/Cyber-Infernox/my-rag-from-scratch.git
```

Navigate to the project directory:

```bash
cd my-rag-from-scratch
```

### 2. Set Up the Environment

Install all project dependencies using:

```bash
uv sync
```

This command automatically:

- Creates a `.venv` virtual environment if it doesn't exist.
- Installs the dependencies specified in `pyproject.toml`.
- Synchronizes the environment using `uv.lock`.

### 3. Activate the Virtual Environment (Optional)

For Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

For Windows Command Prompt:

```cmd
.venv\Scripts\activate.bat
```

You can also execute Python commands without manually activating the environment by using `uv run`.

---

## 📓 Setting Up Jupyter Notebook in VS Code

### Step 1: Install VS Code Extensions

Open VS Code and install the following extensions:

1. **Python** – Microsoft
2. **Jupyter** – Microsoft

### Step 2: Open the Project

Open the repository in VS Code:

```bash
code .
```

### Step 3: Select the Python Interpreter

1. Press `Ctrl + Shift + P`.
2. Search for `Python: Select Interpreter`.
3. Select the interpreter inside your project's `.venv` directory.

Expected path:

```text
.venv\Scripts\python.exe
```

### Step 4: Open a Jupyter Notebook

Navigate to the `notebook/` directory and open an existing `.ipynb` file.

You can also create a new notebook using:

`File → New File → Jupyter Notebook`

### Step 5: Select the Jupyter Kernel

1. Open the notebook.
2. Click **Select Kernel** in the top-right corner.
3. Select **Python Environments**.
4. Choose the interpreter from your project's `.venv`.

You are now ready to execute notebook cells!

---

## 📄 Current Learning: PDF Reading

An important part of building a RAG system is understanding how to load and extract information from documents.

Since PDFs are a common source of knowledge for RAG applications, this stage explores PDF processing using Python libraries.

### Libraries

- **PyPDF** – Reading PDF documents and extracting their text.
- **PyMuPDF** – Working with PDF documents and extracting their contents.

The objective is to understand how information stored in PDF documents can be accessed and prepared for subsequent stages of a RAG pipeline.

---

## 📝 Development Notes

- New dependencies should be added using `uv add <package-name>`.
- Development-only dependencies can be added using `uv add --dev <package-name>`.
- Run `uv sync` after updating project dependencies.
- Keep `pyproject.toml` and `uv.lock` committed to Git.
- Do not commit the `.venv` directory.
- Never commit API keys, passwords, or other sensitive credentials.

---

## 📌 Repository Status

This is an ongoing learning project. The README and notebooks will be updated as I explore additional RAG concepts and implement new components.

**Learn → Experiment → Implement → Understand.**

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
