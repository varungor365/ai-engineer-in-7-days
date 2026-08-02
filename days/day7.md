# Day 7: Evals and Productionizing AI

You built a cool RAG demo on Day 3. Now you want to launch it to customers. How do you know it actually works consistently?

## The AI Engineering Lifecycle
Traditional software engineering uses Unit Tests (assert 2+2 == 4). 
AI engineering uses **Evals**.

## What is an Eval?
An Eval (Evaluation) is a systematic way of grading your LLM's output. Since LLM output is non-deterministic (it changes slightly every time), you can't use simple string matching.

Instead, you use "LLM-as-a-Judge". You have a strong model (like GPT-4) grade the output of your application based on a rubric.

### Typical RAG Evals:
- **Faithfulness:** Did the answer come strictly from the retrieved context, or did it hallucinate?
- **Answer Relevance:** Did the answer actually address the user's question?
- **Context Relevance:** Were the paragraphs you pulled from the Vector DB actually relevant?

## Congratulations!
You've completed the 7 days. You now understand APIs, Embeddings, RAG, Tool Calling, Agents, Local Models, and Evals. 

You are an AI Engineer. Now go build something awesome!
