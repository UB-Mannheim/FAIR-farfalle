# FAIR-farfalle

An open-source AI-powered search engine in the field of research data management based on [farfalle](https://github.com/rashadphz/farfalle) (a Perplexity analogue).

- 🛠️ [Tech Stack](#tech-stack)
- 🛠️ [Features](#features)
- 🏃🏿‍♂️ [Getting Started](#getting-started)
- 🚀 [Deploy](#-deploy)

## 🛠️ Tech Stack

- Frontend: [Next.js](https://nextjs.org/)
- Backend: [FastAPI](https://fastapi.tiangolo.com/)
- Search API: [SearXNG](https://github.com/searxng/searxng), [Tavily](https://tavily.com/), [Serper](https://serper.dev/), [Bing](https://www.microsoft.com/en-us/bing/apis/bing-web-search-api)
- Logging: [Logfire](https://pydantic.dev/logfire)
- Rate Limiting: [Redis](https://redis.io/)
- Components: [shadcn/ui](https://ui.shadcn.com/)


## Features
- Search with multiple search providers (Tavily, Searxng, Serper, Bing)
- Answer questions with cloud models (OpenAI/gpt4-o, OpenAI/gpt3.5-turbo, Groq/Llama3)
- Answer questions with local models (llama3, mistral, gemma, phi3)
- Answer questions with any custom LLMs through [LiteLLM](https://litellm.vercel.app/docs/providers)
- Search with an agent that plans and executes the search for better results

## 🏃🏿‍♂️ Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Ollama](https://ollama.com/download) (If running local models)
  - Download any of the supported models: **llama3**, **mistral**, **gemma**, **phi3**
  - Start ollama server `ollama serve`

### Quick Start:
```
git clone https://github.com/UB-Mannheim/FAIR-farfalle.git
cd FAIR-farfalle && cp .env-template .env
```
Modify .env with your API keys (Optional, not required if using Ollama)

Start the app:
```
docker-compose up -d
```

Wait for the app to start then visit [http://localhost:3000](http://localhost:3000).

For custom setup instructions, see [custom-setup-instructions.md](/custom-setup-instructions.md)
