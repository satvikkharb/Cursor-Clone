# 🤖 AI Assistant with Tool Use (Function Calling)

An intelligent assistant built with OpenAI’s function calling, designed to reason step-by-step and interact with tools like weather APIs and system commands. The assistant follows a structured **Start → Plan → Action → Observe → Output** loop to solve user queries.

---

## 🚀 Features

- 🔁 **Multi-step reasoning** for solving complex queries
- 🧰 **Tool integration** (weather fetch, command runner)
- 🧠 **OpenAI GPT-4o** for structured planning and execution
- 🔧 **JSON output format** for clear, consistent responses
- 🛠️ **Easily extensible** — just add more tools!

---

## 🧰 Available Tools

| Tool Name     | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `get_weather` | Takes a city name and returns current weather using `wttr.in`       |
| `run_command` | Executes shell commands and returns the system output               |

---

## 📦 Requirements

Install dependencies:


pip install openai requests python-dotenv


## 📝 How It Works
User enters a query (e.g. "What's the weather in Paris?")

Assistant plans the steps to solve the query

It selects the appropriate tool

It performs the action using the tool

It observes the result

Returns the final output

## 💬 Example Interaction
bash
Copy
Edit

> What is the weather in New York?

🧠: The user is interested in weather data of New York.
🧠: From the available tools, I should call get_weather.
🔨 Tool Called: get_weather New York
🤖: The weather in New York is Partly cloudy +17°C.


## 🗂️ Project Structure
bash
Copy
Edit
.
├── .env                # Environment variables (your API key)
├── assistant.py        # Main script with assistant logic and tool functions


## ➕ Adding New Tools
Write the function.

Add it to the avaiable_tools dictionary.

Include a description in the system_prompt.

## 🛠 Tech Stack
Python 3

OpenAI GPT-4o

Requests

dotenv
