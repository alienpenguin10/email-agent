# Agentic AI

A comprehensive collection of tutorials and implementations for building intelligent agents from scratch using modern AI frameworks.

## 🚀 Overview

This repository provides hands-on tutorials and complete implementations for building sophisticated AI agents. The main focus is on creating an intelligent email assistant that demonstrates key concepts in agentic AI, including:

- **Agent Architecture**: Building agents with LangGraph
- **Tool Integration**: Connecting agents to external APIs and services
- **Human-in-the-Loop**: Incorporating human feedback and oversight
- **Memory Systems**: Adding persistent memory and learning capabilities
- **Evaluation**: Testing and measuring agent performance
- **Production Deployment**: Real-world deployment considerations

## 📚 Tutorials

### [Agents From Scratch](./tutorials/agents_from_scratch/)

The flagship tutorial that walks you through building an intelligent email assistant from the ground up. This comprehensive guide covers:

![Agent Overview](./tutorials/agents_from_scratch/notebooks/img/overview.png)

#### What You'll Build

An "ambient" email assistant that can:
- **Triage emails** automatically based on priority and content
- **Draft responses** using context-aware language generation
- **Schedule meetings** and manage calendar events
- **Learn from feedback** to improve over time
- **Integrate with Gmail** for real-world email processing

#### Learning Path

The tutorial is structured in progressive modules:

1. **[LangGraph 101](./tutorials/agents_from_scratch/notebooks/langgraph_101.ipynb)** - Foundation concepts
2. **[Basic Agent](./tutorials/agents_from_scratch/notebooks/agent.ipynb)** - Core email assistant
3. **[Evaluation](./tutorials/agents_from_scratch/notebooks/evaluation.ipynb)** - Testing and metrics
4. **[Human-in-the-Loop](./tutorials/agents_from_scratch/notebooks/hitl.ipynb)** - Human oversight
5. **[Memory](./tutorials/agents_from_scratch/notebooks/memory.ipynb)** - Persistent learning

#### Key Features

- **Interactive Notebooks**: Step-by-step Jupyter notebooks with explanations
- **Complete Implementations**: Production-ready code in `src/email_assistant/`
- **Real API Integration**: Gmail API setup and deployment guides
- **Comprehensive Testing**: Automated test suites with LangSmith integration
- **Visual Workflows**: LangGraph Studio integration for debugging

## 🛠️ Quick Start

### Prerequisites

- Python 3.11 or later
- OpenAI API key
- LangSmith account (for tracing and evaluation)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/agentic-ai.git
cd agentic-ai

# Navigate to the tutorial
cd tutorials/agents_from_scratch

# Install dependencies (recommended: using uv)
pip install uv
uv sync --extra dev

# Activate the virtual environment
source .venv/bin/activate
```

### Environment Setup

Create a `.env` file with your API keys:

```bash
LANGSMITH_API_KEY=your_langsmith_api_key
LANGSMITH_TRACING=true
LANGSMITH_PROJECT="agentic-ai-tutorial"
OPENAI_API_KEY=your_openai_api_key
```

### Run the Tutorial

Start with the LangGraph 101 notebook to understand the fundamentals:

```bash
jupyter notebook notebooks/langgraph_101.ipynb
```

## 🏗️ Architecture

The email assistant demonstrates a sophisticated agent architecture:

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Email Input   │───▶│   Triage Agent   │───▶│  Response Agent │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                                │                        │
                                ▼                        ▼
                       ┌──────────────────┐    ┌─────────────────┐
                       │  Priority Queue  │    │   Tool Calls    │
                       └──────────────────┘    └─────────────────┘
                                                        │
                                                        ▼
                                               ┌─────────────────┐
                                               │ Human Approval  │
                                               └─────────────────┘
                                                        │
                                                        ▼
                                               ┌─────────────────┐
                                               │   Memory Store  │
                                               └─────────────────┘
```

## 🧪 Testing

The repository includes comprehensive testing:

```bash
# Test all agent implementations
python tests/run_all_tests.py

# Test notebook execution
python tests/test_notebooks.py

# Run specific evaluations
pytest tests/ -v
```

## 🚀 Deployment

### Gmail Integration

For real-world email processing, follow the [Gmail setup guide](./tutorials/agents_from_scratch/src/email_assistant/tools/gmail/README.md).

### LangGraph Platform

Deploy your agent to LangGraph Platform for production use:

```bash
# Deploy to LangGraph Platform
langgraph deploy
```

## 📊 Evaluation & Monitoring

- **LangSmith Integration**: Automatic tracing and evaluation
- **LLM-as-a-Judge**: Automated quality assessment
- **Human Feedback**: Manual review and approval workflows
- **Performance Metrics**: Response time, accuracy, and user satisfaction

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for:

- Adding new agent implementations
- Improving existing tutorials
- Enhancing evaluation frameworks
- Documentation improvements

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [LangGraph](https://github.com/langchain-ai/langgraph)
- Powered by [LangChain](https://github.com/langchain-ai/langchain)
- Evaluation with [LangSmith](https://smith.langchain.com/)
- Human-in-the-loop with [Agent Inbox](https://github.com/langchain-ai/agent-inbox)

## 📞 Support

- 📖 [Documentation](./tutorials/agents_from_scratch/README.md)
- 🐛 [Issue Tracker](https://github.com/your-username/agentic-ai/issues)
- 💬 [Discussions](https://github.com/your-username/agentic-ai/discussions)

---

**Ready to build your first intelligent agent?** Start with the [Agents From Scratch tutorial](./tutorials/agents_from_scratch/) and join the future of agentic AI! 🚀