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
- [x] Understanding PDF reading and document loading

*More topics and implementations will be added as the learning journey progresses.*

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Primary programming language |
| UV | Python package and virtual environment management |
| Jupyter Notebook | Interactive learning and experimentation |
| VS Code | Development environment |
| LangChain | Framework for working with LLM applications and document processing |
| PyPDF | PDF reading and text extraction |
| PyMuPDF | PDF processing and text extraction |
| Sentence Transformers | Text embedding models |
| FAISS | Vector similarity search |
| ChromaDB | Vector database |

*Note: These are the technologies and libraries included in or explored through the project. Their implementation will be documented as the project progresses.*

---

## 📂 Project Structure

```text
my-rag-from-scratch/
│
├── data/
│                       # Documents and other learning resources
│
├── notebook/
│                       # Jupyter notebooks for learning and experimentation
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

Verify the installations:

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

### 2. Initialize the UV Project

Initialize the Python project using:

```bash
uv init
```

This creates the necessary project configuration files, including `pyproject.toml`.

### 3. Create a Virtual Environment

```bash
uv venv
```

This creates a virtual environment named `.venv` inside the project directory.

### 4. Activate the Virtual Environment

For Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

For Windows Command Prompt:

```cmd
.venv\Scripts\activate.bat
```

### 5. Install IPython Kernel

```bash
uv add ipykernel
```

This installs IPython Kernel, allowing the project's virtual environment to be used with Jupyter Notebooks.

### 6. Install Project Dependencies

```bash
uv add -r requirements.txt
```

This installs the Python packages listed in `requirements.txt` and adds them to the project's dependency configuration.

UV also updates the `pyproject.toml` and `uv.lock` files.

### 7. Verify the Setup

```bash
python --version
uv pip list
```

Your Python development environment is now ready!

---

## 📓 Setting Up Jupyter Notebook in VS Code

Follow these steps to run Jupyter Notebooks using the project's virtual environment.

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
3. Select the Python interpreter inside your project's `.venv` directory.

Expected interpreter path:

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
4. Choose the Python interpreter from your project's `.venv` directory.

You are now ready to execute Jupyter Notebook cells inside VS Code!

---

## 📄 Current Learning: PDF Reading

An important part of building a RAG system is understanding how to load and extract information from documents.

Since PDFs are a common source of knowledge for RAG applications, this stage explores PDF processing using Python libraries.

### Libraries Explored

- **PyPDF** – Reading PDF documents and extracting their text.
- **PyMuPDF** – Working with PDF documents and extracting their contents.

### Learning Objective

Understand how information stored in PDF documents can be accessed and extracted using Python, preparing the way for subsequent stages of a RAG pipeline.

---

## 📝 Development Notes

- Use `uv add <package-name>` to install new project dependencies.
- Use `uv add --dev <package-name>` for development-only dependencies.
- Run `uv sync` whenever dependencies change or when setting up the project on a new machine.
- Keep `pyproject.toml` and `uv.lock` committed to Git.
- Do not commit the `.venv` directory.
- Never commit API keys, passwords, or other sensitive credentials.
- Keep notebooks organized so that the learning sequence is easy to follow.

### Setting Up an Existing Clone

Once the project has been initialized and its configuration files have been committed to GitHub, anyone cloning the repository can simply run:

```bash
uv sync
```

This automatically creates the virtual environment if necessary and installs the dependencies recorded in the project configuration and lockfile.

---

## 📌 Repository Status

This is an ongoing learning project. The README and notebooks will be updated as I explore additional RAG concepts and implement new components.

**Learn → Experiment → Implement → Understand.**

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
