# Day 6: Open Source Models & Local Inference

Using OpenAI and Anthropic is easy, but it ties you to their ecosystem, privacy policies, and pricing. Today, we go local.

## Open Weights
Companies like Meta (Llama 3), Mistral, and Qwen release the "weights" of their models for free. You can download these files and run the model on your own hardware.

## Tools for Local Inference
- **Ollama:** The easiest way to run local models on a Mac or PC. (e.g. `ollama run llama3`).
- **vLLM:** The enterprise standard for serving open source models incredibly fast on GPUs.
- **llama.cpp:** Allows you to run massive models on standard CPU RAM by quantizing them (making the math less precise to save space).

## Hardware
Running AI locally requires VRAM (Video RAM on a GPU). A Macbook with 32GB of unified memory is actually one of the best local AI development machines because the GPU can access all 32GB!

## Homework
1. Install Ollama.
2. Run `ollama run phi3` (a small, fast model by Microsoft).
3. Change your Python scripts from Day 1 to point to `http://localhost:11434/v1` instead of OpenAI.
