
# 🧠 Knowledge Graph Enhanced RAG for Enterprise Documents

### 🚀 Intelligent Retrieval-Augmented Generation with Knowledge Graphs, Neo4j & LLMs

<p align="center">
  <strong>🔗 Knowledge Graphs · 🔍 Hybrid Retrieval · 🤖 LLM-Powered Extraction · 💬 Context-Aware Generation</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?logo=python&logoColor=white" alt="Python 3.8+" />
  <img src="https://img.shields.io/badge/Graph%20Database-Neo4j-008CC1?logo=neo4j&logoColor=white" alt="Neo4j" />
  <img src="https://img.shields.io/badge/Framework-LangChain-1C3C3C?logo=langchain" alt="LangChain" />
  <img src="https://img.shields.io/badge/LLM-OpenAI-412991?logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/RAG-Knowledge%20Graph-6A5ACD" alt="Knowledge Graph RAG" />
</p>

---

## 🌟 Overview

**Knowledge Graph Enhanced RAG for Enterprise Documents** is a Python-based implementation of Retrieval-Augmented Generation (RAG) systems that combines knowledge graphs, graph-based information retrieval, and Large Language Models (LLMs).

Traditional RAG systems primarily retrieve information using semantic similarity from unstructured documents. Knowledge Graph RAG extends this approach by representing information as interconnected entities and relationships, enabling more structured retrieval and contextual understanding.

This repository explores multiple approaches to building and leveraging knowledge graphs for intelligent question answering and AI applications.

The project includes implementations for:

- 🔗 **Simple Knowledge Graph:** Basic Neo4j operations for creating and querying graph data.
- 🧠 **Knowledge Graph RAG:** Graph-enhanced retrieval and question answering using LangChain.
- 🏥 **Healthcare Knowledge Graph:** Domain-specific knowledge graph and healthcare RAG implementation.
- 📝 **Text Preparation for RAG:** Tools for preparing and processing text for retrieval workflows.

## ✨ Key Features

### 🔗 Knowledge Graph Engineering

- 🧩 Entity extraction and relationship mapping.
- 🌐 Knowledge graph creation and management using Neo4j.
- 🏗️ Manual entity and relationship creation.
- 📊 Knowledge graph construction from structured data such as CSV files.
- 🤖 Automated entity extraction from text using LLMs.

### 🔍 Intelligent Retrieval

- 🔎 Graph-based information retrieval.
- 📚 Full-text search capabilities.
- ⚖️ Hybrid retrieval combining structured and unstructured information.
- 🔗 Relationship-aware information exploration.
- 🧠 Contextual retrieval for improved question answering.

### 🤖 LLM-Powered RAG

- 🔄 LangChain-based RAG pipeline implementation.
- 🧠 LLM-powered entity extraction.
- 💬 Context-aware question answering.
- 🗂️ Conversation history handling.
- 🔍 Combining knowledge graph information with document retrieval.

### 🏥 Domain-Specific Implementations

- 🏥 Healthcare knowledge graph and question answering.
- 🏛️ Roman Empire knowledge graph RAG example.
- 📄 Text preparation utilities for RAG applications.

## 🏗️ System Architecture

The project demonstrates how structured knowledge and unstructured information can work together in a RAG workflow.

