# Prompt Templates

This directory contains the prompt templates used in the MITRE-SAGE multi-agent framework evaluated in the accompanying paper.

## Agents

* **Orchestrator Agent** — Routes user queries to specialized retrieval agents.
* **Graph Retrieval Agent** — Generates Cypher queries for the cybersecurity knowledge graph.
* **Text Retrieval Agent** — Selects and performs retrieval over the MITRE–NVD corpus.
* **Web Retrieval Agent** — Retrieves supplementary information from public web sources.
* **Summarization Agent** — Synthesizes outputs from the retrieval agents into a coherent, concise, and grounded final response for the orchestrator.
