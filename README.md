# 🧠 Knowledge Graph Enhanced RAG for Enterprise Documents

**Exploring intelligent information retrieval using Knowledge Graphs, Neo4j, LangChain, and Large Language Models.**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Neo4j](https://img.shields.io/badge/Database-Neo4j-green.svg)](https://neo4j.com/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-1C3C3C.svg)](https://www.langchain.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🌟 Overview

Knowledge Graph Enhanced RAG for Enterprise Documents is a Python-based project exploring how knowledge graphs can complement Retrieval-Augmented Generation (RAG) workflows.

Traditional RAG systems commonly retrieve relevant text chunks from document collections using semantic similarity. Knowledge Graph RAG adds a structured representation of entities and relationships, making it possible to explore connections that may be difficult to capture through text similarity alone.

This project brings together:

- **Knowledge Graph Construction** to represent entities and relationships.
- **Neo4j** for storing and querying graph data.
- **LangChain and LLM Integrations** for retrieval and question-answering workflows.
- **Domain-Focused Examples** to demonstrate graph-based information retrieval.
- **Text Preparation** for downstream RAG workflows.

The repository is organized into separate modules so that each example can be explored independently.

## ✨ Features

### 🔗 Knowledge Graph Engineering

- Create and query knowledge graphs using Neo4j.
- Represent entities and relationships in graph structures.
- Create graph nodes and relationships using Cypher queries.
- Construct healthcare knowledge graphs from structured CSV data.
- Explore graph-based information discovery.

### 🔍 Retrieval and Information Discovery

- Graph-based information retrieval.
- Neo4j full-text search.
- Vector-based similarity search.
- Hybrid retrieval using Neo4j vector search capabilities.
- Relationship-aware context retrieval.

### 🤖 LLM-Powered Workflows

- LangChain integrations for LLM-based applications.
- Entity extraction using structured LLM output.
- Context-aware question-answering workflows.
- Conversation history handling in the Roman Empire RAG example.
- Integration of graph information and vector retrieval.

### 🏥 Domain-Specific Examples

- Healthcare knowledge graph construction.
- Healthcare provider and patient relationship queries.
- Roman Empire knowledge graph RAG example.
- Text preparation and vector retrieval example.

## 🏗️ Architecture

The high-level workflow explored by this project is:

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

The exact processing steps and integrations differ between modules. Refer to each module's implementation for its specific workflow.

## 🧰 Technology Stack

| Technology | Purpose |
|---|---|
| Python | Application and workflow implementation |
| Neo4j | Graph database and Cypher queries |
| Neo4j Aura | Cloud-hosted graph database option |
| LangChain | LLM application and chain integrations |
| OpenAI API | Language-model and embedding integrations where configured |
| Knowledge Graphs | Structured representation of entities and relationships |
| RAG | Retrieval-grounded question answering |
| CSV | Structured sample data and graph construction |

## 📁 Project Structure

```text
Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents/
│
├── healthcare/
│   ├── health_care_kg.py
│   ├── health_care_langchain.py
│   └── healthcare.csv
│
├── kgraph_rag/
│   └── roman_emp_graph_rag.py
│
├── prep_text_for_rag/
│   └── app.py
│
├── simple_kg/
│   └── kg_simple.py
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

### Directory Description

| Directory / File | Description |
|---|---|
| `healthcare/` | Healthcare knowledge graph construction and graph-query examples. |
| `healthcare/health_care_kg.py` | Creates healthcare entities and relationships from CSV data. |
| `healthcare/health_care_langchain.py` | Executes healthcare-related Neo4j queries using LangChain's Neo4j integration. |
| `healthcare/healthcare.csv` | Sample healthcare dataset. |
| `kgraph_rag/` | Knowledge Graph RAG implementation. |
| `kgraph_rag/roman_emp_graph_rag.py` | Roman Empire graph-enhanced retrieval and question-answering example. |
| `prep_text_for_rag/` | Text preparation and vector retrieval example. |
| `simple_kg/` | Basic Neo4j knowledge graph operations. |
| `requirements.txt` | Python project dependencies. |
| `.gitignore` | Files and directories excluded from Git. |
| `LICENSE` | MIT License. |

## 🚀 Getting Started

### 1. Prerequisites

Make sure you have:

- Python 3.8 or later, subject to compatibility with the pinned dependencies.
- Access to a Neo4j database, such as Neo4j Aura or a local Neo4j instance.
- An OpenAI API key for modules configured to use OpenAI.
- Git installed.
- Internet connectivity for cloud services and API access.

### 2. Clone the Repository

```bash
git clone https://github.com/pushpakrai/Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents.git

cd Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents
```

### 3. Create a Virtual Environment

**Windows (PowerShell):**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**Linux / macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4. Install Dependencies

```bash
python -m pip install --upgrade pip

pip install -r requirements.txt
```

### 5. Configure Environment Variables

Create a local `.env` file in the project root.

Configure the variables required by the modules:

```env
AURA_INSTANCENAME=your_aura_instance_name

NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password

OPENAI_API_KEY=your_openai_api_key
OPENAI_ENDPOINT=your_openai_endpoint
```

**Configuration notes:**

- `AURA_INSTANCENAME`, `NEO4J_URI`, `NEO4J_USERNAME`, and `NEO4J_PASSWORD` are read by the Neo4j-related Python modules.
- `OPENAI_API_KEY` is used by the LLM-related examples.
- `OPENAI_ENDPOINT` is used by the text-preparation example's Neo4j vector-encoding query.
- Configure the values required by the specific module you intend to run.

Never commit your `.env` file or expose real credentials in source code, documentation, screenshots, or Git history.

## ▶️ Running the Examples

Run commands from the repository root unless otherwise specified.

### 1. Simple Knowledge Graph

The simple knowledge graph example demonstrates querying Neo4j and exploring relationships associated with Albert Einstein.

```bash
python -c "from simple_kg.kg_simple import connect_and_query; connect_and_query()"
```

The module also contains functions for creating entities and relationships and executing Cypher queries.

### 2. Roman Empire Knowledge Graph RAG

The Roman Empire example demonstrates a graph-enhanced RAG workflow using:

- Neo4j graph data.
- Entity extraction with structured LLM output.
- Full-text entity retrieval.
- Vector similarity search.
- LangChain question-answering components.
- Conversation history handling.

Example invocation:

```python
from kgraph_rag.roman_emp_graph_rag import chain

response = chain.invoke({
    "question": "Who was the first Roman emperor?"
})

print(response)
```

The Neo4j database must contain the expected graph and document data, and the required vector index must be available.

### 3. Healthcare Knowledge Graph

The healthcare module demonstrates creating graph entities and relationships from the healthcare CSV dataset.

Before running `health_care_kg.py`, update its CSV file path to the location of `healthcare/healthcare.csv` on your machine. The current source contains a machine-specific absolute path.

Run:

```bash
python healthcare/health_care_kg.py
```

The healthcare graph-query example can be executed using:

```bash
python healthcare/health_care_langchain.py
```

It runs predefined Neo4j queries to retrieve information such as:

- Healthcare provider counts.
- Provider names.
- Patient names.
- Medical specializations.
- Locations.
- Provider-patient relationships.
- Providers associated with particular specializations and locations.

The healthcare query script executes its queries directly; it does not currently expose a `health_care_chain` object.

### 4. Text Preparation and Vector Retrieval

The text-preparation example demonstrates querying healthcare provider information through Neo4j vector search.

Run:

```bash
python prep_text_for_rag/app.py
```

**Prerequisites for this example:**

- Configure Neo4j and OpenAI environment variables.
- Ensure the Neo4j database has the required vector index named `health_providers_embeddings`.
- Ensure the provider embedding properties and vector index have been populated.
- Configure Neo4j's required vector-encoding integration.

The vector-index creation and embedding-population queries in the current source are commented out, so the required index and data may need to be provisioned separately.

## 🧩 Core Concepts

### Knowledge Graphs

A knowledge graph represents information as entities and relationships. This makes connections between concepts explicit and allows graph queries to traverse those relationships.

### Retrieval-Augmented Generation

RAG retrieves relevant information and supplies it to a language model as context for generating an answer. The quality of the response depends on the retrieved context and the model's ability to use it.

### Graph-Enhanced Retrieval

Graph-enhanced retrieval can add relationship-aware context to a RAG workflow. The examples in this repository explore this approach using Neo4j and LLM integrations.

### Hybrid Retrieval

Hybrid retrieval combines different retrieval techniques, such as graph-based information retrieval, full-text search, and vector similarity search, to explore relevant information from multiple perspectives.

## 💡 Potential Use Cases

Knowledge Graph RAG patterns can be useful when information is highly connected, for example:

- Enterprise knowledge discovery across related documents and concepts.
- Exploring relationships between people, organizations, products, or processes.
- Domain-specific question answering where entity relationships matter.
- Healthcare knowledge exploration using appropriately governed and authorized data.
- Context-aware information retrieval and AI assistant workflows.

These are potential application areas, not claims that this repository is a validated production system.

## 🔐 Security Best Practices

- Never hardcode API keys, database passwords, or access tokens.
- Store secrets in local environment variables or an approved secrets manager.
- Keep `.env` and other local secret files in `.gitignore`.
- Never commit populated credential files or private configuration notes.
- Use secure and appropriately scoped Neo4j credentials.
- Rotate or revoke credentials immediately if they are accidentally exposed.
- Remember that deleting a sensitive file in a later commit does not remove it from earlier Git history.
- Inspect repository history and remove exposed secrets from affected Git references before publishing.

## 🛣️ Future Enhancements

Potential improvements include:

- Advanced enterprise document ingestion.
- Automated knowledge graph construction from multiple document formats.
- Improved graph and vector retrieval integration.
- Graph-based relevance ranking and retrieval optimization.
- Multi-hop graph reasoning.
- Enhanced conversational memory.
- Automated tests for graph creation, retrieval, and answer generation.
- Evaluation datasets and retrieval-quality metrics.
- Observability for retrieval latency, failures, and model usage.

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome!

To contribute:

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feat/your-feature
   ```

3. Implement and test your changes.
4. Commit your changes:

   ```bash
   git commit -m "feat: add your feature"
   ```

5. Push your branch and open a Pull Request.

Please include relevant documentation and testing when introducing new functionality.

## 🙏 Acknowledgments

Special thanks to the tools and open-source projects that make this implementation possible:

- [Neo4j](https://neo4j.com/) — Graph database for storing and querying connected information.
- [LangChain](https://www.langchain.com/) — Framework for building LLM-powered applications and RAG pipelines.
- [OpenAI](https://openai.com/) — Language models and AI capabilities.
- [Python](https://www.python.org/) — Core programming language.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Pushpak Rai**

- GitHub: [@pushpakrai](https://github.com/pushpakrai)
- LinkedIn: [Pushpak Rai](https://www.linkedin.com/in/pushpak-rai-0ab3a3200/)

---

💡 *Connecting knowledge, relationships, and intelligence to explore smarter RAG systems.* 🚀
