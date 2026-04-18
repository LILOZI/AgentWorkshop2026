# Workshop Notebooks — LangGraph Agent Development

This workshop is built around two main notebooks.
Together, they introduce the core ideas behind LLM agent systems using **LangGraph `StateGraph`**, while keeping the workflow explicit, readable, and practical.

The goal is not just to show how to call an LLM with tools, but to help students understand how to build a **stateful agent workflow** with:
- explicit state,
- clear node responsibilities,
- reusable tools,
- visible control flow,
- loops and stopping conditions,
- and simple observability.

These notebooks are designed for students with general Python knowledge, but no prior experience with LangGraph, Ollama, or agent frameworks.

For more useful sources and examples, [jump here](#future-reading-and-appendices)

---

## Workshop Flow

The workshop progresses from a smaller, beginner-friendly agent to a more realistic collection-and-analysis workflow.

### 1. `01_agent_1_agentic_retrieval_arxiv.ipynb`
A first hands-on agent built with LangGraph and a real public API.

This notebook introduces the core mechanics of an agent workflow:
- defining graph state,
- writing node functions,
- using a retrieval tool,
- making decisions,
- routing conditionally,
- looping when more information is needed,
- and producing a final answer.

It is intentionally compact, but it already behaves like a real agent rather than a toy chatbot.

### 2. `02_agent_2_security_collection_nvd_github.ipynb`
A more realistic agent pipeline for collection, filtering, and analysis.

This notebook extends the same LangGraph ideas into a workflow that is closer to the course assignment. It separates the system into clear stages such as:
- planning,
- source discovery,
- fetching,
- validation,
- signal extraction,
- logging,
- and stopping logic.

It is meant to feel more like an actual agent system that could later evolve into a continual security or malware-related pipeline.

---

## What Students Should Learn

By the end of these notebooks, students should be able to:
- understand what agent **state** is and why it matters,
- break agent behavior into focused **nodes**,
- connect nodes with explicit **graph transitions**,
- integrate simple **tools** into the workflow,
- design iterative flows with retries and stopping conditions,
- and recognize how these ideas scale into more realistic autonomous systems.

---

## Design Philosophy

The workshop deliberately emphasizes **clarity over abstraction**.

That means the main notebooks favor:
- **LangGraph `StateGraph`**,
- explicit typed state,
- plain Python functions,
- simple prompt construction,
- and visible control flow.

The workshop does **not** center the teaching around higher-level agent wrappers, middleware-heavy designs, or hidden framework logic.

The intention is to make the agent architecture understandable enough that students can later extend it safely for the course exercise.

---

## Relation to the Course Exercise

These notebooks are not the final project themselves.
They are the foundation for it.

The course exercise asks students to build an autonomous LangGraph-based system that continually collects, analyzes, and improves over time in a malware-detection setting.

The notebooks support that goal by teaching the same underlying building blocks in a smaller and more approachable form:
- workflow design,
- tool integration,
- iterative decision-making,
- validation,
- extraction,
- logging,
- and system structure.

---

## Future Reading and Appendices

The following section contains links to LangGraph documentation and agent examples, along with other blog posts or videos.\
It elaborates on topics we touched on in class and more.\

> Note that all LangChain YT videos have links to detailed video notes and github repositories, it is important that you check them as well.\
>Some implementations are marked as `failed`, in that case, you should only learn from the theoretical side and the idea behind the implementation and not the actual implementation.\
>Remember, abstractions can make developing "easy", but impossible to solve real complex problems.
> 

#### Agent Design Principles
- [IBM Technology: The 7 Skills You Need to Build AI Agents](https://www.youtube.com/watch?v=mtiOK2QG9Q0)

#### State reducers & Pydantic models & Structured Output
- [LangChain: LangGraph Agents with Structured Output](https://www.youtube.com/watch?v=0i9NzY_b3pg&t)
- [LangChain Documentation: Graph API overview](https://docs.langchain.com/oss/python/langgraph/graph-api)

#### Tool abstraction
- [LangGraph Documentation: Tools](https://docs.langchain.com/oss/python/langchain/tools)

#### Prompt Engineering & Context Engineering
- [IBM Technology: Context Engineering vs. Prompt Engineering: Smarter AI with RAG & Agents](https://www.youtube.com/watch?v=vD0E3EUb8-8)
- [LangChain: Context Engineering for Agents](https://www.youtube.com/watch?v=4GiqzUHD5AA)

#### More Agent Examples
- [LangChain: Building a fully local research assistant from scratch with Ollama](https://www.youtube.com/watch?v=XGuTzHoqlj8&t)
- [LangChain: Building Effective Agents With LangGraph](https://www.youtube.com/watch?v=aHCDrAbH_go&t)
- [LangChain: LangGraph Template: Multi-Agent RAG Research](https://www.youtube.com/watch?v=JLDLANs_m_w&t)

#### Long vs Short term Memory
- [LangChain: Memory for agents (conceptual video)](https://www.youtube.com/watch?v=JTL0yp85FsE)
- [Long-Term Memory Agent Template](https://www.youtube.com/watch?v=-xkduCeudgY&t)

#### Checkpointers
- [LangChain: LangGraph: Persistance](https://www.youtube.com/watch?v=YE6A5d8kNp4)
- [LangGraph Documentation: Persistance](https://docs.langchain.com/oss/python/langgraph/persistence)

#### Human In The Loop
- [LangChain: LangGraph Agents - Human-In-The-Loop - User Feedback](https://www.youtube.com/watch?v=YmAaKKlDy7k)

---

## Notes for Students

You are not expected to memorize every LangGraph feature from these notebooks.
The main goal is to leave the workshop with a strong mental model of how an agent system is constructed:

- state holds the working memory,
- nodes perform focused steps,
- tools provide capabilities,
- edges define the workflow,
- and the graph controls the overall behavior.

Once that model is clear, it becomes much easier to build more advanced systems later.
