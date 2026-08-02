# Day 5: AI Agents and Multi-Agent Systems

An AI Agent is an LLM running in a continuous loop, equipped with Tools (from Day 4), and a specific system prompt giving it a goal.

## The ReAct Pattern (Reason + Act)
The foundational pattern for agents is ReAct.
1. **Thought:** The model thinks about what it needs to do.
2. **Action:** The model calls a tool.
3. **Observation:** The model looks at the result of the tool.
4. (Loop back to 1 until the goal is achieved).

## Multi-Agent Systems
Sometimes one giant system prompt fails because it's too complex. 
Multi-agent systems (like LangGraph or AutoGen) split tasks among specialized agents.
- **Agent A (Researcher):** Can search the web.
- **Agent B (Writer):** Takes Agent A's output and writes a blog post.
- **Agent C (Reviewer):** Critiques Agent B's post.

## Homework
1. Write a while-loop in Python that allows an LLM to call your stock price tool, read the result, and decide if it needs to call another tool or return the final answer to the user.
