# Customer Support Agent

## Overview
The **Customer Support Agent** is an AI-powered support system built using **LangChain**, **LangGraph**, and **Gradio**. It integrates multiple AI agents to handle customer queries efficiently, ensuring accurate categorization, sentiment analysis, and automated response generation. The system also features an escalation mechanism to transfer complex or negative-sentiment queries to human agents.

## Features
- **State Management**: Utilizes `TypedDict` to define and manage customer interaction states.
- **Query Categorization**: Classifies queries into **Technical**, **Billing**, or **General** categories.
- **Sentiment Analysis**: Determines the emotional tone of customer queries.
- **Response Generation**: Provides automated responses based on query category and sentiment.
- **Escalation Mechanism**: Escalates negative sentiment queries to human agents.
- **Workflow Graph**: Uses **LangGraph** to create a flexible and extensible workflow.

## Method Details
### 1. Initialization
- Set up the environment and import necessary libraries.

### 2. State Definition
- Define a structured state using `TypedDict` to store query details, category, sentiment, and response.

### 3. Node Functions
- Implement individual functions for:
  - Query categorization
  - Sentiment analysis
  - Handling technical queries
  - Handling billing queries
  - Handling general queries
  - Escalating critical issues

### 4. Graph Construction
- Utilize `StateGraph` to define the customer support workflow.
- Add nodes and edges to represent query handling steps.

### 5. Conditional Routing
- Route queries based on category and sentiment analysis results.

### 6. Workflow Compilation
- Compile the LangGraph workflow into an executable support agent.

### 7. Execution
- Process customer queries through the workflow and return responses.

## Workflow
```plaintext
("categorize", categorize)
("analyze_sentiment", analyze_sentiment)
("handle_technical", handle_technical)
("handle_billing", handle_billing)
("handle_general", handle_general)
("escalate", escalate)
```

![Workflow](/workflow/diagram)

## Technologies Used
- **LangChain**: For conversational AI capabilities.
- **LangGraph**: For creating the structured customer support workflow.
- **Gradio**: For an interactive chat-based user interface.

## Usage
1. Open the chat interface in your browser.
2. Type your query (Technical, Billing, or General).
3. The system will categorize your query, analyze sentiment, and generate a response.
4. If required, queries with negative sentiment will be escalated to a human agent.

