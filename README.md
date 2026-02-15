🤖 Jira AI Assistant

An AI-powered Jira Assistant that lets you manage Jira tickets using natural language — just like chatting with a bot.

Instead of manually navigating Jira, you can simply type:

"Create a Jira ticket for login failure"
"Delete SCRUM-6"
"Yes, confirm it"

And the system understands your intent, asks for confirmation, and performs real Jira operations.

🏗️ Project Architecture

This is a full-stack + ML + integration project built end-to-end.

jira-ai-assistant/
│
├── chat-bot-py/          → Python LLM + NLP (Intent detection + conversation flow)
├── jira-my-admin/        → Spring Boot backend (Secure Jira API integration)
├── jira-chat-ui-bot/     → Angular chat UI (GPT-style experience)
🔄 System Flow

User sends message from Angular UI

FastAPI service processes conversation

DistilBERT model detects intent (create / update / delete)

Confirmation logic handled

Spring Boot service calls Jira REST APIs

Real Jira ticket action is performed

🧠 Tech Stack
Frontend

Angular

Chat-style UI (GPT-like interaction)

AI / NLP Layer

FastAPI

DistilBERT (Intent Classification)

Custom confirmation handling logic

Backend

Spring Boot

REST APIs

Secure Jira API integration

Integration

Jira REST APIs

Real ticket creation / deletion / updates

📦 Module Details
1️⃣ chat-bot-py

Tech: Python, FastAPI, Transformers

Responsibilities:

Conversation flow management

Intent detection (create / update / delete)

Confirmation handling

NLP processing

Run locally:

cd chat-bot-py
pip install -r requirements.txt
uvicorn main:app --reload
2️⃣ jira-my-admin

Tech: Spring Boot

Responsibilities:

Secure integration with Jira APIs

Perform actual ticket operations

Validate and sanitize requests

Act as system-level backend service

Run locally:

cd jira-my-admin
mvn clean install
mvn spring-boot:run
3️⃣ jira-chat-ui-bot

Tech: Angular

Responsibilities:

Chat interface

Message rendering

Confirmation prompts

API communication with FastAPI service

Run locally:

cd jira-chat-ui-bot
npm install
ng serve
✅ Current Features

Create Jira ticket via natural language

Delete Jira ticket via chat

Confirmation-based execution (prevents accidental actions)

Real Jira integration

Working end-to-end system

⚠️ Current Status

❌ Not production ready

❌ Not fully conversational AI

✅ Core architecture complete

✅ Strong backend + ML foundation

✅ Real Jira API integration

🚀 Planned Improvements

Context-aware conversations

Multi-user session handling

Role-based behavior (Scrum Master vs PM)

Sprint-level actions (planning, closing, summaries)

Advanced entity extraction

Memory-based conversation state

Improved NLP fine-tuning

🎯 Vision

Evolve this into an AI Sprint Handler —
an intelligent assistant that helps Scrum Masters and Project Managers run sprints efficiently, not just manage tickets.

Goal:

Reduce time spent on ticket management

Increase time spent on planning & execution

🔐 Environment Configuration

Each service requires:

Jira base URL

Jira email

Jira API token

CORS configuration

Service URLs (Angular → FastAPI → Spring Boot)

Store secrets in:

application.properties (Spring Boot)

.env (Python service)

environment.ts (Angular)

⚠️ Never commit credentials to version control.

🧪 Example Commands
Create a Jira ticket for payment failure
Delete SCRUM-12
Update SCRUM-5 status to Done
Yes, confirm it
📚 Why This Project?

This project was built to:

Reconnect with backend & system design thinking

Work across frontend + backend + ML

Build a real-world integrated system

Learn by building, not just revisiting tutorials

💡 Contributing

Ideas, improvements, and suggestions are welcome.

Potential areas:

Better NLP model training

OAuth-based Jira auth

Production-ready deployment

CI/CD setup

Dockerization

📄 License

MIT License (or update based on your preference)
