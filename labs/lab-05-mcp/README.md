# Lab 05 — MCP (Model Context Protocol)

## Objective
Create a local MCP server exposing enterprise tools and connect the LLM to interact with external systems.

## Concepts Covered
- MCP: Model Context Protocol specification
- Tool Use: LLM calling external functions
- Function Calling: structured tool invocation
- Server/Client architecture for LLM tools

## Enterprise Scenario
The LLM agent receives an incident ticket and uses MCP tools to:
1. Read ticket details from the ticketing system
2. Search documentation for relevant procedures
3. Check equipment history from the asset registry
4. Propose a resolution with supporting evidence

## Steps
1. Understand the MCP specification
2. Build a local MCP server with enterprise tools
3. Implement tool descriptors (schemas, parameters)
4. Connect the LLM to the MCP server
5. Test the full workflow: ticket → analysis → search → action
6. Add error handling and fallback strategies

## Deliverable
MCP agent connected to simulated enterprise tools.

## Tech Stack
- MCP SDK
- FastAPI (for tool endpoints)
- Ollama
- Python
