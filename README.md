# AI Agent Subtitle Downloader

A **LangGraph-powered multi-agent system** for automated TV series subtitle discovery, analysis, and matching.  
This project focuses on **explicit workflow orchestration**, decision routing, and integration with external services (e.g. Sonarr), rather than simple linear scripts.

---

## 🚀 Overview

This project implements an **agent-based workflow** that:
1. Identifies a TV series
2. Fetches metadata and episode information
3. Searches and analyzes available subtitles
4. Makes decisions based on confidence and ambiguity
5. Matches or downloads the most suitable subtitle automatically

The system is built using **LangGraph** to model the workflow as a **state machine with conditional routing and fallback paths**.

---

## 🧠 Architecture

The core design uses **specialized agents**, each responsible for a single concern:

- **Get_Series_Name** — Resolves and normalizes series input
- **Get_Series_Data** — Fetches metadata and season information
- **Get_Series_Subtitle** — Searches subtitle providers
- **Get_Series_Episode** — Maps subtitles to episodes
- **Analyze_Subtitle** — Evaluates subtitle quality and relevance
- **Analyze_Multi** — Handles ambiguous or multiple matches
- **Matcher_Agent** — Matches subtitles to episodes
- **Decider_Agent** — Central decision node that routes execution paths
- **Handle_Unknown** — Fallback for unresolved or low-confidence cases

The workflow is **non-linear** and adapts dynamically based on agent outputs.

---

## 🔁 Workflow Diagram

The system flow is defined as a LangGraph graph with explicit start/end states, decision nodes, and fallback paths:

> _![LangGraph Workflow](https://github.com/0c33/Ai-Agent-Subtitle-Downloader/blob/main/langgraph_workflow.png)_

This approach improves:
- Debuggability
- Control over execution paths
- Extensibility for new agents or tools

---

## ⚙️ Why LangGraph?

LangGraph was chosen to:
- Represent agent orchestration as a **graph instead of ad-hoc logic**
- Enable **conditional branching and retries**
- Separate reasoning, execution, and decision-making clearly

This project complements framework-free agent experiments by showing how the same ideas scale using structured orchestration.

---

## 🧪 Goals of This Project

- Explore **agent-based automation** beyond simple prompting
- Practice **decision-centric system design**
- Integrate AI agents with **real-world tools and services**
- Compare framework-based vs custom agent architectures

---

## 🛠️ Tech Stack

- **Python**
- **LangGraph**
- External integrations (e.g. Sonarr, subtitle providers)
- Modular agent design

---

## 📌 Notes

This is an **engineering-focused project**, not a UI application.  
The emphasis is on **workflow design, agent interaction, and system reasoning**.

---

## 📄 License

MIT
