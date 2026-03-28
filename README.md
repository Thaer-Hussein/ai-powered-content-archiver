# n8n Telegram to Notion Automation

This project automates the process of capturing useful content sent through Telegram, processing it with an LLM, and storing it in a structured Notion database.

## The Problem
In group chats, many useful messages, links, and notes get shared daily. Over time, they become difficult to retrieve, especially when the number of messages grows.

Saving raw text or links alone is not enough, because searching through a large volume of unstructured content becomes inefficient.

## The Solution
I built an automation workflow using:

- **Telegram Bot** as the message input channel
- **n8n** for workflow automation
- **Google Gemini** for processing the message and returning structured JSON
- **Notion** as the final structured knowledge base

## How It Works
1. A message is sent to the Telegram bot
2. The workflow is triggered in n8n
3. Gemini processes the content and returns structured JSON
4. The extracted fields are mapped into a Notion database page

## Output Structure
The message is processed into fields such as:
- Title
- Category
- Summary
- Original Text
- Link
- Platform
- Tags
- Created At

## Why Not WhatsApp?
I originally wanted to integrate with WhatsApp, but due to policy restrictions, complexity, and cost, I used Telegram instead as a practical and free alternative.

## Screenshots

### Telegram Bot Input
![Telegram Bot](screenshots/telegram-bot-example.png)

### n8n Workflow
![n8n Workflow](screenshots/n8n-workflow-overview.png)

### Notion Database Output
![Notion Database](screenshots/notion-database-output.png)

## Tech Stack
- n8n
- Telegram Bot API
- Google Gemini
- Notion API

## Notes
This repository is shared for learning and demonstration purposes.  
Sensitive credentials and private configuration values were removed before publishing.

## Credits
This project idea was developed after learning automation and n8n in a course delivered by Engineer Mohammad Houriya under IEEE supervision.
