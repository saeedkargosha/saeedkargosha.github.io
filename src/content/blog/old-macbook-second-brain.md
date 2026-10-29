---
title: 'My old MacBook became my second brain'
description: 'A 2017 MacBook was sitting in a drawer. Now it runs my second brain with OpenClaw, Claude Code, Notion, and Tailscale.'
pubDate: 'Oct 30 2026'
---

I have a MacBook Pro from 2017. Intel chip, 8 GB of RAM. For a long time it sat in a drawer. My newer laptop did everything, so the old one had no job.

Then one evening I looked at my life and saw a mess. Todos in one app. Career ideas in my head. Tax papers in different folders. German words I wanted to learn, written on random notes. I did not need a faster computer. I needed a place that **remembers things for me**.

And I already had a computer with nothing to do.

## The first step: an agent that lives on it

I installed [OpenClaw](https://github.com/openclaw/openclaw) on the old MacBook. OpenClaw is an AI agent that runs on your own machine. You chat with it, and it can use tools, read files, and do real work.

For the model, OpenClaw uses **Claude Code CLI**. That means the same kind of agent I use for coding can also help with normal life things. It was a small idea, but it changed how I think about these tools. An agent harness is not only for code.

## The second step: give it a home for my data

An agent without a place to write is just a chatbot. So I gave it **Notion** as the home for structured things:

- my todos,
- my career roadmap,
- my money tracking,
- trip plans and shopping lists.

Plain notes and learning links go into Markdown files. **Anki** holds the things I want to remember for a long time, like German vocabulary for my B1 exam.

The rule is simple: every kind of information has exactly one home. If the agent is not sure where something goes, it asks me. It does not guess.

## The third step: take it with me

A second brain on a desk is not very useful. I think of things when I am walking, on the train, or in the kitchen.

This is where **Tailscale** came in. It connects my devices in a private network, so my phone and my iPad can reach the old MacBook from anywhere. No router tricks, no open ports. I open a chat, I say "add this to my todos", and the MacBook at home does the work.

The old machine is not fast. It does not need to be. The heavy thinking happens in the model. The MacBook only needs to stay on, hold my files, and run the agent.

## What I like most

- **It gave an old machine a new life.** Nothing was bought.
- **My data stays with me.** The memory is plain text files. I can open them, edit them, and trust them.
- **Skills fix mistakes once.** When the agent does something wrong, I update its skill, and it does not repeat the mistake.
- **I stay in control.** For anything that sends, posts, or spends money, the agent asks me first.

## What is next

I want to add an Obsidian vault as my learning brain, split the agent into smaller specialists, and maybe build a "Hey OpenClaw" voice assistant. I will write about each part here.

If you also have an old laptop in a drawer, give it a job. It might become the most useful computer you own.
