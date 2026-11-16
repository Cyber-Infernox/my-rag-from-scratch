# My RAG From Scratch

A hands-on journey to understanding and building **Retrieval-Augmented Generation (RAG)** systems from scratch using Python.

This repository documents my learning journey as I explore the fundamental concepts behind RAG, understand its individual components, and implement them step by step.

The goal is to understand how a RAG system works internally rather than simply relying on pre-built frameworks.

## What is RAG?

Retrieval-Augmented Generation (RAG) is a technique that enhances Large Language Models (LLMs) by providing them with relevant external information before generating a response.

Instead of relying entirely on the knowledge learned during training, a RAG system retrieves relevant information from an external knowledge source and uses it as context to generate more accurate and relevant answers.

### Why RAG?

- Provides LLMs with access to external and domain-specific knowledge.
- Helps reduce hallucinations by grounding responses in retrieved information.
- Allows knowledge to be updated without retraining an LLM.
- Enables question-answering over custom documents and datasets.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Primary programming language |
| UV | Python package and environment management |
| VS Code | Development environment |
| Jupyter Notebook | Interactive coding and experimentation |
| LangChain | Document processing and RAG components |
| PyPDF | PDF reading and text extraction |
| PyMuPDF | PDF processing and text extraction |
| Sentence Transformers | Generating text embeddings |
| FAISS | Vector similarity search |
| ChromaDB | Vector database |

## Project Structure

```text
my-rag-from-scratch/
│
├── data/
│   └──                 # Documents and other data
│
├── notebook/
│   └──                 # Jupyter notebooks
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

## Getting Started

Follow the steps below to set up and run this project on your local machine.

### Prerequisites

Install the following software before getting started:

1. **Python 3.12 or newer**
   - https://www.python.org/downloads/

2. **UV**
   - https://docs.astral.sh/uv/getting-started/installation/

3. **Visual Studio Code**
   - https://code.visualstudio.com/

4. **Git**
   - https://git-scm.com/downloads

Verify the installations:

```powershell
python --version
uv --version
git --version
```

### Step 1: Clone the Repository

Open a terminal and execute:

```powershell
git clone https://github.com/Cyber-Infernox/my-rag-from-scratch.git
```

Navigate to the project directory:

```powershell
cd my-rag-from-scratch
```

### Step 2: Install Project Dependencies

This project uses UV to manage its Python environment and dependencies.

Run:

```powershell
uv sync
```

This command automatically:

- Creates a virtual environment named `.venv` if required.
- Installs the dependencies defined in `pyproject.toml`.
- Uses `uv.lock` to maintain consistent dependency versions.

You do not need to initialize the project or install the dependencies individually.

### Step 3: Open the Project in VS Code

From the project directory, execute:

```powershell
code .
```

Alternatively, open VS Code manually and select:

**File → Open Folder → my-rag-from-scratch**

### Step 4: Install VS Code Extensions

Open the Extensions panel in VS Code and install:

1. **Python** – Microsoft
2. **Jupyter** – Microsoft

These extensions provide Python interpreter selection and Jupyter Notebook support.

### Step 5: Select the Python Interpreter

VS Code needs to use the virtual environment created by UV.

1. Press `Ctrl + Shift + P`.
2. Search for `Python: Select Interpreter`.
3. Select the interpreter inside the project's `.venv` directory.

For Windows, the interpreter path should look like:

```text
.venv\Scripts\python.exe
```

### Step 6: Open and Run Jupyter Notebooks

1. Navigate to the `notebook/` directory in VS Code.
2. Open the notebook (`.ipynb`) you want to execute.
3. Click **Select Kernel** in the top-right corner.
4. Select **Python Environments**.
5. Choose the Python interpreter from the project's `.venv` directory.

You can now execute the notebook cells.

**Important:** Execute the cells in their intended order, from top to bottom, because later cells may depend on variables, functions, classes, or objects initialized in earlier cells.

## Working with the Project

- Keep your experiments and learning notebooks inside the `notebook/` directory.
- Keep reusable Python modules inside `src/my_rag_from_scratch/`.
- Use the `data/` directory for documents and other project data.
- Install additional project dependencies using `uv add package-name`.
- Run `uv sync` after dependency configuration changes.

## Important Notes

- The first execution of a Sentence Transformers model may require an internet connection to download the model files.
- Model files and generated vector database data may occupy additional disk space.
- Do not commit your `.venv` directory or unnecessary generated files.
- Never commit API keys, passwords, or other sensitive credentials.
- Keep `pyproject.toml` and `uv.lock` committed to GitHub.

## Repository Status

This is an ongoing learning project. New concepts, implementations, experiments, and notebooks will be added as I progress through the different stages of building a RAG system.

The objective is simple:

**Learn → Experiment → Implement → Understand.**

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for more information.
