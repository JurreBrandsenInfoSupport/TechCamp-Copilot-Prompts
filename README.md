# Zero to Production: Rapid Prototyping with AI Tools

This repository contains the AI prompts and instructions used in the presentation **"Zero to Production: Rapid Prototyping with AI Tools"**. The goal is to demonstrate how to rapidly prototype a full-stack Todo application using modern AI tools and best practices.

## Contents

### 1. Backend Prompts

- **Step-by-step agent prompts for backend setup:**
  See [`backend-step-by-step-agent-prompts.md`](backend-step-by-step-agent-prompts.md) for detailed instructions on initializing a FastAPI backend, setting up PostgreSQL with Docker Compose, and structuring your project for rapid development.

### 2. Frontend Prompts

- **Prompt for generating a Next.js Todo app:**
  See [`chatGPT-prompt.md`](chatGPT-prompt.md) and [`vercel-prompt.md`](vercel-prompt.md) for clear, concise prompts to generate a modern, extensible Next.js frontend, with a focus on future backend integration.

### 3. Copilot Agent Mode

- **Agent instructions and integration prompts:**
  - [`copilot-agent-instruction.md`](copilot-agent-instruction.md): Domain vocabulary, naming conventions, and expected LLM behavior for Todo apps.
  - [`copilot-agent-prompt.md`](copilot-agent-prompt.md): Full-stack integration prompt for combining Next.js frontend and FastAPI backend.
  - [`copilot-agent-uv-instruction.md`](copilot-agent-uv-instruction.md): Project setup and dependency management using `uv`.

- **Learn more about Copilot Agent customization:**
  [Copilot Agent Customization Docs](https://code.visualstudio.com/docs/copilot/copilot-customization)

---

## How to Use

Each markdown file contains a prompt or instruction set that you can use directly with AI coding assistants (like GitHub Copilot, ChatGPT, or similar tools) to bootstrap and iterate on your project.

- **Backend:** Follow the backend prompts to set up your API and database.
- **Frontend:** Use the frontend prompts to scaffold a Next.js app ready for backend integration.
- **Agent Mode:** Use the Copilot Agent prompts to automate and standardize your workflow.

---

Feel free to explore each file for detailed, copy-paste-ready prompts!
