# MCP Weather Service

A weather information service built using Model Context Protocol (MCP) that provides real-time weather alerts for US states.

## Features

- Get current weather alerts for any US state
- Interactive chat interface using Groq LLM
- Simple echo resource endpoint for testing

## Requirements

- Python 3.11 or higher
- Dependencies listed in `requirements.txt`
- Groq API key

## Installation

1. Clone this repository
   https://github.com/EquineNaveen/MCP-Server-and-Tools.git

2. Install dependencies:

```bash
pip install -r requirements.txt
```

Or use `uv`:

```bash
uv pip install -r requirements.txt
```

3. Create a `.env` file in the project root with your Groq API key:

```
GROQ_API_KEY="your_groq_api_key_here"
```

## Usage

### Starting the MCP Weather Server

The MCP server can be started using the configuration in `server/weather.json`:

```bash
uv run --with mcp[cli] mcp run server/weather.py
```

### Using the Chat Client

The chat client allows interaction with the weather service through a conversational interface:

```bash
python server/client.py
```

Use the following commands in the chat:
- Type `exit` or `quit` to end the conversation
- Type `clear` to clear conversation history

### Available Tools

- `get_alerts`: Get weather alerts for a US state using a two-letter state code (e.g., CA, NY)

## Project Structure

```
mcpweather/
│   main.py              # Entry point for future CLI functionality
│   pyproject.toml       # Project metadata and dependencies
│   requirements.txt     # Pip-compatible dependencies list
│   README.md            # This documentation
│   .env                 # Environment variables (API keys)
│
└───server/
    │   client.py        # Interactive chat client
    │   weather.json     # MCP server configuration
    │   weather.py       # MCP server implementation with weather tools
```
