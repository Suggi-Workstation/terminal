---
name: <your-agent-name>-tools
id: <YYYYMMDDTHHMMSSZ>           # REQUIRED: ISO 8601 UTC timestamp, permanent
tier: guest-tools                 # REQUIRED: always "guest-tools"
author: <your-agent-name>         # REQUIRED: who wrote this
tags: [tools, guest, environment] # REQUIRED: lowercase, hyphens
---

# TOOLS.md -- Tool Conventions for <Your Agent Name>

> Fill in every section marked REQUIRED. This file tells other agents
> how you access tools and what your environment looks like.

## GitHub Access (REQUIRED)

> Every agent interacting with the Suggi-Workstation org needs a
> GitHub access pattern. Choose your pattern and document it here.

- **Org:** `Suggi-Workstation`
- **My GitHub user:** <your-github-username>
- **Auth method:** <personal access token / SSH key / gh CLI>
- **Clone pattern:**
  ```
  git clone https://github.com/Suggi-Workstation/<repo>.git
  ```
- **Brain access pattern:** <how do you read the agentic-brain?
  Clone temporarily? gh API? Direct git? Document your approach.>

## Chat Model (REQUIRED)

| Field | Value |
|:--|:--|
| Provider | <provider name, e.g. Anthropic, OpenAI, DeepSeek> |
| Model ID | <model identifier, e.g. claude-4, gpt-5, deepseek-v4-pro> |
| Context window | <token count> |
| Reasoning/thinking | <yes/no> |
| Cost (input/output) | <per-token or per-call cost if known> |

## Embedding Model (REQUIRED if you use memory search)

| Field | Value |
|:--|:--|
| Provider | <e.g. openai, local, ollama, gemini, none> |
| Model | <model name or "none" if keyword-only> |
| Dimensions | <vector dimensions if known> |

## Additional Tools (SUGGESTED)

<What other tools do you have? File I/O, shell execution, browser,
web search, sub-agent spawning? List them here. Other agents need
to know what you can do.>

## Environment Notes (OPTIONAL)

<Operating system, CPU, RAM, GPU, any constraints or quirks.
Examples: "I run on a 4-vCPU VPS with 8 GB RAM, no GPU."
"I have a 1M context window but no browser tool.">
