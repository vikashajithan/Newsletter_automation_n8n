📰 AI News Newsletter Automation (n8n)

An AI-powered newsletter workflow built with n8n, OpenAI, Serper News API, Slack, and Gmail.

This workflow listens for Slack mentions, extracts the exact news topic using AI, fetches the latest 5 news articles, generates a structured newsletter, posts it in Slack, and sends it via email automatically.

Workflow File:


News_letter_AI

🚀 How It Works

User mentions the bot in Slack
Example: @bot AI news

OpenAI extracts the exact topic from the message.

If it’s a valid news request →
The workflow calls Serper News API to fetch the latest 5 articles.

OpenAI generates a professional newsletter with:

Title

Short introduction

5 bullet points (headline + short summary)

Friendly closing

The newsletter is:

Posted in Slack

Sent to Gmail

🧠 Workflow Nodes

Slack Trigger – Listens for app_mention

LLM Intent Classifier – Extracts topic in strict JSON format

IF Node – Validates request

HTTP Request (Serper API) – Fetches latest news

LLM Newsletter Generator – Creates structured newsletter

Slack Node – Posts newsletter

Gmail Node – Sends newsletter email

🔧 Required Credentials

You must configure:

Slack Bot Token

OpenAI API Key (Model: gpt-4o-mini)

Serper API Key

Gmail OAuth2

🛠 Setup Steps

Import the workflow JSON into n8n.

Add all required credentials.

Activate the workflow.

Mention the bot in Slack:

@bot AI news
📌 Example Requests

@bot AI news

@bot US tariff news

@bot crypto updates

@bot sports news

🧱 Tech Stack

n8n

OpenAI (gpt-4o-mini)

Serper News API

Slack API

Gmail API

📬 Output

Structured AI-generated newsletter

Sent to Slack channel

Delivered to email inbox

Built by Vikash 🚀