```text
┌──────────────────────────────────────────────────────────────┐
│          🧠 Knowledge Graph Enhanced RAG System               │
├──────────────────────────────────────────────────────────────┤
│  📥 Knowledge Sources                                        │
│  ├── 📄 Text Documents                                       │
│  ├── 📊 Structured Data (CSV)                                │
│  └── 🏥 Domain-Specific Data                                 │
├──────────────────────────────────────────────────────────────┤
│  ⚙️ Data Processing & Knowledge Extraction                   │
│  ├── 📝 Text Preparation                                     │
│  ├── 🧩 Entity Extraction                                    │
│  └── 🔗 Relationship Mapping                                 │
├──────────────────────────────────────────────────────────────┤
│  🗄️ Knowledge Graph — Neo4j                                  │
│  ├── Entity Storage                                          │
│  ├── Relationship Management                                 │
│  └── Graph Querying                                          │
├──────────────────────────────────────────────────────────────┤
│  🔍 Retrieval & RAG Pipeline                                 │
│  ├── Graph-Based Retrieval                                   │
│  ├── Full-Text Search                                        │
│  ├── Hybrid Information Retrieval                            │
│  └── Context Assembly                                        │
├──────────────────────────────────────────────────────────────┤
│  🤖 LLM Integration — LangChain + OpenAI                     │
│  ├── Context-Aware Question Answering                        │
│  ├── Conversation History                                    │
│  └── Response Generation                                     │
└──────────────────────────────────────────────────────────────┘
```

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| 🐍 Programming Language | Python 3.8+ |
| 🗄️ Graph Database | Neo4j |
| ☁️ Graph Database Hosting | Neo4j Aura |
| 🔗 RAG Framework | LangChain |
| 🤖 Language Models | OpenAI |
| 🧩 Knowledge Representation | Entities & Relationships |
| 🔍 Retrieval | Graph Search, Full-Text Search, Hybrid Retrieval |
| 📊 Data Processing | CSV, Text Processing |
| 🔐 Configuration | Environment Variables (`.env`) |

## 📁 Project Structure

```text
Knowledge-Graph-Enhanced-RAG-for-Enterprise-Documents/
│
├── 📂 simple_kg/
│   └── kg_simple.py
│       # Basic Neo4j knowledge graph operations
│
├── 📂 kgraph_rag/
│   └── roman_emp_graph_rag.py
│       # Roman Empire knowledge graph RAG implementation
│
├── 📂 prep_text_for_rag/
│   └── app.py
│       # Text preparation and processing for RAG
│
├── 📂 healthcare/
│   ├── health_care_kg.py
│   │   # Healthcare knowledge graph implementation
│   ├── health_care_langchain.py
│   │   # Healthcare RAG pipeline using LangChain
│   └── healthcare.csv
│       # Sample healthcare dataset
│
├── 📄 requirements.txt
│   # Python project dependencies
│
├── 📄 .gitignore
│   # Files excluded from Git
│
├── 📄 note-neo4j-creds.md
│   # Neo4j credential-related notes
│
└── 📄 README.md
    # Project documentation
```

## 🚀 Getting Started

### 📋 Prerequisites

Make sure you have the following installed or configured:

- 🐍 Python 3.8 or later.
- 🗄️ A Neo4j Aura instance or locally running Neo4j database.
- 🔑 An OpenAI API key.
- 📦 Git.
- 🌐 Internet connectivity for cloud services and API access.

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

Create a `.env` file in the root directory and configure your credentials:

```env
NEO4J_URI=your_neo4j_uri
NEO4J_USERNAME=your_neo4j_username
NEO4J_PASSWORD=your_neo4j_password
AURA_INSTANCENAME=your_aura_instance_name

OPENAI_API_KEY=your_openai_api_key
```

🔐 **Security Best Practices**

- Never expose API keys or database passwords in source code.
- Keep your `.env` file out of version control.
- Add `.env` to your `.gitignore`.
- Use secure credentials for your Neo4j database.

## 💻 Usage Examples

### 1. 🔗 Simple Knowledge Graph

The simple knowledge graph implementation demonstrates connecting to Neo4j and executing graph operations.

```python
from simple_kg.kg_simple import connect_and_query

# Connect to Neo4j and run a graph query
connect_and_query()
```

### 2. 🧠 Knowledge Graph RAG — Roman Empire

The graph-enhanced RAG implementation demonstrates question answering using the Roman Empire knowledge graph.

