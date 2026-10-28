# LangChain Essentials

Short, hands-on TypeScript notebooks introducing core LangChain and LangGraph concepts. The examples use Google's Gemini API, which offers a free tier so you can follow along without an Anthropic API key. Start with the agent-building lesson, then explore the building blocks and middleware used to customize agents.

## Lessons

The notebooks are in [`js/`](js/):

| Notebook | Topic |
| --- | --- |
| `L1_fast_agent.ipynb` | Build an SQL agent with `create_agent` |
| `L2_messages.ipynb` | Work with messages |
| `L3_streaming.ipynb` | Stream agent responses |
| `L4_tools.ipynb` | Give agents tools |
| `L5_tools_with_mcp.ipynb` | Connect agents to MCP tools |
| `L6_memory.ipynb` | Maintain state between invocations |
| `L7_structuredOutput.ipynb` | Return structured output |
| `L8_dynamic.ipynb` | Customize prompts with middleware |
| `L9_HITL.ipynb` | Add human-in-the-loop interactions |

## Get started

Follow the [TypeScript setup guide](js/README.md) to get a Gemini API key, install dependencies, configure the project, and launch the notebooks.

## Requirements

- Node.js and pnpm
- Deno, for the notebooks' Deno Jupyter kernel
- Python and JupyterLab
- A [Google Gemini API key](https://aistudio.google.com/apikey); Google offers a free tier
- A LangSmith API key is optional for tracing

Gemini's free-tier availability, quotas, and rate limits depend on Google's current policies and your region. Check the [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing) before use; free access is not unlimited or guaranteed.

## Security

Keep API keys in your local `js/.env` file. Do not commit credentials or share them publicly.
