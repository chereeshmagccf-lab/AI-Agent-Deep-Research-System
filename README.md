# AI Agent & Deep Research System

An AI-powered browser agent and deep research system built on top of **browser-use**. The project provides a user-friendly **Gradio WebUI** for interacting with an AI agent that can browse websites, perform research, and execute browser-based tasks.

The system supports multiple Large Language Models and provides features such as custom browser usage, persistent browser sessions, browser automation, and deep research.

## ✨ Features

* 🤖 AI-powered browser agent
* 🔎 Deep research capabilities
* 🌐 Automated web browsing
* 🖥️ Gradio-based WebUI
* 🧠 Support for multiple LLM providers
* 🔑 OpenAI, Anthropic, Google, Azure OpenAI, DeepSeek, Ollama and more
* 🌍 Custom browser support
* 🔄 Persistent browser sessions
* 📹 Browser interaction monitoring
* 🎭 Playwright browser automation
* 🐳 Docker support
* 🧪 Testing support

The WebUI is built with Gradio and supports most browser-use functionality.

## 🏗️ Architecture

```text
                  ┌──────────────────┐
                  │      User        │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │     Gradio       │
                  │      WebUI       │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │    AI Agent      │
                  └────────┬─────────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
       ┌──────────┐  ┌───────────┐  ┌──────────┐
       │   LLM    │  │  Browser  │  │ Research │
       │ Providers│  │ Automation│  │  Engine  │
       └──────────┘  └───────────┘  └──────────┘
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                  ┌──────────────────┐
                  │  Final Response  │
                  └──────────────────┘
```

## 🛠️ Technologies

* **Python**
* **Gradio**
* **browser-use**
* **Playwright**
* **Large Language Models (LLMs)**
* **Browser Automation**
* **Deep Research**
* **Docker**
* **Git & GitHub**

## 🤖 LLM Support

The project provides support for multiple LLM providers, including:

* OpenAI
* Anthropic
* Google
* Azure OpenAI
* DeepSeek
* Ollama

Additional model support can be added as required.

## 🌐 Browser Features

### Custom Browser

The application allows users to connect their own browser, which can help avoid repeatedly logging into websites.

It also supports high-definition screen recording.

### Persistent Browser Sessions

The browser can remain open between AI tasks.

This allows the agent to maintain browser history and state across multiple tasks.

## 📋 Prerequisites

Before installing the project, make sure you have:

* Python **3.11 or higher**
* Git
* Internet connection

Python 3.11+ and Git are listed as the project prerequisites.

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/chereeshmagccf-lab/AI-Agent-Deep-Research-System.git
cd AI-Agent-Deep-Research-System/web-ui
```

### 2. Create Virtual Environment

Using `uv`:

```bash
uv venv --python 3.11
```

Activate the environment.

**Windows CMD:**

```bash
.venv\Scripts\activate
```

**Windows PowerShell:**

```bash
.\.venv\Scripts\Activate.ps1
```

**macOS/Linux:**

```bash
source .venv/bin/activate
```

The project documentation recommends using `uv` for Python environment management.

### 3. Install Dependencies

```bash
uv pip install -r requirements.txt
```

Install Chromium for Playwright:

```bash
playwright install --with-deps chromium
```

Or install all supported browsers:

```bash
playwright install
```

### 4. Configure Environment Variables

Create the `.env` file from the example:

**Windows CMD:**

```bash
copy .env.example .env
```

**PowerShell / macOS / Linux:**

```bash
cp .env.example .env
```

Then open `.env` and add the required API keys and configuration values.

## 🔐 Environment Configuration

Example configuration:

```env
OPENAI_API_KEY=your_key_here
ANTHROPIC_API_KEY=your_key_here
GOOGLE_API_KEY=your_key_here

CHROME_PERSISTENT_SESSION=true

RESOLUTION=1920x1080x24
RESOLUTION_WIDTH=1920
RESOLUTION_HEIGHT=1080

VNC_PASSWORD=your_vnc_password
```

**Never commit your actual API keys to GitHub.**

## ▶️ Running the Application

Start the WebUI using:

```bash
python webui.py --ip 127.0.0.1 --port 7788
```

Then open:

```text
http://127.0.0.1:7788
```

The application supports configuration options such as IP address, port, theme, and dark mode.

## 🐳 Docker Installation

Make sure Docker and Docker Compose are installed.

Build and start the application:

```bash
docker compose up --build
```

To keep the browser session persistent:

```bash
CHROME_PERSISTENT_SESSION=true docker compose up --build
```

The project also supports AMD64 and ARM64 architectures.

## 🖥️ Access the Application

After starting Docker:

**WebUI**

```text
http://localhost:7788
```

**VNC Browser Viewer**

```text
http://localhost:6080/vnc.html
```

The VNC viewer allows you to watch browser interactions in real time.

## 🔄 Browser Session Modes

### Default Mode

```env
CHROME_PERSISTENT_SESSION=false
```

* Browser opens for the AI task
* Browser closes after the task
* Provides a clean state for each interaction

### Persistent Mode

```env
CHROME_PERSISTENT_SESSION=true
```

* Browser remains open
* Maintains browser history and state
* Makes it possible to observe previous interactions

## 🌟 Use Cases

This project can be used for:

* AI-assisted web research
* Automated browser tasks
* Information gathering
* Research workflows
* Browser-based AI automation
* Multi-step web interactions
* AI agent experimentation
* LLM-powered browser automation

## 🧪 Testing

The project includes tests for different parts of the system, including:

* Browser functionality
* Deep research
* LLM API integration
* Playwright automation

Run the tests with:

```bash
pytest
```

## 🔮 Future Improvements

Possible improvements include:

* Retrieval-Augmented Generation (RAG)
* More agent tools
* Better research verification
* Agent evaluation frameworks
* MCP-based integrations
* Persistent conversation memory
* Cloud deployment
* Improved error handling
* Authentication and user management

## 👩‍💻 Author

**Chereeshma Alahari**

B.Tech – Computer Science and Engineering

GitHub:
`https://github.com/chereeshmagccf-lab/AI-Agent-Deep-Research-System`

## 📄 License

This project is intended for educational, research, and development purposes.
