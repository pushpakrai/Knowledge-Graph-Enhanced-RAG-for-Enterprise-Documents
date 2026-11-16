# 🧠 Knowledge Graph Enhanced RAG for Enterprise Documents

**Intelligent document retrieval using Knowledge Graphs, Neo4j, LangChain, and Large Language Models.**

This repository explores how knowledge graphs can complement Retrieval-Augmented Generation (RAG) workflows by representing entities and their relationships in a graph database. It includes focused examples and experiments for building, querying, and using graph-based context with language models.

---

## 🌟 Overview

Traditional RAG systems commonly retrieve relevant text chunks from a document collection. Knowledge Graph RAG adds a structured representation of entities and relationships, making it possible to explore connections that may be difficult to capture through text similarity alone.

This project brings together:

- **Knowledge graph construction** to represent entities and relationships.
- **Neo4j** for storing and querying graph data.
- **LangChain and LLM integrations** for retrieval and question-answering workflows.
- **Domain-focused examples** to demonstrate how graph-based context can be applied.

The repository is organized into separate modules so that each example can be explored independently.

## ✨ Features

- Build and query knowledge graphs with Neo4j.
- Explore graph-based retrieval workflows.
- Connect graph context with LLM-powered question answering.
- Work through example domains, including healthcare and Roman Empire knowledge.
- Prepare text for downstream RAG workflows.
- Keep examples separated into focused Python packages.

## 🏗️ Architecture

The high-level workflow demonstrated by this project is:

```text
              Documents / Example Data
                         |
                         v
                 Text Preparation
                         |
                         v
              Entity & Relationship
                    Extraction
                         |
                         v
                 Knowledge Graph
                      (Neo4j)
                         |
                         v
                Graph-Based Retrieval
                         |
                         v
                  Relevant Context
                         |
                         v
                 Language Model
                         |
                         v
                  Generated Answer
```

The exact processing steps and integrations may differ between modules. Refer to each module's implementation for its specific workflow.

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| Python | Application and workflow implementation |
| Neo4j | Graph database and Cypher queries |
| LangChain | LLM application and chain integrations |
| OpenAI API | Language-model integration where configured |
| Knowledge Graphs | Structured representation of entities and relationships |
| RAG | Retrieval-grounded question answering |

## 📁 Project Structure

```text
Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents/
│
├── healthcare/          # Healthcare-focused example
├── kgraph_rag/           # Knowledge graph RAG example
├── prep_text_for_rag/    # Text preparation utilities / example
├── simple_kg/            # Basic knowledge graph example
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## 🚀 Getting Started

### 1. Prerequisites

- Python 3.8 or later (use the version supported by the dependencies in this repository).
- Access to a Neo4j database, such as Neo4j Aura or a local Neo4j instance, for modules that use Neo4j.
- An OpenAI API key if you run modules configured to use the OpenAI API.

### 2. Clone the repository

```bash
git clone https://github.com/pushpakrai/Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents.git
cd Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents
```

### 3. Create and activate a virtual environment

**Windows (Command Prompt):**

```cmd
python -m venv .venv
.venv\\Scripts\\activate
```

**macOS / Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Configure environment variables

Create a local `.env` file in the location expected by the relevant module. Do not commit this file or place real credentials in source code, notebooks, documentation, screenshots, or Git history.

Example template (use only the variable names actually read by your code):

```env
NEO4J_URI=
NEO4J_USERNAME=
NEO4J_PASSWORD=
OPENAI_API_KEY=
```

If a module requires additional settings, check its source code and configure those values locally. Keep `.env` excluded through `.gitignore`.

## ▶️ Running the Examples

Run commands from the repository root unless a module's code specifies otherwise.

### Simple knowledge graph

```bash
python -c "from simple_kg.kg_simple import connect_and_query; connect_and_query()"
```

### Knowledge Graph RAG example

```bash
python -c "from kgraph_rag.roman_emp_graph_rag import chain; print(chain.invoke('Ask a question about the Roman Empire'))"
```

### Healthcare example

```bash
python -c "from healthcare.health_care_langchain import health_care_chain; print(health_care_chain.invoke('Ask a question supported by the healthcare example data'))"
```

### Text preparation

```bash
python prep_text_for_rag/app.py
```

These are example entry points based on the repository's module layout. If an import or command differs in your local checkout, inspect the relevant Python file for its actual entry point and required configuration.

## 🧩 Core Concepts

### Knowledge Graphs

A knowledge graph represents information as entities and relationships. This makes connections between concepts explicit and allows graph queries to traverse those relationships.

### Retrieval-Augmented Generation

RAG retrieves relevant information and supplies it to a language model as context for generating an answer. The quality of the response depends on the retrieved context and the model's ability to use it.

### Graph-Enhanced Retrieval

Graph-enhanced retrieval can add relationship-aware context to a RAG workflow. The examples in this repository are intended to help explore this approach using Neo4j and LLM integrations.

## 💡 Potential Use Cases

Knowledge Graph RAG patterns can be useful when information is highly connected, for example:

- Enterprise knowledge discovery across related documents and concepts.
- Exploring relationships between people, organizations, products, or processes.
- Domain-specific question answering where entity relationships matter.
- Healthcare knowledge exploration using appropriately governed and authorized data.

These are potential application areas, not claims that this repository is a validated production system.

## 🔐 Security Notes

- Never commit API keys, database passwords, access tokens, or populated credential files.
- Store secrets in local environment variables or an approved secrets manager.
- Keep `.env` and other local secret files in `.gitignore`.
- If a credential has ever been pushed to a public repository, rotate or revoke it immediately. Deleting the file in a later commit does **not** remove it from earlier Git history.
- Before publishing, inspect the repository history and remove exposed secrets from all affected refs. Coordinate history rewrites with collaborators.

## 🛣️ Possible Future Enhancements

- Add automated tests for graph creation, retrieval, and answer generation.
- Add evaluation datasets and retrieval / answer-quality metrics.
- Document each module's configuration and execution steps.
- Add observability for retrieval latency, failures, and model usage.
- Explore hybrid graph and vector retrieval where supported by the implementation.

## 🤝 Contributing

Contributions, suggestions, and issue reports are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make a focused change and add or update tests where appropriate.
4. Verify that no secrets or private data are included.
5. Open a pull request with a clear description of the change.

## 📄 License

This project is licensed under the **MIT License**. See the [`LICENSE`](LICENSE) file for details.

## 👤 Author

**Pushpak Rai**

- GitHub: [@pushpakrai](https://github.com/pushpakrai)
- LinkedIn: [Pushpak Rai](https://www.linkedin.com/in/pushpak-rai-0ab3a3200/)

---

If you find this project useful, consider giving the repository a ⭐ on GitHub.
"""
