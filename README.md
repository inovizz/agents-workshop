# 🤖 Agentic AI Workshop

A comprehensive hands-on workshop for building AI agents using LangChain and LangGraph.

## 📚 Workshop Structure

| Session | Topics |
|---------|--------|
| **Session 1** | Introduction to Agents, ReAct Pattern, Workflow Patterns, Multi-Agent Systems, Framework Comparison, Advanced LangGraph |
| **Session 2** | Memory Architecture, Advanced HITL, Self-Reflection, Multi-Agent Collaboration, Context Engineering |
| **Session 3** | Evaluation Frameworks, Observability & Cost, Security & Guardrails, Case Studies, MCP Integration |

---

## 🚀 Quick Setup

### Prerequisites

- **Python 3.10+** installed on your system
- **API Key** from one of:
  - **DIAL** (EPAM AI Proxy) - for EPAM employees
  - **OpenAI** - for personal use

### Step 1: Clone & Navigate

```bash
git clone <repository-url>
cd "Agentic-AI Workshops"
```

### Step 2: Configure API Key

```bash
cp .env.example .env
```

Edit `.env` and set **ONE** of the following:

**Option A - DIAL (EPAM AI Proxy):**
```env
DIAL_API_KEY=your-dial-api-key-here
```

**Option B - OpenAI:**
```env
OPENAI_API_KEY=your-openai-api-key-here
```

### Step 3: Run Setup

**macOS/Linux:**
```bash
chmod +x setup.sh
./setup.sh
```

**Windows:**
```cmd
setup.bat
```

**Alternative (All Platforms):**
```bash
python setup.py
```

The setup script will:
1. ✅ Create a virtual environment
2. ✅ Install all dependencies
3. ✅ Register Jupyter kernel
4. ✅ Verify your API configuration
5. 🚀 **Automatically launch Jupyter Lab** (opens first notebook!)

### Step 4: Start Learning!

1. Open the folder in VS Code
2. Open any notebook in `session-1/`
3. Select the `.venv` or "Agentic AI Workshop" kernel
4. Run the cells!

---

## 📁 Project Structure

```
Agentic-AI Workshops/
├── .env.example          # Environment template
├── setup.py              # Main setup script
├── setup.sh              # macOS/Linux launcher
├── setup.bat             # Windows launcher
├── setup_llm.py          # LLM client helper
├── verify_setup.py       # Verification script
├── requirements.txt      # Python dependencies
│
├── session-1/            # Foundations
│   ├── module-0-introduction-to-agents.ipynb
│   ├── module-1-react-and-foundations.ipynb
│   ├── module-2-workflow-patterns.ipynb
│   ├── module-3-multi-agent-systems.ipynb
│   ├── module-4-framework-comparison.ipynb
│   └── module-5-advanced-langgraph.ipynb
│
├── session-2/            # Production Patterns
│   ├── module-0-opening.ipynb
│   ├── module-1-memory-architecture.ipynb
│   ├── module-2-advanced-hitl.ipynb
│   ├── module-3-self-reflection.ipynb
│   ├── module-4-multi-agent-collaboration.ipynb
│   ├── module-5-context-engineering.ipynb
│   └── projects/
│       └── incident-postmortem/  # Hands-on project
│
└── session-3/            # Enterprise & Operations
    ├── module-1-evaluation-frameworks.ipynb
    ├── module-2-observability-cost.ipynb
    ├── module-3-security-guardrails.ipynb
    ├── module-4-case-studies.ipynb
    └── module-5-mcp-integration.ipynb
```

---

## 🔧 What the Setup Does

The setup script automatically:

✅ Checks Python version (requires 3.10+)  
✅ Creates a virtual environment (`.venv`)  
✅ Installs all dependencies from `requirements.txt`  
✅ Sets up Jupyter kernel for VS Code  
✅ Verifies LLM connection (DIAL or OpenAI)  

