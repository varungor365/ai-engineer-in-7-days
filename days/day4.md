# Day 4: Tool Calling & Function Calling

LLMs are trapped in a box. They only know text. If you ask an LLM "What's the weather today?", it fails.

## Tool Calling (Function Calling)
Modern models (GPT-4, Claude 3.5 Sonnet) have been fine-tuned to output JSON payloads that request the execution of a function.

1. You send a message: "What's the weather in Tokyo?"
2. You also send a JSON schema describing a tool you have: `get_weather(location)`.
3. The model does NOT reply with text. It replies with a `tool_call` requesting `get_weather("Tokyo")`.
4. YOU execute the python function on your computer.
5. YOU send the result back to the model.
6. The model reads the result and says "It's 75 degrees and sunny in Tokyo."

## Homework
1. Write a python function `get_stock_price(ticker: str) -> float`.
2. Use the OpenAI SDK's `tools` array to let GPT-4 call your function.
