# AI_AGENT
AI Agent with Tool Calling — Brief Notes

Purpose:
This Python code creates a simple AI Agent using Groq LLM that can decide when to use external tools like Web Search and Calculator.

Main Components
Libraries
Groq → communicates with the LLM.
TavilyClient → performs web searches.
dotenv → loads API keys from .env.
ast + operator → safely evaluates mathematical expressions.
Tools
web_search(query) → searches the web using Tavily and returns results.
calculate(expression) → evaluates basic mathematical expressions safely.
Tool Schema
tools tells the LLM:
What tools are available.
What each tool does.
What arguments each tool requires.
Agent Loop — run_agent()
Takes the user's query.
Sends it to the Groq LLM with available tools.
LLM decides whether a tool is required.
If no tool is needed → directly returns the answer.
If a tool is needed → executes the requested tool.
Tool result is added back to the conversation.
LLM receives the tool result and generates the final answer.
