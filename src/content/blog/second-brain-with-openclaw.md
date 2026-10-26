---
title: 'How I set up my second brain with OpenClaw'
description: 'My personal AI setup: OpenClaw as the brain, Notion and Obsidian as memory, Google as the inbox, and skills for todos, money, travel, and Anki.'
pubDate: 'Oct 26 2026'
---

I work with software and AI every day, but my own life was still a mess of notes, tabs, and half-finished lists. So I decided to build a **second brain**: one place that remembers things for me and helps me act on them.

This post is the big picture. Later posts will go deep on each part.

## The idea

A second brain should do three things:

1. **Capture** things fast (a todo, an idea, a link, an expense).
2. **Store** them in the right place, with a clear structure.
3. **Help me act** on them (remind me, search, plan, compare).

I did not want to build everything from zero. I use tools that already work and let an AI agent connect them.

## The stack

| Part | Tool | What it does |
|---|---|---|
| The brain | [OpenClaw](https://github.com/openclaw/openclaw) | The agent. I talk to it, and it uses tools and skills. |
| Structured data | Notion | Todos, finances, trips, wishlist, tax records. |
| Learning notes | Obsidian | My "Mind Library": AI links, things to learn, notes. |
| Inbox and calendar | Google Workspace | Email, calendar, Drive. |
| Memorizing | Anki | Flashcards for vocabulary, including German. |

The rule I follow: **each kind of information has exactly one home.** Money goes to Notion Finance. Things to learn go to Obsidian. If I am not sure where something goes, the agent should not guess. It should ask me.

## Skills, not giant prompts

The most useful lesson so far: don't put everything into one big prompt. Write a **skill** for each repeated job.

A skill is a short instruction file that tells the agent how to do one task well. For example:

- A **todo skill** that adds, lists, and completes tasks in my Notion database.
- A **finance skill** that records income and spending and gives me a monthly summary.
- A **travel skill** that searches flights, compares options, and saves them in Notion.
- A **grocery** and a **wishlist** skill, so the agent knows which list is which.
- An **Anki skill** to create and organize flashcards.

When the agent gets something wrong, I fix the skill once, and the mistake is gone for next time. This works much better than correcting the same thing in chat again and again.

## Memory

OpenClaw keeps simple Markdown files for memory: daily notes, a file about me (my preferences), and a file for long-term facts. Because they are plain text, I can read them, edit them, and trust them. There is no hidden database that I cannot inspect.

## From one agent to many agents

Today I mostly have **one main agent** with many skills. The next step is to split it into specialist agents, for example:

- an **Anki agent** for study and flashcards,
- a **tax agent** that knows my tax profile and deadlines,
- a **finance agent** for budgeting.

Why split? Each agent gets a smaller job, less context, and clearer rules. It also makes privacy easier: the tax agent can see tax data, and the travel agent cannot.

## What I learned

- **Start with structure.** An agent is only as good as the place it writes to. Clean Notion databases made everything easier.
- **Let the agent ask.** One good question is better than a wrong guess in my finance data.
- **Keep humans in the loop** for anything that sends, posts, or spends money.
- **Plain text wins.** Markdown files are easy to inspect, version, and move.

## A note about privacy

This setup holds private data: taxes, money, travel. On this website I will share the *design* (how it is built, what the skills do), but never real numbers, documents, or personal details.

## What's next

- A hands-free "Hey OpenClaw" voice assistant on a Raspberry Pi.
- Splitting the main agent into specialist agents.
- A publishing flow so the agent can draft posts like this one from my notes, and I approve them before they go live.

If you build something similar, I would love to hear how you do it.
