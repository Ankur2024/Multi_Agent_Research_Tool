# Multi-Agent AI Research System

An autonomous AI-powered research assistant built using LangChain that performs end-to-end web research, content extraction, report generation, and quality evaluation through a coordinated multi-agent workflow.

## Overview

This project demonstrates how multiple AI agents can collaborate to automate the research process. Instead of relying on a single LLM prompt, the system decomposes the task into specialized agents responsible for searching, reading, writing, and reviewing information.

The workflow mimics advanced "Deep Research" systems by gathering information from the web, extracting relevant content, generating structured reports, and automatically evaluating report quality.

## Features

* Real-time web search using Tavily Search API
* Automated webpage scraping using BeautifulSoup
* Multi-agent architecture powered by LangChain
* Structured report generation
* Automated report review and scoring
* Source attribution and citation tracking
* Streamlit-based user interface
* Modular and extensible pipeline design

---

## Architecture

### Search Agent

Responsible for searching the web and collecting relevant URLs and resources related to the research topic.

### Reader Agent

Scrapes webpages and extracts clean textual content for analysis.

### Writer Chain

Processes gathered information and generates a structured professional research report.

### Critic Chain

Evaluates the generated report and provides:

* Quality assessment
* Completeness review
* Improvement suggestions
* Overall score out of 10

---

## Workflow

User Query
↓
Search Agent
↓
Web Search Results
↓
Reader Agent
↓
Extracted Content
↓
Writer Chain
↓
Research Report
↓
Critic Chain
↓
Final Report + Quality Score

---

## Project Structure

```text
multi_agent_research_tool/
│
├── agents.py          # Agent definitions
├── tools.py           # Search and scraping tools
├── pipeline.py        # Research workflow orchestration
├── app.py             # Streamlit UI
├── main.py            # Backend execution logic
├── requirements.txt   # Project dependencies
├── .env.example       # Environment variable template
│
├── outputs/
│   └── generated_reports/
│
└── README.md
```

## Technologies Used

### Frameworks

* LangChain
* Streamlit

### LLM Providers

* OpenAI
* Hugging Face
* DeepSeek (optional)

### Tools & Libraries

* Tavily Search API
* BeautifulSoup4
* Requests
* Python Dotenv
* Pydantic

---

## Installation

### Clone Repository

```bash
git clone https://github.com/your-username/multi-agent-ai-research-system.git

cd multi-agent-ai-research-system
```

### Create Virtual Environment

```bash
python -m venv .venv
```

Activate:

Windows

```bash
.venv\Scripts\activate
```

Linux / Mac

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file in the root directory.

```env
TAVILY_API_KEY=your_tavily_api_key
OPENAI_API_KEY=your_openai_api_key
```

---

## Running the Application

### Streamlit UI

```bash
streamlit run app.py
```

### FastAPI Backend (Optional)

```bash
uvicorn main:app --reload
```

---

## Example Research Query

```text
Impact of Generative AI on Healthcare Industry
```

### Output

The system automatically:

1. Searches relevant sources
2. Scrapes content
3. Extracts key insights
4. Generates a structured report
5. Reviews report quality
6. Returns a final research score

---

## Sample Report Sections

* Executive Summary
* Key Findings
* Industry Analysis
* Opportunities
* Risks and Challenges
* Future Trends
* References

---

## Key Learning Outcomes

* Multi-Agent System Design
* LangChain Expression Language (LCEL)
* Tool Calling and Agent Orchestration
* State Management Between Agents
* Web Search Integration
* Automated Content Extraction
* Report Generation Pipelines
* Streamlit Application Development

---

## Future Improvements

* LangGraph Integration
* Vector Database Memory
* PDF Report Export
* Citation Verification
* Multi-Source Fact Checking
* Parallel Agent Execution
* RAG-based Knowledge Retrieval

---

## Author

Ankur Gupta

Data Analyst | AI & ML Enthusiast | Building Intelligent Multi-Agent Systems

---

If you found this project useful, consider giving it a star on GitHub.