---

## 🛠️ Manual Setup (Alternative)

If the automated setup doesn't work:

```bash
# 1. Create virtual environment
python -m venv .venv

# 2. Activate it
# macOS/Linux:
source .venv/bin/activate
# Windows:
.venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Install Jupyter kernel
python -m ipykernel install --user --name agentic-ai-workshop --display-name "Agentic AI Workshop"

# 5. Verify setup
python verify_setup.py
```

---

## 🔑 API Key Configuration

### DIAL (EPAM AI Proxy)

Get your API key from: https://ai-proxy.lab.epam.com

```env
DIAL_API_KEY=your-dial-api-key

# These are auto-configured for DIAL:
AZURE_OPENAI_ENDPOINT=https://ai-proxy.lab.epam.com
AZURE_OPENAI_API_VERSION=2024-02-01
AZURE_OPENAI_DEPLOYMENT_NAME=gpt-4
```

### OpenAI (Direct)

Get your API key from: https://platform.openai.com/api-keys

```env
OPENAI_API_KEY=your-openai-api-key

# Optional model configuration:
OPENAI_MODEL_NAME=gpt-4o-mini
```

> **Note:** Set only ONE provider. The system auto-detects which to use.

---

## ❓ Troubleshooting

### "Python not found"
- Install Python 3.10+ from [python.org](https://python.org/downloads)
- Ensure Python is in your system PATH

### "LLM connection failed"
- Check your `.env` file has the correct API key
- For DIAL: Verify access to https://ai-proxy.lab.epam.com
- For OpenAI: Verify your key at https://platform.openai.com

### "Module not found" in notebooks
- Select the correct kernel: `.venv` or "Agentic AI Workshop"
- Try restarting the kernel (Cmd/Ctrl + Shift + P → "Restart Kernel")

### Permission errors (macOS/Linux)
```bash
chmod +x setup.sh
```

### Verify your setup
```bash
python verify_setup.py
```

---

## 📖 Learning Path

### Session 1: Foundations (Start Here!)

| Module | Topic | What You'll Learn |
|--------|-------|-------------------|
| 0 | Introduction to Agents | What makes an agent, LLM + Tools + Memory |
| 1 | ReAct & Foundations | Reasoning + Acting loop, tool binding |
| 2 | Workflow Patterns | Chaining, Routing, Parallelization, Orchestrator-Worker |
| 3 | Multi-Agent Systems | Supervisor pattern, agent coordination |
| 4 | Framework Comparison | LangGraph vs CrewAI vs AutoGen |
| 5 | Advanced LangGraph | StateGraph, checkpointing, basic HITL |

### Session 2: Production Patterns

| Module | Topic | What You'll Learn |
|--------|-------|-------------------|
| 0 | Opening | Session 1 recap, setting context |
| 1 | Memory Architecture | Store API, semantic memory, streaming |
| 2 | Advanced HITL | `interrupt()`, `Command(resume=...)`, `@task` |
| 3 | Self-Reflection | Generate → Critique → Revise, LLM-as-Judge |
| 4 | Multi-Agent Collaboration | Peer review, Send API, parallel agents |
| 5 | Context Engineering | WRITE/SELECT/COMPRESS/ISOLATE pillars |

### Session 3: Enterprise & Operations

| Module | Topic | What You'll Learn |
|--------|-------|-------------------|
| 1 | Evaluation Frameworks | DeepEval, LangSmith, automated testing |
| 2 | Observability & Cost | Tracing, metrics, cost optimization |
| 3 | Security & Guardrails | Prompt injection, Meta's Rule of Two |
| 4 | Case Studies | Klarna, Replit, Elastic production examples |
| 5 | MCP Integration | Model Context Protocol for tool interop |

### Each Module Contains

- 📝 Conceptual explanations
- 💻 Hands-on code examples
- 🧪 Exercises to practice
- 🔗 Links to official documentation

