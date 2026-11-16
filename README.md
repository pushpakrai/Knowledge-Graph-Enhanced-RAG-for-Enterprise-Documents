# 🧠 Knowledge Graph Enhanced RAG for Enterprise Documents

**Exploring Retrieval-Augmented Generation (RAG) with Knowledge Graphs, Neo4j, LangChain, and Large Language Models.**

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Neo4j](https://img.shields.io/badge/Database-Neo4j-green.svg)](https://neo4j.com/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-1C3C3C.svg)](https://www.langchain.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Knowledge Graphs · Hybrid Retrieval · Entity Extraction · Vector Search · Context-Aware Question Answering**

---

## 🌟 Overview

Knowledge Graph Enhanced RAG for Enterprise Documents is a Python-based project exploring how knowledge graphs can complement Retrieval-Augmented Generation (RAG) workflows.

Traditional RAG systems commonly retrieve relevant document chunks using semantic similarity. Knowledge Graph RAG extends this approach by representing information as interconnected entities and relationships, enabling structured retrieval and relationship-aware information discovery.

This repository demonstrates different approaches to:

- Creating and querying knowledge graphs using Neo4j.
- Extracting entities and relationships from text.
- Combining graph-based retrieval with vector search.
- Building LLM-powered question-answering workflows using LangChain.
- Exploring domain-specific knowledge graphs using healthcare data.

The repository contains independent examples covering knowledge graph construction, graph querying, hybrid retrieval, and text preparation.

## ✨ Key Features

### 🔗 Knowledge Graph Engineering

- Create and manage knowledge graphs using Neo4j.
- Represent entities and relationships using graph structures.
- Create nodes and relationships using Cypher queries.
- Construct healthcare knowledge graphs from structured CSV data.
- Explore relationship-based information retrieval.

### 🔍 Intelligent Retrieval

- Graph-based information retrieval.
- Neo4j full-text search.
- Vector similarity search.
- Hybrid retrieval using Neo4j vector search capabilities.
- Relationship-aware context retrieval.

### 🤖 LLM-Powered Workflows

- LangChain integrations for LLM applications.
- Structured entity extraction using LLMs.
- Context-aware question-answering workflows.
- Conversation history handling in the Roman Empire example.
- Integration of graph information and vector retrieval.

### 🏥 Domain-Specific Examples

- Healthcare knowledge graph construction.
- Healthcare provider, patient, specialization, and location queries.
- Roman Empire knowledge graph RAG example.
- Text preparation and vector retrieval example.

## 🏗️ Architecture

The following diagram illustrates the general workflow explored in this repository.

```text
              Knowledge Sources
             /        |         \
            /         |          \
       Text Data   CSV Data   Domain Data
            \         |          /
             \        |         /
                      |
                      v
               Data Processing
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
             Retrieval Pipeline
              /             \
             /               \
      Graph Retrieval    Vector Search
             \               /
              \             /
                      |
                      v
               Context Assembly
                      |
                      v
               LangChain + LLM
                      |
                      v
              Generated Response
```

The exact processing steps vary by module. Refer to the individual Python implementations for their specific workflows.

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python 3.10+ |
| Graph Database | Neo4j |
| Database Hosting | Neo4j Aura |
| RAG Framework | LangChain |
| LLM Integration | OpenAI |
| Graph Integration | LangChain Neo4j |
| Knowledge Representation | Entities and Relationships |
| Retrieval | Graph Search, Full-Text Search, Vector Search |
| Data Processing | CSV, Python |
| Environment Configuration | python-dotenv |
| Dependencies | Pinned packages in `requirements.txt` |

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

| File / Directory | Description |
|---|---|
| `healthcare/health_care_kg.py` | Creates healthcare graph entities and relationships using CSV data. |
| `healthcare/health_care_langchain.py` | Executes healthcare-related Neo4j graph queries using LangChain. |
| `healthcare/healthcare.csv` | Sample healthcare dataset. |
| `kgraph_rag/roman_emp_graph_rag.py` | Roman Empire knowledge graph-enhanced RAG implementation. |
| `prep_text_for_rag/app.py` | Healthcare provider vector retrieval example. |
| `simple_kg/kg_simple.py` | Basic Neo4j graph creation and querying operations. |
| `requirements.txt` | Pinned Python dependencies. |
| `.gitignore` | Excludes local and sensitive files from Git. |
| `LICENSE` | MIT License. |

## 🚀 Getting Started

### 1. Prerequisites

Install or configure:

- Python 3.10 or later.
- Neo4j Aura or a locally running Neo4j database.
- An OpenAI API key for LLM and embedding-related examples.
- Git.
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

The repository uses pinned dependency versions, including LangChain, Neo4j, OpenAI, NumPy, pandas, and Jupyter-related packages.

### 5. Configure Environment Variables

Create a `.env` file in the project root directory.

Add your own Neo4j and OpenAI configuration:

```env
AURA_INSTANCENAME=your_aura_instance_name

NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password

OPENAI_API_KEY=your_openai_api_key
OPENAI_ENDPOINT=your_openai_endpoint
```

**Environment variable usage:**

| Variable | Purpose |
|---|---|
| `AURA_INSTANCENAME` | Neo4j Aura instance configuration. |
| `NEO4J_URI` | Neo4j database connection URI. |
| `NEO4J_USERNAME` | Neo4j database username. |
| `NEO4J_PASSWORD` | Neo4j database password. |
| `OPENAI_API_KEY` | OpenAI API authentication. |
| `OPENAI_ENDPOINT` | Endpoint used by the Neo4j vector-encoding example. |

The Python modules use `python-dotenv` to load environment variables from the root `.env` file.

Use your own credentials. Never commit populated `.env` files or expose API keys and database passwords.

## ▶️ Usage Examples

Run commands from the repository root directory.

### 1. Simple Knowledge Graph

The simple knowledge graph example demonstrates:

- Connecting to Neo4j.
- Creating entities such as people, subjects, awards, and countries.
- Creating relationships between entities.
- Executing Cypher queries to retrieve graph paths.

First, populate the graph:

```bash
python -c "from simple_kg.kg_simple import build_knowledge_graph; build_knowledge_graph()"
```

Then execute the example queries:

```bash
python simple_kg/kg_simple.py
```

The example uses Albert Einstein-related entities and relationships.

### 2. Roman Empire Knowledge Graph RAG

The Roman Empire implementation explores:

- Knowledge graph retrieval using Neo4j.
- Entity extraction using structured LLM output.
- Full-text search for entity identification.
- Vector similarity search.
- Hybrid retrieval.
- Conversation history handling.
- LLM-powered response generation.

The implementation expects an existing Neo4j graph containing the required document and entity data, along with the appropriate vector index.

**Before running:** the current source needs a small chain-input correction. In the `RunnableParallel` mapping, pass the question value rather than the entire input dictionary:

```python
"question": RunnableLambda(lambda x: x["question"])
```

The existing file also runs a sample chain invocation at module import time. Move that sample invocation into an `if __name__ == "__main__":` block to prevent an LLM request when importing the module.

After these corrections and database setup, run:

```bash
python kgraph_rag/roman_emp_graph_rag.py
```

### 3. Healthcare Knowledge Graph

The healthcare graph builder creates:

- Healthcare provider nodes.
- Patient nodes.
- Specialization nodes.
- Location nodes.
- `TREATS`, `SPECIALIZES_IN`, and `LOCATED_AT` relationships.

The example uses `healthcare/healthcare.csv`.

**Important:** the current source contains a machine-specific absolute CSV path. Before running it, replace that path in `health_care_kg.py` with a path relative to the script:

```python
from pathlib import Path

csv_path = Path(__file__).with_name("healthcare.csv")

with csv_path.open(mode="r", newline="", encoding="utf-8") as file:
    reader = csv.DictReader(file)
```

Then run:

```bash
python healthcare/health_care_kg.py
```

### 4. Healthcare Graph Queries

The healthcare query example uses LangChain's Neo4j integration to execute predefined Cypher queries.

It demonstrates retrieving:

- Total graph node counts.
- Healthcare provider names and counts.
- Patient names.
- Medical specializations.
- Locations.
- Patients treated by a provider.
- Providers associated with a specialization and location.

Run:

```bash
python healthcare/health_care_langchain.py
```

This script executes predefined graph queries directly. It does not currently expose a `health_care_chain` object.

### 5. Text Preparation and Vector Retrieval

The text-preparation example demonstrates retrieving healthcare providers through Neo4j vector search.

It uses:

- OpenAI vector encoding through Neo4j's GenAI integration.
- A healthcare provider vector index.
- Vector similarity search.
- Provider information and similarity scores.

Run:

```bash
python prep_text_for_rag/app.py
```

**Required database setup:**

- Configure Neo4j connection variables.
- Configure the OpenAI API key and endpoint.
- Create and populate the `health_providers_embeddings` vector index.
- Ensure healthcare provider nodes contain the expected embedding properties.
- Ensure Neo4j's GenAI vector-encoding integration is configured.

The vector-index creation and embedding-population queries in the current source are commented out. The required index and embeddings must therefore be provisioned separately before running this example.

## 🧩 Core Concepts

### Knowledge Graphs

Knowledge graphs represent information through entities and relationships. They allow connected information to be stored and queried using graph structures.

### Retrieval-Augmented Generation

RAG retrieves relevant information and supplies it as context to a language model to generate grounded responses.

### Graph-Based Retrieval

Graph-based retrieval uses entity relationships and graph queries to discover relevant information connected to a given question.

### Vector Search

Vector search retrieves information based on semantic similarity between embeddings.

### Hybrid Retrieval

Hybrid retrieval combines retrieval approaches, such as graph-based information retrieval and vector similarity search, to provide complementary context.

## 💡 Potential Applications

Knowledge Graph RAG patterns can be explored in areas where relationships between information are important:

- Enterprise document search and knowledge discovery.
- Relationship-based information retrieval.
- Healthcare information exploration.
- Context-aware AI assistants.
- Domain-specific knowledge management.
- Connected-data question-answering systems.

These are potential application areas, not claims of production deployment or validated performance.

## 🔐 Security Best Practices

- Never hardcode API keys, passwords, or access tokens.
- Store credentials in environment variables or an approved secrets manager.
- Keep `.env` and private configuration files out of version control.
- Never commit credential notes or populated configuration files.
- Use appropriately scoped Neo4j credentials.
- Rotate credentials immediately if they are accidentally exposed.
- Remember that deleting a secret file in a later commit does not remove it from earlier Git history.
- Review repository history and remove exposed credentials from affected Git references before publishing.

## 🛣️ Future Enhancements

Potential improvements include:

- Advanced enterprise document ingestion.
- Automated graph construction from multiple document formats.
- Improved graph and vector retrieval integration.
- Graph-based relevance ranking.
- Multi-hop graph reasoning.
- Enhanced conversational memory.
- Automated retrieval evaluation and benchmarking.
- Unit and integration tests.
- Monitoring and observability for retrieval workflows.

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

Please include relevant documentation and tests when introducing new functionality.

## 🙏 Acknowledgments

Special thanks to the tools and open-source projects used in this project:

- [Neo4j](https://neo4j.com/) — Graph database for storing and querying connected information.
- [LangChain](https://www.langchain.com/) — Framework for building LLM-powered applications and RAG workflows.
- [OpenAI](https://openai.com/) — Language models and embedding capabilities.
- [Python](https://www.python.org/) — Core programming language.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Pushpak Rai**

- GitHub: [@pushpakrai](https://github.com/pushpakrai)
- LinkedIn: [Pushpak Rai](https://www.linkedin.com/in/pushpak-rai-0ab3a3200/)

---

*Connecting knowledge, relationships, and intelligence to explore smarter RAG systems.* 🚀
