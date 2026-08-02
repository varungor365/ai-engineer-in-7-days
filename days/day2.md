# Day 2: Embeddings and Vector Databases

LLMs have a context limit (e.g. 128k tokens). You can't fit a whole company's documentation into one prompt. How do we solve this? Embeddings.

## What is an Embedding?
An embedding is a numerical representation of a piece of text. It's a massive array of floats (e.g. `[0.12, -0.05, 0.99...]`). 
Sentences with similar meanings will have embedding vectors that are mathematically close to each other (using Cosine Similarity).

## Vector Databases
A Vector Database (like Pinecone, Qdrant, Chroma, or pgvector) is optimized for storing these arrays of floats and searching through them incredibly fast.

### Workflow:
1. You take a massive PDF.
2. You chunk it into paragraphs.
3. You run each paragraph through an Embedding API (like `text-embedding-3-small`).
4. You store the text and its vector in the Vector DB.

## Homework
1. Use an Embedding API to get the vector for "I love machine learning".
2. Set up a local ChromaDB instance or use `pgvector`.
3. Insert 5 sentences into the DB, and search for the one closest to "AI is awesome".
