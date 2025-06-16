# 📅 Calendar Assistant Workflow for n8n

[![Language](https://img.shields.io/badge/n8n-v1.1+-blue)](https://n8n.io/)
[![OpenAI Model](https://img.shields.io/badge/OpenAI-gpt--4o--mini-ff69b4)](https://platform.openai.com/)
[![Google Calendar](https://img.shields.io/badge/API-Google%20Calendar-brightgreen)](https://developers.google.com/calendar)

This n8n workflow integrates **OpenAI GPT-4o-mini** with **Google Calendar** to act as an intelligent scheduling assistant. It listens to chat messages, interprets user intent through a smart AI agent, and creates events in your selected Google Calendar automatically.

---

## 🧠 Features

* **Chat Trigger**: Reacts to incoming chat messages.
* **AI Agent (LangChain)**: Uses system prompts and language models to process scheduling requests.
* **OpenAI GPT-4o-mini**: Handles natural language understanding and intent extraction.
* **Google Calendar Integration**: Schedules events into a specific calendar using OAuth2 credentials.

---

## ⚙️ Workflow Overview

1. **Trigger** – Listens for a new message via the `chatTrigger`.
2. **AI Agent** – Processes the user's intent using a system message like:

   > *"You are a calendar assistant. Your job is to evaluate the user's availability and create new events."*
3. **OpenAI Chat Model** – Uses GPT-4o-mini to generate AI responses.
4. **Google Calendar Node** – Creates the event in your configured calendar.

---

## 🛠️ Requirements

* **n8n** v1.1 or higher
* A valid **OpenAI API Key**
* A connected **Google Calendar** account with OAuth2 credentials set up in n8n

---

## 📂 How to Use

1. **Import the Workflow**: Upload the `.json` file into your n8n instance.
2. **Set Credentials**:

   * OpenAI API
   * Google Calendar OAuth2
3. **Enable and Test**: Trigger the workflow by sending a chat message like:

   > "Schedule a meeting with John on Friday at 3 PM."

---

## 📌 Notes

* The workflow uses LangChain’s agent system to combine natural language reasoning with real tool usage.
* The calendar ID is hardcoded, so ensure you replace it with your own calendar ID as needed.

---

## 📄 License

This project is open for adaptation under the MIT License.
