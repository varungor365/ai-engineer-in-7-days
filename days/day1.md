# Day 1: APIs, Tokens, and Prompt Engineering

Welcome to Day 1! Today, you'll learn the absolute fundamentals of working with Large Language Models (LLMs).

## What is an LLM?
At its core, an LLM is a giant auto-complete engine. It takes text, turns it into "tokens" (chunks of characters), and predicts the next token.

## The API
You interact with an LLM via an API. The standard interface looks like this (OpenAI style):

```json
{
  "model": "gpt-4",
  "messages": [
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "Explain quantum computing in one sentence."}
  ]
}
```

## Prompt Engineering
Prompt engineering isn't just "talking to AI". It's a programming paradigm.

### 1. Zero-shot vs Few-shot
- **Zero-shot:** Asking a question with no examples.
- **Few-shot:** Giving the model 3-4 examples of inputs and desired outputs before asking the real question. (This drastically improves reliability).

### 2. System Prompts
The `system` message is where you define the persona, constraints, and output format. 
*Pro-tip: Always tell the model EXACTLY what format to output (e.g. "Output ONLY valid JSON without markdown wrapping").*

## Homework
1. Get an API key (OpenAI or Anthropic).
2. Write a Python script that calls the API and prints the response.
3. Use a Few-shot prompt to make the AI extract named entities from a sentence.
