# Google 5-Day AI Agents Intensive 🤖

> Complete learning guide for building production-grade AI agents using tools, context engineering, memory systems, and deployment strategies.

![Course Progress](https://img.shields.io/badge/Course%20Progress-100%25-brightgreen)
![Last Updated](https://img.shields.io/badge/Last%20Updated-Nov%202025-blue)
![License](https://img.shields.io/badge/License-Apache%202.0-green)

***/

## 🎯 What You'll Learn

### **Foundation (Day 1)**
- What makes an agent different from a chatbot
- The architecture of stateful AI systems
- When to use agents vs simpler approaches

### **Tools & Integration (Day 2)**
- Designing custom function tools
- Model Context Protocol (MCP) fundamentals
- Multi-agent systems with tool composition
- **[→ Explore Currency Converter Agent Example](./codelabs/day-2a-agent-tools)**

### **Memory & Context (Day 3)**
- Context engineering: Dynamic context assembly
- Session management for stateful conversations
- Long-term memory systems (ETL pipeline)
- Recursive summarization for context efficiency
- **[→ Sessions Codelab](./codelabs/day-3a-agent-sessions)** -  **[→ Memory Codelab](./codelabs/day-3b-agent-memory)**

### **Quality & Evaluation (Day 4)**
- Metrics for agent quality
- Testing strategies
- Production readiness checklist

### **Deployment at Scale (Day 5)**
- Going from development to production
- Scaling considerations
- Cost optimization
- Observability & monitoring

***

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- Jupyter Notebook or JupyterLab
- Google API Key ([get one free here](https://aistudio.google.com/app/api-keys))

### Installation

```bash
# Clone the repository
git clone https://github.com/azaynul10/google-ai-agents-intensive-5days.git
cd google-ai-agents-intensive-5days

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# For development
pip install -r requirements-dev.txt
``````

### First Codelab

```
# Navigate to Day 2a codelab
cd codelabs/day-2a-agent-tools

# Start Jupyter
jupyter notebook day-2a-agent-tools.ipynb
``````

***

## 📖 Core Concepts Explained

### **The Three Pillars of Stateful Agents**

#### 1. **Tools** - Agent hands and eyes
- **Function tools** - Custom Python functions
- **Built-in tools** - Google Search, Code Execution
- **Agent tools** - Agents calling other agents

#### 2. **Context Engineering** - Smart information assembly
- Dynamically fetch relevant memory
- Load tool definitions
- Prevent context rot with summarization

#### 3. **Memory** - Personalization over time
- **Declarative memory** - Facts about users
- **Procedural memory** - How to do things
- **ETL pipeline** - Consistency and quality

***

## 🛠️ Technologies Used

| Technology | Purpose |
|-----------|---------|
| [Google ADK](https://google.github.io/adk-docs/) | Agent Development Kit |
| [Gemini API](https://ai.google.dev/) | LLM backbone |
| [Kaggle Notebooks](https://www.kaggle.com/notebooks) | Learning environment |
| [LangGraph](https://langchain-ai.github.io/langgraph/) | Agent orchestration (alternative) |
| [Pydantic](https://docs.pydantic.dev/) | Type hints & validation |

***

## 🎓 Learning Resources

| Resource | Type | Link |
|----------|------|------|
| Official Course | Video | [Google AI Agents Intensive](https://rsvp.withgoogle.com/events/google-ai-agents-intensive_2025) |
| ADK Documentation | Docs | [google.github.io/adk-docs](https://google.github.io/adk-docs/) |
| Kaggle Community | Discord | [Kaggle Discord Server](https://discord.gg/kaggle) |
| Gemini API Guide | Tutorial | [ai.google.dev](https://ai.google.dev/) |

***

## 👥 Community & Contribution

### Bangladesh AI Community

This repository is maintained by the **Machine Learning, AI, Deep Learning & NLP Community - Bangladesh** (part of Google AI Community Network).

**📍 Join us:**
- **Discord:** [Kaggle Discord Server](https://discord.gg/kaggle)
- **LinkedIn:** [ML/AI/DL/NLP Community Bangladesh](https://www.linkedin.com/groups/13986331/)
- **🕐 Weekly Livestreams:** Thursdays at 1 AM UTC+6

### Contributing

We welcome contributions! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

**Ways to contribute:**
- 📝 Add codelab solutions
- 🐛 Report issues & suggest improvements
- 🎓 Share your own agent examples
- 💬 Answer community questions
- 🌍 Translate resources to other languages

***

## 📊 Repository Stats

![GitHub Stars](https://img.shields.io/github/stars/azaynul10/google-ai-agents-intensive-5days?style=flat.io/github/forks/azaynul10/google-



![GitHub Issues](https://img.shields.io/github/issues/azaynio/github/last-commit/azaynul10/google-ai-agents-intensive-5days 💡 Code Examples

### Currency Converter Agent (Day 2)

```python
# See: codelabs/day-2a-agent-tools/currency_agent_example.py
from google.adk.agents import LlmAgent
from google.adk.models.google_llm import Gemini

agent = LlmAgent(
    name="currency_agent",
    model=Gemini(model="gemini-2.5-flash-lite"),
    tools=[get_fee_for_payment_method, get_exchange_rate],
)

result = agent.run("Convert 1,250 USD to INR using Bank Transfer")
# Output: "The final converted amount is 103,199.10 INR..."
``````

### Multi-Agent System (Day 2)

```
# See: examples/multi-agent-system/
from google.adk.tools import AgentTool

enhanced_currency_agent = LlmAgent(
    name="enhanced_currency_agent",
    tools=[
        get_fee_for_payment_method,
        get_exchange_rate,
        AgentTool(agent=calculation_agent),  # Agent as tool!
    ],
)
``````

***

## 🎖️ Highlights

- ✅ **Complete** - All 5 days of materials covered
- 📚 **Well-documented** - Detailed explanations for each concept
- 🔬 **Hands-on** - Working code examples & codelabs
- 🤝 **Community-driven** - Expert questions & answers
- 🌍 **Accessible** - Beginner-friendly with advanced depth
- 🚀 **Production-ready** - Real-world deployment strategies

***

## 📁 Repository Structure

```
docs/                → Conceptual guides & explanations
whitepapers/         → Official Google X Kaggle whitepapers
codelabs/            → Hands-on notebooks & code
examples/            → Real-world agent implementations
resources/           → Best practices & patterns
expert-questions/    → Community Q&A with responses
community/           → Community guidelines & events
setup/               → Installation & configuration
``````

---

## 📄 License

This repository is licensed under the [Apache License 2.0](./LICENSE), matching the official course materials.

---

## 🤝 Acknowledgments

Special thanks to:
- **Google** & **Kaggle** for the amazing 5-day course
- **[Kanchana Patlolla](https://linkedin.com/in/kanchana-patlolla)** & **[Anant Nawalgaria](https://linkedin.com/in/anant-nawalgaria)** for course facilitation
- **Expert speakers:** Julia Wiesinger, Jay Alammar, Steven Johnson, Kimberly Milam, and others
- **Bangladesh AI Community** for collaborative learning
- **All contributors** from around the world

---

## ❓ FAQ

**Q: Do I need a Google API key?**

A: Yes, for Gemini API calls. [Get one free here](https://aistudio.google.com/app/api-keys) (no credit card required for free tier).

**Q: Can I use this for commercial projects?**

A: The code examples are Apache 2.0 licensed, so yes. See [LICENSE](./LICENSE) for full details.

**Q: How do I run the codelabs?**

A: See [SETUP.md](./setup/SETUP.md) for detailed step-by-step instructions.

**Q: Can I contribute?**

A: Absolutely! Read [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

**Q: What Python version is required?**

A: Python 3.10 or higher.

---

## 📞 Support

- **📝 GitHub Issues:** [Report a bug or request a feature](https://github.com/azaynul10/google-ai-agents-intensive-5days/issues)
- **💡 GitHub Discussions:** [Ask questions or share ideas](https://github.com/azaynul10/google-ai-agents-intensive-5days/discussions)
- **🔗 Discord Community:** [Join Kaggle Discord](https://discord.gg/kaggle)

---

## 📢 Share Your Work

Built something cool with agents? Share it with the community!

```
#AIAgents #GoogleAI #Kaggle #AIBANGLADESH #MachineLearning #AgentDevelopment
``````

***

## 🔗 Related Resources

- [ADK GitHub Repository](https://github.com/google/adk)
- [Gemini API Documentation](https://ai.google.dev/docs)
- [LangChain Documentation](https://python.langchain.com/)
- [Model Context Protocol](https://modelcontextprotocol.io/)

***

**Last Updated:** November 14, 2025  
**Maintained by:** Machine Learning, AI, Deep Learning & NLP Community - Bangladesh  
**Status:** ✅ Active & Growing  

***

*This repository is a community-driven resource created by learners for learners. If you find it helpful, please give it a ⭐ and share with others!*
```

---

## **CONTRIBUTING.md - Corrected Version**

``````markdown
# Contributing to Google AI Agents Repository

Welcome! We're excited to have you contribute to this learning resource. 🎉

## Table of Contents

- [How to Contribute](#how-to-contribute)
- [Pull Request Process](#pull-request-process)
- [Code of Conduct](#code-of-conduct)
- [Community Guidelines](#community-guidelines)

---

## How to Contribute

There are many ways to contribute, regardless of your skill level:

### 1. Add Codelab Solutions

Help others by sharing your solutions to the codelabs:

```
# Fork the repo, then:
cd codelabs/day-X/solutions/
# Add your solution files
git add .
git commit -m "Add Day X solution with detailed comments"
git push origin feature/day-x-solution
``````

**Guidelines:**
- Include comments explaining key concepts
- Follow Python PEP 8 style guide
- Test your code before submitting
- Reference the original problem

### 2. Share Agent Examples

Create new real-world agent implementations:

```bash
cd examples/
mkdir my-agent-name/
# Add implementation files and README
``````

**Guidelines:**
- Create a descriptive README with use case
- Include working code example
- Document any external dependencies
- Add your example to main [README.md](../README.md)

### 3. Improve Documentation

Help make documentation clearer and more accessible:

- Fix typos and grammar
- Clarify confusing explanations
- Add diagrams or visualizations
- Suggest better organization
- Update outdated references

### 4. Answer Expert Questions

Share your insights and expertise:

- Add responses to `expert-questions/day-X.md`
- Include references and citations
- Tag relevant experts or resources
- Explain from multiple perspectives

### 5. Report Issues

Found a bug or want to suggest improvements?

- Check if the issue already exists
- Provide clear description and steps to reproduce
- Include error messages and screenshots
- Suggest a fix if possible

---

## Pull Request Process

### Step 1: Fork and Clone

```
# Fork the repository on GitHub
git clone https://github.com/YOUR-USERNAME/google-ai-agents-intensive-5days.git
cd google-ai-agents-intensive-5days
git remote add upstream https://github.com/azaynul10/google-ai-agents-intensive-5days.git
``````

### Step 2: Create a Feature Branch

```bash
# Keep main clean by creating feature branches
git checkout -b feature/your-feature-name
# Good examples:
# - feature/day-2-solution
# - docs/improve-memory-explanation
# - example/chatbot-agent
``````

### Step 3: Make Changes

- Make small, focused commits
- Write clear, descriptive commit messages
- Test your changes thoroughly
- Follow existing code style

### Step 4: Commit and Push

```
# Example commits:
git commit -m "Add Day 2a currency converter solution with explanations"
git commit -m "Fix typo in context engineering guide"
git commit -m "Add real-world travel booking agent example"

# Push to your fork
git push origin feature/your-feature-name
``````

### Step 5: Create Pull Request

1. Go to GitHub and open a Pull Request
2. Use a clear, descriptive title
3. Reference any related issues (`Closes #123`)
4. Describe what you changed and why
5. Highlight key learnings or insights

**Good PR Title Examples:**
- `Add Day 3 memory consolidation codelab solution`
- `Fix context engineering explanation in docs`
- `Add customer support agent example`

### Step 6: Review and Merge

- Respond to feedback from maintainers
- Make requested changes
- Once approved, your PR will be merged! 🎉

***

## Code of Conduct

### Our Commitment

We are committed to providing a welcoming and inspiring community for all.

### Expected Behavior

- **Be respectful** - Treat everyone with kindness and courtesy
- **Be inclusive** - Welcome people of all backgrounds and experience levels
- **Help others learn** - Share knowledge generously
- **Give credit** - Always acknowledge and cite sources
- **Be constructive** - Provide helpful feedback and suggestions

### Unacceptable Behavior

- Harassment or discrimination
- Disrespectful or offensive language
- Plagiarism or uncredited work
- Spam or promotional content
- Any form of abuse

### Reporting Issues

If you experience or witness unacceptable behavior:
- Contact maintainers privately
- Email: [community email if applicable]
- Discord: Report to moderators

***

## Community Guidelines

### For Everyone

- 💬 Ask questions - No question is too basic
- 🤝 Help others - Share what you've learned
- 📚 Cite sources - Give credit to resources
- 🌟 Be positive - Encourage and support others

### For Contributors

- Write clear, well-documented code
- Follow existing style conventions
- Test before submitting
- Be open to feedback
- Update documentation

### For Maintainers

- Respond promptly to issues and PRs
- Provide constructive feedback
- Merge quality contributions
- Maintain code quality standards
- Foster inclusive community

***

## Getting Help

**Questions about contributing?**
- Check [FAQ](../README.md#faq)
- Ask in [GitHub Discussions](https://github.com/azaynul10/google-ai-agents-intensive-5days/discussions)
- Join [Kaggle Discord](https://discord.gg/kaggle)

**Getting started?**
- Read [SETUP.md](../setup/SETUP.md)
- Try a codelab first
- Start small with documentation improvements

***

## Contributor Acknowledgment

All contributors are recognized in:
- [README.md](../README.md) Acknowledgments
- [CONTRIBUTORS.md](./CONTRIBUTORS.md) (coming soon)
- [GitHub Contributors Graph](https://github.com/azaynul10/google-ai-agents-intensive-5days/graphs/contributors)

***

## Additional Resources

- [ADK Contributing Guide](https://google.github.io/adk-docs/contributing/)
- [GitHub's Open Source Guide](https://opensource.guide/)
- [How to Write Good Commit Messages](https://cbea.ms/git-commit/)

***

## Thank You! 🙏

Your contributions make this community stronger. We appreciate:
- Your time and effort
- Your passion for AI agents
- Your commitment to learning and teaching
- Your respect for our values

***

**Happy Contributing!**

*For questions or concerns, reach out to the maintainers on [Discord](https://discord.gg/kaggle) or open an issue.
