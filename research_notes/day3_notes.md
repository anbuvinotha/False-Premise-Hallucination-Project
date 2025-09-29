# Day 3: LLM Hallucination Insights from Video

## LLM Hallucination Overview
- Every LLM has a training cutoff date. Example: If GPT-5’s cutoff is August 1, 2025, and today is September 29, 2025, it lacks data post-cutoff. It may generate factually untrue answers for recent events, making them seem credible.

## Causes of Hallucination
1. Training cutoff date limits knowledge of recent data.
2. Insufficient training data on specific topics.

## Mitigation Strategies
- Hallucinations can’t be fully eliminated but can be reduced by 20-30% using:
  - **RAG Application**: Optimizes LLM output with an external knowledge base.
  - **LLM Fine-Tuning**: Expensive and time-consuming due to billions of parameters; impractical for daily updates.
  - **Human Verification**: Manual fact-checking.

## Retrieval-Augmented Generation (RAG)
- **Definition**: Enhances LLM output by referencing an authoritative external knowledge base (e.g., vector database) without retraining.
- **Process**: 
  - Query triggers a search in the knowledge base.
  - Data ingestion pipeline handles structured/unstructured data (PDF, HTML, Excel, SQL).
  - Parsing divides data into chunks.
  - Embedding converts text to vectors for similarity search.
- **Use Case**: For a startup chatbot with private policies (e.g., finance, HR), RAG accesses an internal database instead of fine-tuning daily.

## Reflection
- The training cutoff date explains why recent stats questions might trigger hallucinations. RAG could help my project by adding a stats fact base to test LLM accuracy on post-2025 data.

- <img width="1719" height="944" alt="Screenshot 2025-09-29 212224" src="https://github.com/user-attachments/assets/b863bda8-9622-4871-8ca4-e98a58c435c3" />
