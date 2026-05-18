---
name: 13-retrieval-strategies
description: Use when executing 13 retrieval strategies protocols within the engineering sector.
---

# 13 Retrieval Strategies: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 13 Retrieval Strategies. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 13 retrieval strategies logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 1.3 Retrieval Strategies

```python
# Basic semantic search
def semantic_search(query: str, top_k: int = 5):
    query_embedding = embed(query)
    results = vector_db.similarity_search(
        query_embedding,
        top_k=top_k
    )
    return results

# Hybrid search (semantic + keyword)
def hybrid_search(query: str, top_k: int = 5, alpha: float = 0.5):
    """
    alpha=1.0: Pure semantic
    alpha=0.0: Pure keyword (BM25)
    alpha=0.5: Balanced
    """
    semantic_results = vector_db.similarity_search(query)
    keyword_results = bm25_search(query)

    # Reciprocal Rank Fusion
    return rrf_merge(semantic_results, keyword_results, alpha)

# Multi-query retrieval
def multi_query_retrieval(query: str):
    """Generate multiple query variations for better recall"""
    queries = llm.generate_query_variations(query, n=3)
    all_results = []
    for q in queries:
        all_results.extend(semantic_search(q))
    return deduplicate(all_results)

# Contextual compression
def compressed_retrieval(query: str):
    """Retrieve then compress to relevant parts only"""
    docs = semantic_search(query, top_k=10)
    compressed = llm.extract_relevant_parts(docs, query)
    return compressed
```