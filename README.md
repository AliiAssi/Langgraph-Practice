# 🔄 LangGraph Course Practice
![LangGraph Logo](https://miro.medium.com/v2/resize:fit:1400/1*Z1NtI1D-YEGBJfb7bW4MIA.png)

## 📋 Overview

This repository contains several examples demonstrating how to build powerful and dynamic AI agents using LangGraph, a library for creating stateful, multi-actor applications with LLMs. These examples showcase various features, from integrating local models and external tools to implementing human-in-the-loop workflows and managing conversational memory.

### Examples

#### 1\. Stateful Conversational AI with Mistral and Arithmetic Tools

This example illustrates how to build a stateful, conversational AI agent that can perform a sequence of arithmetic operations. It leverages LangGraph with a Mistral large language model.

**Key Features:**

  * **Arithmetic Tools**: Defines basic Python functions (add, multiply, divide) that the LLM can call as tools.
  * **Graph Construction**: Constructs a graph with "assistant" and "tool" nodes for decision-making and execution.
  * **Conversational Memory**: Utilizes a `MemorySaver` checkpointer to maintain conversation context, allowing the agent to remember previous results and handle follow-up commands (e.g., "Multiply that by 2").

#### 2\. Local LLM Integration with Ollama and Tavily Search

This example guides you through setting up and using a local Llama 3 model with the LangChain framework by leveraging Ollama.

**Key Features:**

  * **Local LLM Setup**: Instructions for installing Ollama and pulling the `llama3` model.
  * **LangChain Integration**: Connects to the local model using `langchain-ollama` for text generation.
  * **Tool-Based Information Retrieval**: Incorporates the Tavily Search API as a tool to execute search queries and present results in a structured table using `tabulate`.

#### 3\. Human-in-the-Loop Agent with LangGraph

This example demonstrates how to build a Human-in-the-Loop agent using the LangGraph framework, enabling AI to pause and request human input.

**Key Features:**

  * **Custom Human Assistance Tool**: A `human_assistance` tool is created to intentionally trigger an interrupt in the graph when invoked by the ChatGroq LLM.
  * **Resume Functionality**: Shows how a user can provide a response, which is then injected back into the graph using a `resume` command.
  * **Contextual Understanding**: The LLM incorporates human guidance into its final answer while maintaining conversational context with a `MemorySaver`.

#### 4\. Groq Llama 3 Integration with Custom Tools

This example details the creation of a LangGraph application that integrates a Groq Llama 3 large language model with a custom tool.

**Key Features:**

  * **Groq and LangSmith Integration**: Setup includes configuring API keys for Groq and LangSmith.
  * **Custom Tool Definition**: Defines an `add` tool for numerical addition that the LLM can invoke.
  * **Intelligent Routing**: The graph routes user queries, allowing the LLM to answer general questions directly or trigger a tool call to the `add` function for numerical operations.
  * **Stateful Conversational Flow**: Demonstrates how the LLM delegates tasks, processes tool output, and provides coherent responses within a stateful conversation.

#### 5\. Iterative Chatbot Development with Groq DeepSeek Llama 70B

This example showcases the iterative development of a LangGraph chatbot using Groq's DeepSeek Llama 70B model, progressing from a basic agent to one with advanced capabilities.

**Key Features:**

  * **Basic Conversational Agent**: Starts with a fundamental chatbot implementation.
  * **External Tool Integration**: Integrates Tavily Search for web lookup and custom arithmetic functions (add, multiply).
  * **ReAct-like Pattern**: Implements a ReAct-like pattern where the graph loops back to the LLM after a tool call, enabling multi-step reasoning and complex task execution.
  * **Enhanced with Memory**: Utilizes LangGraph's `MemorySaver` to maintain conversational context, allowing the chatbot to recall previous interactions and user information.

-----

## 📚 Resources

  * [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
  * [LangChain Documentation](https://python.langchain.com/)
  * [Ollama Documentation](https://ollama.ai/docs)

-----

## 🤝 Contributing

Feel free to fork this repository and submit pull requests with improvements or additional examples using other open-source LLMs.
