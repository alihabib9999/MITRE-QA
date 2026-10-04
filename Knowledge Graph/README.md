# MITRE-QA Knowledge Graph

This directory contains the knowledge graph used by the MITRE-QA benchmark and the graph-based retrieval component of the proposed MITRE-SAGE multi-agent framework.

## File

- [`mitre_qa_knowledge_graph.gpickle`](mitre_qa_knowledge_graph.gpickle) — NetworkX `MultiDiGraph` containing the integrated cybersecurity knowledge graph.

## Graph Statistics

| Property | Value |
|---|---:|
| Graph type | NetworkX `MultiDiGraph` |
| Number of nodes | 280,147 |
| Number of edges | 163,652 |

### Node Types

The graph contains the following cybersecurity entity types:

| Entity Type | Number of Nodes |
|---|---:|
| CVE | 274,693 |
| Analytic | 1,739 |
| Malware | 696 |
| Detection Strategy | 691 |
| Technique | 611 |
| CAPEC | 559 |
| CWE | 399 |
| Mitigation | 268 |
| Group | 187 |
| Data Component | 109 |
| Tool | 91 |
| Campaign | 52 |
| Data Source | 38 |
| Tactic | 14 |

### Knowledge Sources

The knowledge graph integrates cybersecurity information from:

- MITRE ATT&CK
- MITRE CAPEC
- MITRE CWE
- NVD CVE

The CVE entities included in the knowledge graph are restricted to vulnerabilities **published after 2010**.

## Loading the Knowledge Graph

The graph can be loaded using NetworkX:

```python
import pickle

with open("mitre_qa_knowledge_graph.gpickle", "rb") as f:
    graph = pickle.load(f)

print(f"Nodes: {graph.number_of_nodes()}")
print(f"Edges: {graph.number_of_edges()}")