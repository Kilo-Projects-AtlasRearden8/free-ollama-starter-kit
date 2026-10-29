# STATUS — Free Local AI Starter Kit

## What was built

A freebies directory of free local AI programs that run offline, in the folder `/workspace/kilo-lab/free-ollama-starter-kit`:

- `README.md` — Markdown directory of all listings. Each listing shows cost, steps to get started, and the official link. No affiliate links. Credits Asdale Dynamics, LLC.
- `index.html` — Static HTML site with client-side search (no server, no API, no tracking). Same listings, filterable by category and searchable by name, description, category, and steps.
- `LICENSE` — MIT License. Copyright line exactly: `Copyright (c) 2026 Asdale Dynamics, LLC`.

Listings (10 total):

Ollama setup
- Ollama — https://ollama.com

Model picks
- Llama 3.2 (3B) — https://ollama.com/library/llama3.2
- Qwen 2.5 (7B) — https://ollama.com/library/qwen2.5
- Phi-4 (14B) — https://ollama.com/library/phi4
- Gemma 3 (4B) — https://ollama.com/library/gemma3

Frontends
- Open WebUI — https://openwebui.com
- AnythingLLM Desktop — https://anythingllm.com
- LM Studio — https://lmstudio.ai

Prompt collections
- Awesome ChatGPT Prompts — https://github.com/f/awesome-chatgpt-prompts
- Prompt Engineering Guide — https://www.promptingguide.ai

Credit: Dylan Asdale project, published by Asdale Dynamics, LLC (Indiana, formed October 2026). Hub: https://dylanasdale.github.io

## How to run it

No build step. Open `index.html` directly in any browser, or serve it locally:

```
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

The Markdown directory is readable in any text editor or Markdown viewer.

## Verification results

- HTML structure parses cleanly (no unmatched or unclosed tags).
- Inline JavaScript passes `node --check` syntax check.
- `index.html`, `README.md`, and `LICENSE` served with HTTP 200 via `python3 -m http.server`.
- `index.html` contains all 10 listings.
- `LICENSE` contains the exact copyright line `Copyright (c) 2026 Asdale Dynamics, LLC`.
- `README.md` credits Asdale Dynamics, LLC.
- No `.github/workflows` files, no affiliate links, no secrets, API keys, or personal data in any file.
- Git initialized and committed as `7a20f67` ("Initial commit: Free Local AI Starter Kit directory") under the existing git identity (Dylan Asdale). No push, no remote, no co-author trailers.

## Known gaps

- No automated test suite or linter configured (static site; verified manually above).
- Ollama, frontends, and model downloads are not bundled — users must download them from the official links.
- Open WebUI listing references the Docker run command in the README rather than inlining it fully on the card.
- Client-side search only; no server-side index or dark mode.
- Healthcare disclaimer included in README; nothing in these tools is medical advice.
