# AI Agent & Deep Research System

An AI-powered agent system designed to understand user tasks, interact with web resources, perform research, and generate useful responses. The project combines an AI agent, browser interaction, research utilities, custom prompts, and a web-based user interface.

## 🚀 Features

* 🤖 **AI Agent** – Processes user instructions and performs multi-step tasks.
* 🔎 **Deep Research** – Performs structured research and collects relevant information from the web.
* 🌐 **Browser Automation** – Enables the agent to interact with web pages.
* 🧠 **Custom Prompting** – Uses customized system prompts and agent instructions to improve task execution.
* 💬 **Message Management** – Handles communication between the user interface and the agent.
* 🛠️ **Custom Controller** – Provides tools and actions that can be used by the agent.
* 📊 **Agent State Management** – Maintains information required during agent execution.
* 🖥️ **Web Interface** – Provides an interface for interacting with the AI agent.
* 🧪 **Testing** – Includes tests for browser interaction, research functionality, LLM integration, and Playwright-based workflows.
* 🐳 **Docker Support** – Includes Docker configuration for running the application in a containerized environment.

## 🏗️ Project Structure

```text
ai-agent/
└── web-ui/
    ├── src/
    │   ├── agent/
    │   │   ├── custom_agent.py
    │   │   ├── custom_message_manager.py
    │   │   ├── custom_prompts.py
    │   │   ├── custom_system_prompt.md
    │   │   └── custom_views.py
    │   │
    │   ├── browser/
    │   │   ├── custom_browser.py
    │   │   └── custom_context.py
    │   │
    │   ├── controller/
    │   │   └── custom_controller.py
    │   │
    │   └── utils/
    │       ├── agent_state.py
    │       ├── deep_research.py
    │       ├── llm.py
    │       └── utils.py
    │
    ├── tests/
    │   ├── test_browser_use.py
    │   ├── test_deep_research.py
    │   ├── test_llm_api.py
    │   └── test_playwright.py
    │
    ├── assets/
    ├── webui.py
    ├── requirements.txt
    ├── docker-compose.yml
    ├── .env.example
    └── README.md
```

## 🔄 How It Works

The system follows an agent-based workflow:

```text
User
  │
  ▼
Web Interface
  │
  ▼
AI Agent
  │
  ├── Understands the task
  │
  ├── Creates an execution plan
  │
  ├── Uses available tools
  │
  ├── Interacts with web resources
  │
  └── Performs research
  │
  ▼
Research / Tool Results
  │
  ▼
AI Processing
  │
  ▼
Final Response
```

## 🧩 Main Components

### AI Agent

`src/agent/custom_agent.py`

The main agent component responsible for processing tasks and coordinating the different parts of the system.

### Deep Research

`src/utils/deep_research.py`

Provides functionality for carrying out research-oriented tasks and processing information gathered during the workflow.

### LLM Utilities

`src/utils/llm.py`

Contains utilities used for interacting with the language-model layer of the application.

### Browser

`src/browser/`

Contains custom browser and browser-context functionality used when the agent needs to interact with web pages.

### Controller

`src/controller/custom_controller.py`

Provides custom actions and controller functionality that can be used by the agent during task execution.

### Agent State

`src/utils/agent_state.py`

Maintains state information required during agent workflows.

### Web UI

`webui.py`

Provides the user-facing interface for interacting with the AI agent.

## 🛠️ Technologies

* Python
* Large Language Models (LLMs)
* AI Agents
* Web Research
* Browser Automation
* Playwright
* Python Web UI
* Docker
* Git & GitHub

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd ai-agent/web-ui
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

On Linux/macOS:

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file using the provided example:

```bash
cp .env.example .env
```

For Windows, you can also create the `.env` file manually from `.env.example`.

Add the required API credentials and configuration values to the `.env` file.

### 5. Run the Application

```bash
python webui.py
```

Then open the local web interface shown by the application.

## 🐳 Docker

The project also contains Docker configuration.

To run using Docker Compose:

```bash
docker compose up --build
```

After the containers start, access the application through the configured local port.

## 🧪 Testing

The project includes tests covering different parts of the system.

Run the test suite using:

```bash
pytest
```

Individual tests can also be executed, for example:

```bash
pytest tests/test_deep_research.py
```

```bash
pytest tests/test_llm_api.py
```

```bash
pytest tests/test_playwright.py
```

## 🔐 Environment Variables

The project uses environment variables for configuration and API credentials.

Do not commit your actual `.env` file or API keys to GitHub.

Use:

```text
.env.example
```

as the template for required configuration.

## 📌 Use Cases

This project can be used for:

* Automated web research
* AI-assisted information gathering
* Multi-step task execution
* Browser-based automation
* Research assistance
* AI-powered workflow automation
* Experimenting with agent-based AI systems

## 🔮 Future Improvements

Possible future improvements include:

* Retrieval-Augmented Generation (RAG)
* Persistent conversation memory
* Better agent evaluation and monitoring
* Additional tools and integrations
* Improved research result verification
* More robust error handling
* Authentication and user management
* Deployment to a cloud platform
* MCP-based tool integration

## 👩‍💻 Author

**Chereeshma Alahari**

B.Tech – Computer Science and Engineering

## 📄 License

This project is intended for educational and development purposes.
