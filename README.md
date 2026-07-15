# Daily Cybersecurity Intelligence Digest

An automated workflow built in n8n that tracks the latest developments in cybersecurity, data privacy, and compliance, then delivers a curated, AI summarized briefing straight to your inbox every morning.

## Why I Built This

Staying current in cybersecurity means keeping up with a firehose of information: new vulnerabilities, regulatory changes, breach disclosures, and emerging technologies, often scattered across dozens of sources. Reading everything manually is not realistic for anyone with a full time role.

This project was built as part of my ongoing effort to upskill in AI powered automation. Rather than just reading about how large language models can be used in real workflows, I wanted to build something that solves an actual problem I face: staying informed without spending hours doing it.

The result is a fully automated pipeline that collects, filters, and summarizes cybersecurity related news using AI, then formats it into a clean digest and emails it out on a daily schedule with zero manual effort required after setup.

## What It Does

Every day at a scheduled time, the workflow:

1. Pulls fresh articles from a curated list of trusted RSS sources covering security, privacy, and compliance news.
2. Filters out anything older than 24 hours, so the digest only reflects what is genuinely new.
3. Removes duplicate stories and sorts everything chronologically.
4. Passes the remaining articles to an AI agent that categorizes them, writes concise summaries, and highlights the most critical alerts.
5. Formats the output into a clean, readable HTML email.
6. Sends the finished digest directly to a chosen inbox.

This runs across three parallel tracks:

- **Security**: threat intelligence, breaches, tools, cloud security, and emerging technologies.
- **Privacy**: regulatory developments, consent and data minimization, privacy enhancing technologies, and enforcement actions.
- **Compliance**: frameworks, audits, third party risk, and governance updates.

## Who This Is For

You do not need a technical background to benefit from the output. The digest is written to be understood by both technical and non technical readers. For technical readers, it is a fast way to scan what matters before diving into the details. For non technical readers, such as managers, founders, or anyone simply trying to stay aware, it is a plain language summary of a fast moving industry without the jargon overload.

## How It Is Built

The workflow is built entirely in n8n and uses:

- RSS feed nodes to pull raw articles from multiple trusted sources.
- Filtering and sorting logic to keep only recent, relevant content.
- A Google Gemini powered AI agent to categorize and summarize each article.
- Code nodes to structure the final output into a polished HTML email.
- Gmail integration to deliver the finished digest automatically.

## Setup Requirements

To run this workflow yourself, you will need:

- An n8n instance (cloud or self hosted).
- A Google Gemini API key for the AI summarization step.
- A Gmail account connected via OAuth2 for sending the digest.
- Your preferred recipient email address, updated in the send node.

RSS sources can be customized or expanded to match your own areas of interest.

## A Note on This Project

This is a living project. As I continue learning how to design and refine AI powered automations, this workflow will keep evolving, whether that means improving summarization quality, adding new categories, or expanding the source list. Feedback and suggestions are always welcome.
