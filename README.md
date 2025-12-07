# LangGraph Chatbot with Tavily AI Integration

This project demonstrates building a conversational AI agent (chatbot) using [LangGraph](https://langchain.com/langgraph), a library for building stateful, multi-actor applications with LLMs. It also showcases integration with [Tavily AI](https://tavily.com/) for enhanced web search capabilities and explores the "Reflection & Critique" pattern for improving agent responses.

## Features

*   **LangGraph Chatbot**: A basic chatbot implementation using [`StateGraph`](main.ipynb) and [`ChatOpenAI`](main.ipynb) (`gpt-4o-mini` model).
*   **Graph Visualization**: Visualize the LangGraph agent's structure using Mermaid and ASCII diagrams. The notebooks include examples to draw the graph with `graph.get_graph().draw_mermaid_png()` and `graph.get_graph().draw_ascii()`.
*   **Tavily AI Integration**: Utilizes the [`TavilyClient`](main.ipynb) (or `TavilySearchResults` tool) for web search and question-answering, demonstrating how to fetch relevant information and integrate it into the agent's workflow.
*   **Reflection & Critique Pattern**: An example of how to implement a reflection agent to analyze search results and generate structured reports, enhancing the quality of AI-generated content. This pattern involves an AI system evaluating and critiquing its own outputs to generate improved versions. This is demonstrated in both [main.ipynb](main.ipynb) and [tweet-generator.ipynb](tweet-generator.ipynb) for different use cases (report generation and tweet refinement).
*   **Persistent Memory**: The chatbot incorporates memory using [`SqliteSaver`](main.ipynb) (or [`MemorySaver`](main.ipynb)) to maintain conversational context across turns.
*   **Langsmith Tracing**: The [tweet-generator.ipynb](tweet-generator.ipynb) notebook includes examples of using [`@traceable`](tweet-generator.ipynb) from `langsmith` to trace the execution of the agent.
*   **Environment Variable Management**: Securely handles API keys using `.env` files.

## Setup

Follow these steps to set up and run the project locally.

### Prerequisites

*   Python 3.8+
*   pip

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/py-langgraph.git
cd py-langgraph