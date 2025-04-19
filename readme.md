# Market Trend Analyzer with CrewAI + AgentOps

This project demonstrates how to build a simple multi-agent system using [CrewAI](https://github.com/joaomdmoura/crewAI) to analyze market data and conduct research. Each agent has a dedicated task, and their collaboration results in an insightful market analysis report. The execution is tracked using [AgentOps](https://agentops.ai) for observability.

---

## Features

- Two specialized AI agents (Data Analyst & Market Researcher)
- Well-defined tasks for each agent
- Sequential task execution using `CrewAI`
- AgentOps integration for LLM traceability and performance monitoring

---

## Agents Overview

1. **Data Analyst**  
   - Goal: Analyze data trends in the market  
   - Background: Experienced economist with deep data insight

2. **Market Researcher**  
   - Goal: Gather and summarize market dynamics  
   - Background: Meticulous researcher skilled at synthesis

---

## 🧪 Tasks

1. **Collect Data Task**  
   - Collect recent market data and identify key trends

2. **Market Research Task**  
   - Research and analyze factors affecting market dynamics

---

## 🛠️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Create and Activate a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
# or directly
pip install 'crewai[agentops]'
```

### 4. Add Your API Key

Create a `.env` file in the root directory:

```env
AGENTOPS_API_KEY=your_agentops_api_key_here
```

> 🔑 Get your key from [AgentOps Dashboard](https://app.agentops.ai/settings/projects)

---

## ▶️ Run the App

```bash
python your_script_name.py
```

You’ll see a printout of the task results once the crew finishes.

---

## 📦 Folder Structure

```
├── .env
├── market_crew.py         # Main script (rename as needed)
├── README.md
└── requirements.txt
```

---

## 📈 Output

Example result:
```
[Data Analyst] Finished Collect Data Task: Summary of market trends...
[Market Researcher] Completed analysis of market influencers...
```

---

## 📋 Notes

- Set `instrument_llm_calls=True` to trace interactions with LLMs using AgentOps
- Crew is run in **sequential** mode using `Process.sequential`

---

## 🙏 Acknowledgements

- [CrewAI](https://github.com/joaomdmoura/crewAI)
- [AgentOps](https://agentops.ai)
- [LangChain](https://www.langchain.com/)

---

- Note: crewai will automatically detect the openai_api_key and no need to pass in the py file. because it uses default llm opeai

