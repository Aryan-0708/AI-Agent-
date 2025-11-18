# AI-Agent-
# Code Runner Agent

**Short description**

Code Runner Agent is a Jupyter Notebook project that demonstrates an agent-based code execution workflow. The notebook integrates Google ADK agents (Sequential/Parallel/Loop agents and tools), a Gemini LLM model, and utility libraries (NumPy, pandas). It also includes a safe execution helper (`safe_run_code`) to run user code with basic guarding.

This README was generated from the notebook `code-agent.ipynb` you provided.

---

## Features

* Uses Google ADK agent classes (Agent, SequentialAgent, ParallelAgent, LoopAgent).
* Integrates `Gemini` model from `google.adk.models.google_llm` for LLM-driven workflows.
* Demonstrates runner usage (`InMemoryRunner`) and tools (`AgentTool`, `FunctionTool`, `google_search`).
* Utility code using `numpy` and `pandas` for data processing.
* A `safe_run_code` helper to execute code snippets with minimal safeguards.

---

## Files to include in repository

* `code-agent.ipynb` — main Jupyter notebook (already provided).
* `README.md` — this file.
* `requirements.txt` — Python package requirements (see below).

---

## Requirements

Below is a suggested `requirements.txt` based on the imports found in the notebook. Please review and adjust versions to match your environment or environment managers (pip, conda).

```
# requirements.txt (suggested)
google-adk
google-genai
kaggle-secrets
numpy
pandas

# Optional: if using Jupyter in a repo
notebook
ipykernel

# If you need typing / helper libs
typing-extensions
```

> Note: "google-adk" and "google-genai" package names are inferred from import paths used in the notebook. If your environment uses different package names (or internal SDKs), update `requirements.txt` accordingly.

---

## Installation (local)

1. Create a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate    # on macOS / Linux
venv\Scripts\activate     # on Windows
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook code-agent.ipynb
```

---

## Usage

Open `code-agent.ipynb` and run cells in order. The notebook shows how to:

* Configure and instantiate ADK agents and tools
* Use the `InMemoryRunner` to execute agent flows
* Run small code snippets safely with `safe_run_code`

If the notebook requires API keys (e.g., Google or Kaggle secrets), set them in your environment or in the secret manager used by the notebook (`kaggle_secrets` is referenced in the notebook).

---

## How I generated this README

I parsed the notebook and detected the following notable imports and definitions:

* `from google.adk.agents import Agent, SequentialAgent, ParallelAgent, LoopAgent`
* `from google.adk.models.google_llm import Gemini`
* `from google.adk.runners import InMemoryRunner`
* `from google.adk.tools import AgentTool, FunctionTool, google_search`
* `from google.genai import types`
* `from kaggle_secrets import UserSecretsClient`
* `import numpy as np`
* `import pandas as pd`
* A helper function named `safe_run_code`

Use this README as a starting point. If any of the imports are internal or part of a private SDK, replace them in `requirements.txt` with the correct package names.

---

## Recommended next steps (I can do these for you)

1. I can create a `requirements.txt` file containing the exact lines above.
2. I can produce a zipped project folder ready for upload.
3. I can produce a short `LICENSE` (MIT) if you want to make the repo open source.

Tell me which of the three you want me to generate next and I will create the file(s) for you.