```python
from kgraph_rag.roman_emp_graph_rag import chain

# Ask a question about the Roman Empire
response = chain.invoke({
    "question": "Who was the first Roman emperor?"
})

print(response)
```

### 3. 🏥 Healthcare Knowledge Graph

The healthcare implementation demonstrates domain-specific knowledge graph retrieval and question answering using LangChain.

```python
from healthcare.health_care_langchain import health_care_chain

# Ask a healthcare-related question
response = health_care_chain.invoke({
    "question": "What are the symptoms of diabetes?"
})

print(response)
```

### 4. 📝 Text Preparation for RAG

The `prep_text_for_rag` module provides text preparation and processing functionality for RAG workflows.

Explore the application in:

```text
prep_text_for_rag/app.py
```

## 🧩 Core Components

### 🔗 Knowledge Graph Creation

The repository demonstrates different approaches to knowledge graph construction:

- ✍️ Manual entity and relationship creation.
- 🤖 Automated entity extraction from text using LLMs.
- 📊 Knowledge graph creation from structured CSV data.
- 🗄️ Storage and querying through Neo4j.

### 🔍 RAG Implementation

The RAG workflow combines:

- 🧠 Structured information retrieval from knowledge graphs.
- 📄 Unstructured information retrieval using vector search.
- 🔄 Hybrid retrieval combining graph and document information.
- 💬 Context-aware question answering with conversation history.

### 🧩 Entity Extraction & Relationship Mapping

Entity extraction identifies meaningful information from text and represents it as structured graph data.

The extracted entities and their relationships are stored in the knowledge graph to support future querying and information retrieval.

### 💬 Context-Aware Question Answering

The system uses retrieved graph information and contextual information to support LLM-based responses.

Conversation history is also handled to provide context across interactions.

## 🏢 Enterprise RAG Applications

Knowledge Graph Enhanced RAG can be applied to enterprise information systems where relationships between entities and documents are important.

Potential application areas include:

- 📚 Enterprise document search and knowledge discovery.
- 🏥 Healthcare information retrieval.
- 🏛️ Historical and domain-specific knowledge exploration.
- 🔗 Relationship-based information discovery.
- 💬 Context-aware AI assistants.
- 🧠 Structured knowledge management.

## 🛠️ Future Enhancements

Potential areas for extending this project include:

- 📄 Advanced enterprise document ingestion.
- 🧩 Automated knowledge graph construction from multiple document formats.
- 🔍 Improved graph and vector retrieval integration.
- ⚖️ Graph-based relevance ranking and retrieval optimization.
- 🧠 Multi-hop graph reasoning.
- 💬 Enhanced conversational memory.
- 📊 Retrieval evaluation and performance benchmarking.

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome! 🎉

To contribute:

1. 🍴 Fork the repository.
2. 🌿 Create a feature branch:

   ```bash
   git checkout -b feat/your-feature
   ```

3. 💻 Implement and test your changes.
4. 📌 Commit your changes:

   ```bash
   git commit -m "feat: add your feature"
   ```

5. 🚀 Push your branch and open a Pull Request.

Please include relevant documentation and testing when introducing new functionality.

## 🙏 Acknowledgments

Special thanks to the tools and open-source projects that make this implementation possible:

- 🗄️ **Neo4j** — Graph database for storing and querying connected information.
- 🔗 **LangChain** — Framework for building LLM-powered applications and RAG pipelines.
- 🤖 **OpenAI** — Language models and AI capabilities.
- 🐍 **Python** — Core programming language.

---

## 👨‍💻 Author

**Pushpak Rai**

- 🐙 GitHub: [@pushpakrai](https://github.com/pushpakrai)
- 💼 LinkedIn: [Pushpak Rai](https://www.linkedin.com/in/pushpak-rai-0ab3a3200/)

<p align="center">
  <strong>💡 Connecting knowledge, relationships, and intelligence to build smarter RAG systems. 🚀</strong>
</p>
