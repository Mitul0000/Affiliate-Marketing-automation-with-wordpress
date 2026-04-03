# Affiliate Marketing Automation with WordPress

An AI-powered n8n automation workflow that reads blog topics from a Google
Sheet, generates fully written, SEO-optimised blog posts using GPT-4o-mini,
and automatically publishes them to WordPress — complete with images —
then notifies you on Telegram.

## Features

### Google Sheets Integration
- Reads blog topics, keywords, or product details directly from a Google Sheet
- Fully automated — no manual input needed once set up

### AI Content Generation
- Copywriter AI Agent powered by **GPT-4o-mini** writes complete blog posts
- Humanizer node refines the content to sound natural and engaging
- Generates **HTML content**, **title**, **slug**, and **meta description** automatically
- Structured Output Parser ensures clean, consistent formatting

### Image Handling
- Fetches a relevant image via HTTP request
- Uploads the image directly to WordPress
- Sets it as the featured image on the post

### WordPress Publishing
- Combines all blog details and publishes the post directly to WordPress
- Cleans and formats HTML before publishing for a polished output

### Telegram Notification
- Sends a success message to Telegram once the post is live

## How It Works

1. **Schedule Trigger** fires the workflow automatically at set intervals
2. Reads the next blog topic from **Google Sheets**
3. **Copywriter AI Agent** (GPT-4o-mini) writes the full blog post
4. **Humanizer** refines the content tone
5. Two parallel paths generate:
   - Full **HTML blog content**
   - **Title, slug, and meta description**
6. All details are **merged and combined**
7. HTML is cleaned up and formatted
8. Post is created on **WordPress** with an uploaded featured image
9. A **Telegram message** confirms successful publishing

## Tech Stack

- **n8n** — Workflow automation
- **OpenAI GPT-4o-mini** — AI content generation
- **Google Sheets** — Blog topic source
- **WordPress REST API** — Auto-publishing
- **Telegram Bot API** — Success notifications
- **HTTP Request** — Image fetching

## Setup

1. Import `workflow.json` into your n8n instance
2. Set up credentials for:
   - Google Sheets OAuth2
   - OpenAI API key
   - WordPress (username + application password)
   - Telegram Bot (create via @BotFather)
3. Add your blog topics/keywords to the Google Sheet
4. Set your preferred schedule in the Schedule Trigger node
5. Activate the workflow and let it run!

## Usage

Simply add a new row to your Google Sheet with a blog topic or keyword —
the workflow handles everything else automatically:
- Writing the post
- Generating SEO metadata
- Adding an image
- Publishing to WordPress
- Notifying you on Telegram

## About

Built with n8n's visual workflow automation, this project demonstrates how
AI can fully automate affiliate blog content creation and publishing —
from a simple spreadsheet row to a live WordPress post, hands-free.
