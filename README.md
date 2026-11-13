# queryPilot

queryPilot is a multi-agent AI system that turns plain English questions into SQL queries and explains how they work.

It bridges the gap between complex relational schemas and human-friendly natural language, enabling developers, analysts, and business users to explore data conversationally without writing a single line of SQL.

> Vision: Democratize data access — make querying as simple as having a conversation.



## 🧩 Key Highlights
- Multi-Agent Orchestration: Modular agentic pipeline — intent detection, table identification, column pruning, SQL generation, and explanation — each powered by structured LLM calls.
- Context-Aware Querying: Maintains chat history and dynamically enhances prompts to handle follow-ups and modifications intelligently.
- Schema-Constrained Generation: Every SQL is schema-validated — no hallucinated tables or columns.
- Explainable AI Queries: Each generated SQL comes with a concise, human-readable explanation.
- Extensible: Add agents to the query pipeline or adapt the database connector.


## 🧱 System Architecture

The application uses a multi-agent system where each agent has a specialized role. The process is orchestrated by a backend Flask API and presented to the user through a simple frontend.

![queryPilot architecture](assets/architecture.png)

### Dashboard / User Interface Screenshots

#### Main Chat Interface
![Main Chat Interface](assets/dashboard-1.png)

#### SQL Query Result
![Query Result](assets/dashboard-2.png)

#### Additional Features
![Dashboard Analytics](assets/dashboard-3.png)

## 💼 Use Cases

*   **Rapid Prototyping:** Developers can quickly generate complex queries needed for new application features.
*   **Data Exploration:** Analysts can perform ad-hoc analysis without writing boilerplate SQL.
*   **Business Intelligence:** Business users can get answers to questions like "How many new users signed up last week?" without waiting for an analyst.
*   **Learning SQL:** Junior developers or students can use the agent as a tool to learn SQL by seeing how their questions translate into code.

## ⚡ Getting Started

1. Clone the repository and install dependencies in a virtual environment.
    ```bash
    git clone https://github.com/Achyuth5689/queryPilot.git
    cd queryPilot
    python3 -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt
    ```
2. In a local `.env` file, set `GEMINI_API_KEY`, `GEMINI_MODEL`, and `DB_TYPE=mysql`. Set `DB_HOST`, `DB_PORT`, `DB_USER`, `DB_PASSWORD`, and `DB_NAME` to your MySQL connection settings.
3. Start the development server.
    ```bash
    PORT=5000 ./devserver.sh
    ```
4. Open `http://localhost:5000` in your browser.

## 🛣️ Roadmap: The Future of Conversational Data

This project is just the beginning. Our future plans include:

*   [ ] **Support for More SQL Dialects:** Adding support for PostgreSQL, MySQL, and others.
*   [ ] **Data Visualization:** Automatically generating charts and graphs to visualize the query results.
*   [ ] **Query History & Saving:** Allowing users to save and reuse frequently asked questions.
*   [ ] **Advanced Data Context:** Enabling the agent to understand more complex relationships and business-specific logic.
*   [ ] **Integration with BI Tools:** Connecting the agent to popular BI platforms.

## 🤝 Contributing

Open an issue or pull request in this repository to suggest a change.

## Maintainer

[Achyuth5689](https://github.com/Achyuth5689)
