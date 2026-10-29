# Free Local AI Starter Kit

A free, local-first directory of AI tools you can run entirely offline on your own computer. No subscriptions, no API keys, no affiliate links, and nothing in this directory tracks you.

Built by **Asdale Dynamics, LLC** (Indiana, formed October 2026) for Dylan Asdale's beginner-friendly AI education work — books, guides, and practical tools explained plainly, step by step, like a friend would.

## Who this is for

Anyone who wants to try AI without handing over their data or a credit card. If you've heard about local AI but weren't sure where to start, start here.

## What "local AI" means

You download the software and the models once, then run them on your own machine. No account required, no monthly bill, and your prompts never leave your computer. Good for private writing, book work, and sensitive notes.

Downloading models uses the internet once; after that, everything runs offline.

## How to use this directory

Each listing below shows three things:

- **Cost** — what you pay (every listing here is $0)
- **Steps** — what to do, in order
- **Official link** — where to download it straight from the source

No affiliate links, ever. Pick one listing, follow the steps, and you're running local AI.

## View this directory as a website

This folder includes a static website with client-side search: `index.html`. Open it directly in any browser, or serve it locally:

```
python3 -m http.server 8000
```

Then open http://localhost:8000/index.html. Search and filter work entirely in your browser — nothing is sent to a server.

## 1. Ollama setup (start here)

### Ollama

Ollama is the engine that runs large language models locally on Mac, Windows, and Linux. It downloads models, serves them, and stops them when you're done.

- **Cost:** $0 (free, open source)
- **Steps:**
  1. Download the installer for your operating system at https://ollama.com
  2. Run the installer and follow the prompts
  3. Open a terminal (Mac/Linux) or PowerShell/Command Prompt (Windows)
  4. Verify the install: `ollama --version`
  5. Run your first model: `ollama run llama3.2`
  6. Type `/bye` or press Ctrl+D to exit the chat
- **Official link:** https://ollama.com

Once Ollama is running, it listens at `http://localhost:11434`, and any frontend in section 3 can connect to it.

## 2. Model picks (free models to run with Ollama)

Models download once through Ollama and then work offline forever. Start small — a 3B model runs well on most laptops.

### Llama 3.2 (3B) — best starter model

Fast, capable, and light enough for most laptops. Great for writing, summarizing, and general questions.

- **Cost:** $0
- **Steps:**
  1. With Ollama installed, open a terminal
  2. Download the model: `ollama pull llama3.2`
  3. Run it: `ollama run llama3.2`
- **Official link:** https://ollama.com/library/llama3.2

### Qwen 2.5 (7B) — strong general-purpose model

A step up in capability from Llama 3.2. Good for drafting, reasoning, and longer writing tasks.

- **Cost:** $0
- **Steps:**
  1. Open a terminal
  2. Download the model: `ollama pull qwen2.5:7b`
  3. Run it: `ollama run qwen2.5:7b`
- **Official link:** https://ollama.com/library/qwen2.5

### Phi-4 (14B) — reasoning model

Microsoft's small-but-sharp model. Strong on logic, math, and structured tasks while still running on many laptops.

- **Cost:** $0
- **Steps:**
  1. Open a terminal
  2. Download the model: `ollama pull phi4`
  3. Run it: `ollama run phi4`
- **Official link:** https://ollama.com/library/phi4

### Gemma 3 (4B) — Google's lightweight model

A compact, capable model from Google that works well for everyday chats and writing help.

- **Cost:** $0
- **Steps:**
  1. Open a terminal
  2. Download the model: `ollama pull gemma3:4b`
  3. Run it: `ollama run gemma3:4b`
- **Official link:** https://ollama.com/library/gemma3

**Tip:** See every free model available for Ollama at https://ollama.com/library. Models with "B" in the name (3B, 7B, 14B) refer to size in billions of parameters — smaller ones run faster on weaker computers.

## 3. Frontends (friendly faces for Ollama)

Ollama runs in the terminal by default. These frontends give you a chat window, document upload, and saved conversations — still fully local.

### Open WebUI

A full-featured web interface for Ollama with saved chats, document uploads, and multiple model support. Self-hosted with Docker.

- **Cost:** $0 (free, open source, self-hosted)
- **Steps:**
  1. Install Docker Desktop from https://www.docker.com
  2. Run Ollama in one terminal window
  3. Start Open WebUI:

     ```
     docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway \
       -v open-webui:/app/backend/data --name open-webui --restart always \
       ghcr.io/open-webui/open-webui:main
     ```

  4. Open http://localhost:3000 and create an admin account
  5. In Settings → Admin, confirm Ollama is connected at http://host.docker.internal:11434
- **Official link:** https://openwebui.com

### AnythingLLM Desktop

A desktop app that lets you chat with local models and your own documents (PDFs, text files) offline.

- **Cost:** $0 (free for personal and community use)
- **Steps:**
  1. Download AnythingLLM Desktop at https://anythingllm.com
  2. Install and launch the app
  3. Choose Ollama as your LLM provider and point it at http://localhost:11434
  4. Import a folder of documents to chat with your own files offline
- **Official link:** https://anythingllm.com

### LM Studio

A desktop app for discovering, downloading, and running models with a visual chat interface and a local API server.

- **Cost:** $0 (free for personal use)
- **Steps:**
  1. Download LM Studio at https://lmstudio.ai
  2. Install and launch the app
  3. Use the built-in model catalog to download a model (try Llama 3.2 3B)
  4. Start the local server in the app, then chat inside LM Studio — or point other Ollama-compatible tools at http://localhost:1234
- **Official link:** https://lmstudio.ai

## 4. Prompt collections (free, work offline once downloaded)

Download these once, then copy prompts into your local LLM chat anytime — no internet needed.

### Awesome ChatGPT Prompts

A community collection of ready-to-use prompts for writing, coding, learning, and productivity.

- **Cost:** $0
- **Steps:**
  1. Visit https://github.com/f/awesome-chatgpt-prompts
  2. Click Code → Download ZIP, or run `git clone https://github.com/f/awesome-chatgpt-prompts.git`
  3. Open the prompt file in any text editor
  4. Copy a prompt and paste it into your local model chat
- **Official link:** https://github.com/f/awesome-chatgpt-prompts

### Prompt Engineering Guide

A free guide to writing better prompts, with examples you can practice with offline.

- **Cost:** $0
- **Steps:**
  1. Visit https://www.promptingguide.ai
  2. Read the basics section and save the page for offline reading
  3. Try the example prompts in your local model chat, then tweak them
- **Official link:** https://www.promptingguide.ai

## Staying safe

- These are educational tools, not medical advice. If you're a healthcare worker exploring AI, use it for learning and admin only — never for patient diagnoses or treatment decisions.
- No listing here contains affiliate links, tracking, or paid upsells. Everything listed has a genuine free tier or is fully open source. Individual apps may have their own privacy practices; check each official site for details.
- Downloading models uses internet once; after that, everything runs offline.

## About Asdale Dynamics, LLC

Asdale Dynamics, LLC (Indiana, formed October 2026) is Dylan Asdale's LLC for beginner-friendly AI education, books, and guides. Dylan is a registered nurse turned AI author. His book *The Massive AI Manual* and hub site https://dylanasdale.github.io explain AI plainly, step by step, like a friend would. This directory is published by Asdale Dynamics, LLC.

## License

This directory is MIT licensed. Copyright (c) 2026 Asdale Dynamics, LLC. See [LICENSE](LICENSE).
