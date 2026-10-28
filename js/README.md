# LangChain Essentials - TypeScript

This folder contains the TypeScript tutorial notebooks. For a project overview and lesson list, see the [repository README](../README.md).

## Prerequisites

- Node.js
- [pnpm](https://pnpm.io/installation)
- [Deno](https://deno.com/) and its Jupyter kernel
- Python and JupyterLab

Install the Deno Jupyter kernel:

```sh
deno jupyter --install
```

After starting JupyterLab, select the **Deno** kernel for the notebooks.

## Setup

Clone the repository and enter the TypeScript project:

```sh
git clone https://github.com/Ash469/LangChain_Essentials.git
cd LangChain_Essentials/js
```

Enable Corepack if needed, then install the dependencies:

```sh
corepack enable
pnpm install
```

Create a local `.env` file from the example. In PowerShell:

```powershell
Copy-Item example.env .env
```

In macOS/Linux:

```sh
cp example.env .env
```

Get a Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey) and add it to `.env`. The notebooks and LangGraph Studio agent use Gemini. Google offers a free tier, subject to current regional availability, quotas, and rate limits; check the [Gemini API pricing](https://ai.google.dev/gemini-api/docs/pricing). LangSmith tracing is optional:

```env
GOOGLE_API_KEY=your_google_api_key_here
LANGSMITH_API_KEY=your_langsmith_api_key_here
LANGSMITH_TRACING=true
LANGSMITH_PROJECT=lca-LangGraph-Essentials-V1
# Set this only if you use the LangSmith EU region:
LANGSMITH_ENDPOINT=https://eu.api.smith.langchain.com
```

Do not commit `.env` or put API keys in notebooks. No Anthropic API key is needed for these examples.

## Run the notebooks

If JupyterLab is not installed, create a Python virtual environment and install it:

```sh
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows PowerShell
# .\.venv\Scripts\Activate.ps1
python -m pip install jupyterlab
```

Start JupyterLab from this directory:

```sh
jupyter lab
```

Open a notebook and select the **Deno** kernel in the notebook's kernel selector.

## Run LangGraph Studio

From this directory, start the local LangGraph development server:

```sh
pnpm dev
```

See the [LangGraph Studio documentation](https://docs.langchain.com/oss/javascript/langgraph/studio) for details.

## Notebook contents

- **L1 - Create an agent** (`L1_fast_agent.ipynb`): Build an SQL agent with `create_agent` and explore it in LangGraph Studio.
- **L2-L7 - Agent building blocks**: Messages, streaming, tools, MCP tools, memory, and structured output.
- **L8-L9 - Customize agents**: Use middleware for dynamic prompts and human-in-the-loop interactions.
