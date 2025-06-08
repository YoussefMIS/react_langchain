# ReAct Langchain Agent Example

This project demonstrates how to build a simple ReAct-style agent using [LangChain](https://python.langchain.com/) and [Ollama](https://ollama.com/) for local LLM inference. The agent can use tools, follow a reasoning/action loop, and is easily extensible.

## Features
- **ReAct Agent Loop**: Implements the ReAct pattern for tool-augmented reasoning.
- **Custom Tools**: Example tool to get the length of a text string.
- **Ollama LLM Integration**: Uses a local LLM via Ollama for fast, private inference.
- **Callback Logging**: Custom callback handler to print prompts and responses for debugging.

## Requirements
- Python 3.9+
- [Ollama](https://ollama.com/) (for local LLMs)
- [LangChain](https://python.langchain.com/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)

## Installation
1. Clone this repository.
2. Install dependencies:
   ```sh
   pip install langchain langchain_ollama python-dotenv
   ```
3. (Optional) Install and run Ollama, and pull a model (e.g., `ollama pull qwen3:0.6b`).
4. Set up your `.env` file with the required API keys (see example in `.env`).

## Usage
Run the main script:
```sh
python main.py
```
You should see the agent reasoning through the question and using the tool.

## Project Structure
- `main.py` — Main agent loop and tool definitions.
- `callbacks.py` — Custom callback handler for logging.
- `.env` — Environment variables for API keys and settings.
- `ReadMe.md` — This documentation file.

## Example Output
```
Hello, World!
***Prompt to LLM was:***
... (prompt text)
*********
AgentAction(...)
get_text_length called with text: DOG
observation=3
...
Final Answer: 3
```

## Customization
- Add more tools by defining new functions and adding them to the `tools` list in `main.py`.
- Change the LLM model by editing the `ChatOllama` instantiation.

## License
This project is for educational purposes. See individual package licenses for dependencies.
