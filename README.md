# 🧠 Knowledge Graph Enhanced RAG for Enterprise Documents

### Intelligent Retrieval-Augmented Generation with Knowledge Graphs, Neo4j, LangChain & LLMs

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Neo4j](https://img.shields.io/badge/Database-Neo4j-green.svg)](https://neo4j.com/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-1C3C3C.svg)](https://www.langchain.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Knowledge Graphs · Hybrid Retrieval · Entity Extraction · Context-Aware Question Answering

## 🌟 Overview

**Knowledge Graph Enhanced RAG for Enterprise Documents** is a Python-based project exploring Retrieval-Augmented Generation (RAG) using knowledge graphs, Neo4j, LangChain, and Large Language Models (LLMs).

Traditional RAG systems primarily retrieve information through semantic similarity searches over unstructured documents. Knowledge Graph RAG extends this approach by representing information as interconnected entities and relationships, enabling structured retrieval and relationship-aware information discovery.

This repository demonstrates different approaches to creating, storing, querying, and leveraging knowledge graphs alongside retrieval workflows.

The project includes:

- **Simple Knowledge Graph:** Basic Neo4j operations for creating and querying graph data.
- **Knowledge Graph RAG:** Graph-enhanced retrieval and question answering using LangChain.
- **Healthcare Knowledge Graph:** Domain-specific graph construction and healthcare data queries.
- **Text Preparation for RAG:** Text preparation and processing for retrieval workflows.

## ✨ Key Features

### 🔗 Knowledge Graph Engineering

- Entity extraction and relationship mapping.
- Knowledge graph creation and management using Neo4j.
- Manual entity and relationship creation.
- Knowledge graph construction from structured data such as CSV files.
- LLM-powered entity extraction from text.

### 🔍 Intelligent Retrieval

- Graph-based information retrieval.
- Full-text search capabilities.
- Hybrid retrieval combining structured and unstructured information.
- Relationship-aware information exploration.
- Contextual retrieval for question answering.

### 🤖 LLM-Powered RAG

- LangChain-based RAG pipeline implementation.
- LLM-powered entity extraction.
- Context-aware question answering.
- Conversation history handling.
- Integration of knowledge graph information with document retrieval.

### 🏥 Domain-Specific Examples

- Healthcare knowledge graph and data querying.
- Roman Empire knowledge graph RAG example.
- Text preparation utilities for RAG applications.

## 🏗️ System Architecture

The project explores how structured knowledge and unstructured information can work together in a retrieval-augmented generation workflow.

```text
              KNOWLEDGE GRAPH ENHANCED RAG
                          |
                          v
                  Knowledge Sources
                  /       |        \
                 /        |         \
          Text Data   Structured   Domain-Specific
                     Data (CSV)       Data
                 \        |         /
                  \       |        /
                          v
                Data Processing
                          |
             +------------+------------+
             |                         |
             v                         v
        Text Preparation        Entity Extraction
                                       |
                                       v
                              Relationship Mapping
                                       |
                                       v
                             Neo4j Knowledge Graph
                                       |
                                       v
                          Retrieval & RAG Pipeline
                          /          |           \
                         /           |            \
                  Graph Search  Full-Text Search  Vector Search
                         \           |            /
                          \          |           /
                           v         v          v
                              Context Assembly
                                      |
                                      v
                              LangChain + OpenAI
                                      |
                                      v
                         Context-Aware Question
                                  Answering
```

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Graph Database | Neo4j |
| Graph Database Hosting | Neo4j Aura |
| RAG Framework | LangChain |
| Language Models | OpenAI |
| Knowledge Representation | Entities and Relationships |
| Retrieval | Graph Search, Full-Text Search, Hybrid Retrieval |
| Data Processing | CSV, Text Processing |
| Configuration | Environment Variables |

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
| `simple_kg/` | Basic Neo4j knowledge graph operations. |
| `kgraph_rag/` | Roman Empire knowledge graph RAG implementation. |
| `prep_text_for_rag/` | Text preparation and processing for RAG workflows. |
| `healthcare/` | Healthcare knowledge graph examples and sample dataset. |
| `requirements.txt` | Python project dependencies. |
| `.gitignore` | Files and directories excluded from Git. |
| `LICENSE` | MIT License. |

## 🚀 Getting Started

### 📋 Prerequisites

Before running the project, make sure you have:

- Python 3.8 or later.
- A Neo4j Aura instance or locally running Neo4j database.
- An OpenAI API key for the LLM-related functionality.
- Git installed.
- Internet connectivity for cloud services and API access.

### 1. Clone the Repository

```bash
git clone https://github.com/pushpakrai/Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents.git

cd Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents
```

### 2. Create a Virtual Environment

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

### 3. Install Dependencies

```bash
python -m pip install --upgrade pip

pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root directory.

Add your Neo4j and OpenAI configuration:

```env
AURA_INSTANCENAME=your_aura_instance_name

NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password

OPENAI_API_KEY=your_openai_api_key
OPENAI_ENDPOINT=your_openai_endpoint
```

Replace the placeholder values with your own credentials and configuration.

**Important:** Never commit your `.env` file or expose database credentials and API keys in source code.

## 💻 Usage Examples

### 1. 🔗 Simple Knowledge Graph

The simple knowledge graph implementation demonstrates connecting to Neo4j and executing graph operations.

```python
from simple_kg.kg_simple import connect_and_query

# Connect to Neo4j and execute graph operations
connect_and_query()
```

### 2. 🧠 Knowledge Graph RAG — Roman Empire

The Roman Empire implementation demonstrates graph-enhanced retrieval and question answering using LangChain.

```python
from kgraph_rag.roman_emp_graph_rag import chain

# Ask a question about the Roman Empire
response = chain.invoke({
    "question": "Who was the first Roman emperor?"
})

print(response)
```

### 3. 🏥 Healthcare Knowledge Graph

The healthcare implementation demonstrates domain-specific knowledge graph operations and Neo4j queries.

Run the healthcare query example:

```bash
python healthcare/health_care_langchain.py
```

The script executes the configured healthcare graph queries and displays the retrieved results.

### 4. 📝 Text Preparation for RAG

The text preparation module provides text processing and retrieval-related functionality.

Explore and run:

```bash
python prep_text_for_rag/app.py
```

This example requires the relevant Neo4j configuration and vector index to be available.

## 🧩 Core Components

### 🔗 Knowledge Graph Creation

The repository demonstrates different approaches to knowledge graph construction:

- Manual entity and relationship creation.
- Automated entity extraction from text using LLMs.
- Knowledge graph creation from structured CSV data.
- Storage and querying through Neo4j.

### 🔍 RAG Implementation

The RAG workflow explores combining:

- Structured information retrieval from knowledge graphs.
- Unstructured information retrieval using vector search.
- Full-text and hybrid retrieval.
- Context assembly for LLM-based question answering.
- Conversation history for contextual interactions.

### 🧩 Entity Extraction & Relationship Mapping

Entity extraction identifies meaningful information from text and represents it as structured graph data.

The extracted entities and their relationships can be stored in a knowledge graph to support querying and information discovery.

### 💬 Context-Aware Question Answering

Retrieved graph information and contextual information are used to support LLM-powered responses.

The Roman Empire RAG implementation also demonstrates handling conversation history as part of the question-answering workflow.

## 🏢 Potential Enterprise Applications

Knowledge Graph Enhanced RAG can be useful in information systems where relationships between entities, records, and documents matter.

Potential application areas include:

- Enterprise document search and knowledge discovery.
- Healthcare information retrieval.
- Historical and domain-specific knowledge exploration.
- Relationship-based information discovery.
- Context-aware AI assistants.
- Structured knowledge management.

## 🔐 Security Best Practices

- Never hardcode API keys, passwords, or database credentials.
- Keep `.env` files out of version control.
- Use `.gitignore` to exclude sensitive configuration files.
- Use secure and appropriately scoped Neo4j credentials.
- Rotate credentials immediately if they are accidentally exposed.
- Avoid committing private configuration files or credential notes.

## 🛠️ Future Enhancements

Potential areas for extending this project include:

- Advanced enterprise document ingestion.
- Automated knowledge graph construction from multiple document formats.
- Improved graph and vector retrieval integration.
- Graph-based relevance ranking and retrieval optimization.
- Multi-hop graph reasoning.
- Enhanced conversational memory.
- Retrieval evaluation and performance benchmarking.

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

💡 *Connecting knowledge, relationships, and intelligence to build smarter RAG systems.* 🚀
