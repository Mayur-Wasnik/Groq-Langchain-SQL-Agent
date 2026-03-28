# Lang SQL Agent

A natural language SQL database agent built with LangChain and Groq, powered by Streamlit. This application allows users to interact with a SQLite database using conversational language for task management.

## Features

- **Natural Language Processing**: Convert natural language queries to SQL
- **Task Management**: CRUD operations on a tasks database
- **AI-Powered**: Uses Llama-3.1-8b via Groq for intelligent query understanding
- **Interactive UI**: Built with Streamlit for an intuitive user interface
- **Memory Management**: In-memory checkpointer for conversation context

## Prerequisites

- Python 3.8 or higher
- Groq API key

## Installation

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

Create a `.env` file in the project root with your Groq API key:
```
GROQ_API_KEY=your_api_key_here
```

## Usage

Run the Streamlit application:
```bash
streamlit run app.py
```

The application will start a local server (typically at `http://localhost:8501`) where you can interact with the SQL agent.

## Database Schema

The application comes with a pre-configured `tasks` table:

| Column      | Type      | Description                              |
|-------------|-----------|------------------------------------------|
| id          | INTEGER   | Primary key, auto-incremented            |
| title       | TEXT      | Task title (required)                    |
| description | TEXT      | Task description                         |
| status      | TEXT      | Task status (pending/in_progress/completed) |
| created_at  | TIMESTAMP | Creation timestamp                       |

## Supported Operations

- **List tasks**: View all tasks with filtering and sorting
- **Create task**: Add new tasks with title and description
- **Update task**: Modify task status or details
- **Delete task**: Remove tasks by ID or title

## Technologies Used

- **LangChain**: Framework for building LLM applications
- **Groq**: Fast LLM inference engine
- **Streamlit**: Web application framework
- **SQLite**: Lightweight database
- **LangGraph**: Agentic workflow management

## License

MIT
