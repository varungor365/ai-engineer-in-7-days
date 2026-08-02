# Day 3: RAG (Retrieval-Augmented Generation)

Now that you know how Embeddings and Vector DBs work, we combine them with LLMs to create RAG.

## The Problem
LLMs hallucinate. If you ask GPT-4 about a private company policy created yesterday, it will make up an answer because it wasn't trained on it.

## The RAG Solution
1. **Retrieve:** When the user asks a question, turn the question into an embedding. Search your Vector DB for the top 5 most relevant paragraphs of your private data.
2. **Augment:** Inject those 5 paragraphs into the System Prompt.
3. **Generate:** Let the LLM answer the user's question *using only the injected context*.

```python
prompt = f"""
Answer the user's question using ONLY the context provided below.
If the answer is not in the context, say "I don't know."

Context:
{retrieved_documents}

Question:
{user_question}
"""
```

## Homework
1. Build a basic RAG script in Python without using heavy frameworks like LangChain. Just use the OpenAI SDK and a local dictionary or Chroma.
