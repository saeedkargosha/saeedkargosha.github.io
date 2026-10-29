---
title: 'I talk to my second brain on Telegram'
description: 'How voice notes on Telegram reach my old MacBook, get turned into text on the machine itself, and how the agent can talk back.'
pubDate: 'Oct 30 2026'
---

In the first post I told you about my old MacBook and the agent that lives on it. There was one problem. I only had a chat window, and typing is slow.

My best ideas do not come at a desk. They come when my hands are busy: cooking, walking, carrying bags. I wanted to say the thing out loud and be done.

So I gave my second brain **ears**.

## Step one: Telegram as the front door

I already used Telegram every day, so I did not want a new app. I made a small Telegram bot and connected it to OpenClaw. Only paired people can talk to it, so strangers get nothing.

Now my agent is a chat contact on my phone. I can text it, send a photo, or hold the microphone button and just talk.

## Step two: what happens to a voice note

This part is my favourite, because the MacBook does the work by itself.

1. I record a voice note in Telegram.
2. Telegram carries the audio file to my old MacBook.
3. OpenClaw hands the file to a small script I wrote.
4. The script runs **faster-whisper**, an open-source speech model, with the "small" model, on the CPU.
5. The text goes to the agent like a normal message, and the agent answers.

The speech-to-text step runs on the MacBook, not in a cloud service. There is no API key and no extra bill.

The old Intel chip is not fast. A short test clip took about 20 seconds, including loading the model. For a voice note that I send and forget, that is fine. I do not wait for it.

## It is not perfect

I tested it with "Hello Saeed, this is a test." The MacBook understood: "Hello Said, this is a test."

Names are hard. Mixed languages are also hard. Sometimes my voice note is unclear, and the agent tells me, "I may have missed a detail," instead of guessing. I like that. A small honest doubt is better than a confident mistake.

## Step three: the agent talks back

The agent can also answer with a voice. Another small script picks the voice by looking at the text:

- **Farsi** text uses Piper, an offline voice model.
- **German** text uses the macOS voice "Anna".
- **English** text uses the macOS voice "Samantha".

I keep this switched off by default, so I get text unless I ask for audio. It is useful for German practice. I can ask for a sentence, hear it, and say it back.

## What I learned

- **Voice is the real mobile interface.** Typing on a phone is the thing that stops me from capturing ideas.
- **Local does not mean fancy.** Two short scripts and two free open-source models replaced a paid service.
- **An old machine is enough**, if you accept that it is slow and design around it.
- **Let the agent say "I am not sure."** It makes the whole system more trustworthy.

## What is next

I want the agent to wake up when I say its name, with a small microphone box in the kitchen. That is a story for another post.
