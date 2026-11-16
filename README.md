# 🧠 Knowledge Graph Enhanced RAG for Enterprise Documents

**Intelligent Retrieval-Augmented Generation with Knowledge Graphs, Neo4j, LangChain, and LLMs**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Neo4j](https://img.shields.io/badge/Database-Neo4j-008CC1.svg)](https://neo4j.com/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green.svg)](https://www.langchain.com/)
[![OpenAI](https://img.shields.io/badge/AI-OpenAI-black.svg)](https://openai.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

🔗 Knowledge Graphs · 🔍 Hybrid Retrieval · 🤖 LLM-Powered Extraction · 💬 Context-Aware Generation

## 🌟 Overview

Knowledge Graph Enhanced RAG for Enterprise Documents is a Python-based project exploring Retrieval-Augmented Generation (RAG) using knowledge graphs, Neo4j, LangChain, and Large Language Models (LLMs).

The project demonstrates how structured knowledge representations, entity relationships, graph-based retrieval, and unstructured document information can work together to support contextual question answering and intelligent information discovery.

Traditional RAG systems commonly retrieve information using semantic similarity over unstructured documents. Knowledge Graph RAG extends this approach by representing information as interconnected entities and relationships, enabling relationship-aware retrieval and more structured exploration of information.

This repository contains several implementations and experiments involving knowledge graph creation, graph querying, hybrid retrieval, and domain-specific applications.

### Project modules

- **Simple Knowledge Graph:** Creating entities and relationships and querying graph data using Neo4j.
- **Knowledge Graph RAG:** A Roman Empire example combining graph retrieval, vector search, and LLM-based question answering.
- **Healthcare Knowledge Graph:** Building a domain-specific graph from structured healthcare CSV data and querying it through Neo4j.
- **Text Preparation for RAG:** An example of vector-based retrieval using Neo4j and text embeddings.

## ✨ Key Features

### 🔗 Knowledge Graph Engineering

- Create and manage knowledge graphs using Neo4j.
- Define entities and relationships manually.
- Construct graphs from structured CSV datasets.
- Explore LLM-powered entity extraction and relationship mapping.
- Query connected information using Cypher.

### 🔍 Intelligent Retrieval

- Graph-based information retrieval.
- Full-text search capabilities.
- Vector similarity search.
- Hybrid retrieval combining graph and vector-based information.
- Relationship-aware information exploration.

### 🤖 LLM-Powered RAG

- LangChain-based RAG workflow experiments.
- LLM-powered entity extraction.
- Context-aware question answering.
- Combining graph context with document retrieval.
- OpenAI model and embedding integration.

### 🏥 Domain-Specific Examples

- Healthcare knowledge graph construction.
- Healthcare entity and relationship queries.
- Roman Empire knowledge graph RAG example.
- Text preparation and vector retrieval experiments.

## 🏗️ System Architecture

The repository explores a workflow in which structured and unstructured information can be processed, represented, retrieved, and used to provide context for LLM-based responses.

```text
┌──────────────────────────────────────────────────────────────┐
│             KNOWLEDGE GRAPH ENHANCED RAG SYSTEM               │
├──────────────────────────────────────────────────────────────┤
│  📥 KNOWLEDGE SOURCES                                        │
│  ├── Text Documents                                          │
│  ├── Structured Data (CSV)                                   │
│  └── Domain-Specific Data                                    │
├──────────────────────────────────────────────────────────────┤
│  ⚙️ DATA PROCESSING & KNOWLEDGE EXTRACTION                    │
│  ├── Text Preparation                                        │
│  ├── Entity Extraction                                        │
│  └── Relationship Mapping                                     │
├──────────────────────────────────────────────────────────────┤
│  🗄️ KNOWLEDGE GRAPH — NEO4J                                  │
│  ├── Entity Storage                                           │
│  ├── Relationship Management                                  │
│  └── Graph Querying                                           │
├──────────────────────────────────────────────────────────────┤
│  🔍 RETRIEVAL & RAG PIPELINE                                  │
│  ├── Graph-Based Retrieval                                    │
│  ├── Full-Text Search                                        │
│  ├── Vector Similarity Search                                 │
│  └── Context Assembly                                         │
├──────────────────────────────────────────────────────────────┤
│  🤖 LLM INTEGRATION — LANGCHAIN + OPENAI                      │
│  ├── Context-Aware Question Answering                         │
│  └── Response Generation                                      │
└──────────────────────────────────────────────────────────────┘
```

*This architecture represents the concepts explored across the repository modules; it is not a claim that every stage is currently connected in one end-to-end application.*

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python 3.10+ |
| Graph Database | Neo4j |
| Graph Database Hosting | Neo4j Aura / Neo4j |
| RAG Framework | LangChain |
| Language Models | OpenAI |
| Knowledge Representation | Entities and Relationships |
| Retrieval | Graph Search, Full-Text Search, Vector Search, Hybrid Retrieval |
| Data Processing | CSV and Text Processing |
| Configuration | Environment Variables and python-dotenv |

## 📁 Project Structure

```text
Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents/
│
├── healthcare/
│   ├── health_care_kg.py
│   │   └── Healthcare knowledge graph construction
│   ├── health_care_langchain.py
│   │   └── Healthcare graph queries using LangChain
│   └── healthcare.csv
│       └── Sample healthcare dataset
│
├── kgraph_rag/
│   └── roman_emp_graph_rag.py
│       └── Roman Empire knowledge graph RAG example
│
├── prep_text_for_rag/
│   └── app.py
│       └── Text and vector retrieval example
│
├── simple_kg/
│   └── kg_simple.py
│       └── Basic Neo4j knowledge graph operations
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## 🚀 Getting Started

### 📋 Prerequisites

Make sure you have the following installed or configured:

- Python **3.10 or later**.
- A Neo4j Aura instance or locally running Neo4j database.
- An OpenAI API key for modules that use OpenAI services.
- Git.
- Internet connectivity for cloud services and API access.

> **Note:** The project uses pinned Python dependencies. Python 3.10+ is recommended for compatibility with the versions specified in `requirements.txt`.

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/pushpakrai/Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents.git

cd Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents
```

### 2️⃣ Create a Virtual Environment

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

### 3️⃣ Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4️⃣ Configure Environment Variables

Create a `.env` file in the repository root directory.

Add the credentials required by the Neo4j and OpenAI integrations:

```env
# Neo4j Configuration
NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password
AURA_INSTANCENAME=your_aura_instance_name

# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key
OPENAI_ENDPOINT=your_openai_endpoint
```

**Configuration notes:**

- Neo4j variables are required by the graph modules.
- `OPENAI_API_KEY` is required by modules that use OpenAI models or embeddings.
- `OPENAI_ENDPOINT` is used by the text preparation example's Neo4j GenAI integration.
- `AURA_INSTANCENAME` is read by the Neo4j modules.
- Use the endpoint and credentials appropriate for your Neo4j and OpenAI configuration.

## 💻 Usage Examples

The repository contains independent examples. Each module may require its own graph data, indexes, and external service configuration.

### 1. 🔗 Simple Knowledge Graph

The simple knowledge graph module demonstrates manual entity and relationship creation using Neo4j.

It creates example entities related to Albert Einstein, including Physics, the Nobel Prize in Physics, Germany, and the USA.

**Step 1: Build the graph**

Run this command from the repository root:

```bash
python -c "from simple_kg.kg_simple import build_knowledge_graph; build_knowledge_graph()"
```

**Step 2: Query the graph**

```bash
python simple_kg/kg_simple.py
```

The script executes an example Einstein-related graph query.

### 2. 🧠 Knowledge Graph RAG — Roman Empire

Location:

```text
kgraph_rag/roman_emp_graph_rag.py
```

This module demonstrates a graph-enhanced RAG approach using:

- Neo4j graph retrieval.
- Vector similarity search.
- Hybrid retrieval.
- LLM-based entity extraction.
- LangChain components.
- OpenAI chat models and embeddings.

**Important prerequisites:**

The example expects the relevant Neo4j graph data to exist already. In particular, its vector retrieval expects `Document` nodes containing text and embeddings, together with a compatible vector index.

The module also creates a full-text index for entity retrieval.

Before running it, verify the RAG chain's input mapping and move the example `chain.invoke()` call into an `if __name__ == "__main__":` block. This avoids executing an LLM request merely by importing the module.

Once those source-level checks are addressed and the required graph data and indexes are available, run:

```bash
python kgraph_rag/roman_emp_graph_rag.py
```

### 3. 🏥 Healthcare Knowledge Graph

Location:

```text
healthcare/health_care_kg.py
```

This module builds a healthcare knowledge graph from the supplied CSV dataset.

It demonstrates creating nodes and relationships for:

- Healthcare providers.
- Patients.
- Medical specializations.
- Locations.

Example relationship types include:

- `TREATS`
- `SPECIALIZES_IN`
- `LOCATED_AT`

**Important:** Before running the script, update the CSV file path in `health_care_kg.py`. The current implementation contains a machine-specific absolute path.

A portable alternative is:

```python
from pathlib import Path

csv_path = Path(__file__).with_name("healthcare.csv")
```

Use this path when opening the CSV file so the script can locate the dataset relative to its own directory.

After correcting the path and configuring Neo4j, run:

```bash
python healthcare/health_care_kg.py
```

### 4. 🏥 Healthcare Graph Queries with LangChain

Location:

```text
healthcare/health_care_langchain.py
```

This module connects to Neo4j through LangChain's Neo4j integration and executes example Cypher queries.

The queries explore information such as:

- Total graph nodes.
- Healthcare providers.
- Patients.
- Medical specializations.
- Provider locations.
- Patients treated by a specific provider.
- Providers associated with a location or specialization.

Run:

```bash
python healthcare/health_care_langchain.py
```

**Note:** This is a direct graph-query example. The current source does not define a `health_care_chain` object or a healthcare question-answering RAG chain.

### 5. 📝 Text Preparation and Vector Retrieval

Location:

```text
prep_text_for_rag/app.py
```

This module demonstrates vector-based retrieval using Neo4j's GenAI vector encoding integration.

The example uses:

- Neo4j.
- OpenAI embedding generation through Neo4j GenAI integration.
- Vector similarity search.
- Healthcare provider information.

**Important prerequisites:**

The application expects the `health_providers_embeddings` vector index and corresponding provider embedding data to be available in Neo4j.

The example vector-index creation and embedding-population queries are commented out in the current source. They must be configured and executed before the active vector retrieval query can work.

The Neo4j GenAI integration and required database procedures must also be available.

Run after provisioning the required index and data:

```bash
python prep_text_for_rag/app.py
```

## 🧩 Core Concepts

### 🔗 Knowledge Graph Creation

Knowledge graphs represent information as entities connected through relationships.

This repository explores different approaches to graph construction:

- Manual entity and relationship creation.
- Graph construction from structured CSV data.
- LLM-powered entity extraction experiments.
- Storing and querying connected information using Neo4j.

### 🔍 Graph-Based Retrieval

Graph retrieval uses relationships between entities to explore connected information.

Instead of relying only on similarity between text passages, graph queries can identify relationships and connected entities that provide additional context.

### 📄 Vector-Based Retrieval

Vector retrieval represents text as numerical embeddings and retrieves relevant information based on similarity.

The repository includes examples of Neo4j vector retrieval and OpenAI-based embedding integration.

### ⚖️ Hybrid Retrieval

Hybrid retrieval combines different retrieval approaches, such as:

- Graph-based retrieval.
- Full-text search.
- Vector similarity search.

Combining these methods can provide complementary context for LLM-powered question answering.

### 🤖 Context-Aware Question Answering

Retrieved information can be supplied to an LLM to generate responses grounded in the available context.

The Roman Empire example explores this approach by combining graph information, vector retrieval, and LLM-based response generation.

## 🏢 Potential Enterprise Applications

Knowledge Graph Enhanced RAG approaches can be useful in applications where relationships between documents, entities, and business information are important.

Potential application areas include:

- Enterprise document search and knowledge discovery.
- Healthcare information retrieval.
- Historical and domain-specific knowledge exploration.
- Relationship-based information discovery.
- Context-aware AI assistants.
- Structured knowledge management.

These are potential application areas rather than claims of deployed production use.

## 🔐 Security Best Practices

- Never commit API keys, database passwords, or private credentials.
- Store secrets in a local `.env` file.
- Keep `.env` excluded from version control.
- Use `.env.example` only with placeholder values.
- Rotate credentials immediately if they have been exposed.
- Avoid uploading credential notes or secret configuration files to public repositories.
- Review Git history if a secret was previously committed; deleting a file from the latest commit does not remove it from earlier commits.

## 🛠️ Future Enhancements

Potential areas for extending this project include:

- Advanced enterprise document ingestion.
- Automated knowledge graph construction from multiple document formats.
- Improved graph and vector retrieval integration.
- Graph-based relevance ranking and retrieval optimization.
- Multi-hop graph reasoning.
- Enhanced conversational memory.
- Retrieval evaluation and performance benchmarking.
- Automated testing and end-to-end RAG evaluation.
- Improved configuration and reusable application interfaces.

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

Special thanks to the tools and open-source projects that make this implementation possible:

- [Neo4j](https://neo4j.com/) — Graph database for storing and querying connected information.
- [LangChain](https://www.langchain.com/) — Framework for building LLM-powered applications and RAG pipelines.
- [OpenAI](https://openai.com/) — Language models and AI capabilities.
- [Python](https://www.python.org/) — Core programming language.

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Pushpak Rai**

- GitHub: [@pushpakrai](https://github.com/pushpakrai)
- LinkedIn: [Pushpak Rai](https://www.linkedin.com/in/pushpak-rai-0ab3a3200/)

---

💡 *Connecting knowledge, relationships, and intelligence to explore smarter RAG systems.*
