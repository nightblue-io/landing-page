---
title: Introducing Freya
image: /uploads/blog-00001-introducing-freya.png
date: 2025-06-02
tags:
  - product
---

## Friction

The context switch is the worst part. You're deep in thought, untangling some legacy service or designing a new data schema, and then you get a ping: "Can we get a summary of the Q3 technical debt reduction efforts for the stakeholder sync?" An hour of your life is gone, your mental stack is cleared, and the flow state is a distant memory.

This sort of administrative friction seems to be a byproduct of most modern development frameworks. Agile, for all its benefits, created a lot of ceremony. Stand-ups, retros, sprint planning, backlog grooming. They all generate administrative exhaust. Someone has to capture it. Usually, that falls to the team.

Surely, we can improve this, can we?

## What it is

Freya is a project management automation agent, or assistant. You connect it to your tools; your calendar, your shared drive, GitHub, your chat app (Slack/Teams), your project management board (Jira/Asana/ClickUp/etc.). Then, it listens in the background and does the mundane, clerical work.

It’s not a project manager. It has no opinions. It doesn't make decisions. It just takes predictable, repetitive inputs and produces predictable outputs.

## How it works

There's no magic here. It hooks into the APIs you'd expect.

- It captures most of your project's "contextual data" (or activities) and put them in a centralized knowledgebase.
- It runs in the background, looking for hints and events, then reacts. It then uses its knowledgebase and feeds that to a language model.
- The prompt is very specific: "Summarize this stand-up. Identify action items and the person responsible. Draft a ticket for any new work mentioned. Note any blockers."
- It then uses your existing tool's API to show its work. It doesn't do its own thing. That seemed like a bad idea. You get a notification to review and approve its work.

## What it can do right now

It’s still in active development, but the core loops are:

- **Daily/weekly summaries of the team and members** - Freya tracks the teams activities, as long as they can be accessed by your tools' API. It then joins, records, and produces a summary to the intended targets.
- **Meeting summaries** - Point it at a calendar invite for your stand-up or planning meeting. It joins, records, and produces a summary with action items a few minutes after the meeting ends.
- **Onboarding new members** - This is a personal pain of mine. And time consuming. Freya will attempt to collate what it can find in its knowledgebase and proposes an onboarding program for your new member. Someone still needs to do the actual onboarding, but the preparations, such as schedules, duration and progress tracking, and pinging of relevant people; Freya will handle them (and probably get lost in the process most likely).
- **Slack/Teams thread summaries** - You can tag Freya in a long, rambling thread. It will read the whole thing and post a concise summary of the problem, the proposed solutions, and the conclusion.
- **Drafting stakeholder updates** You can ask it: "Draft an update on the 'New Checkout Flow' epic for a non-technical audience." It will scan the related tickets, PRs, and conversations to generate a plain-English summary of progress, which you can then edit and send.

## What it can't (and won't) do

Let's be clear about what Freya isn't.

- It's not a replacement for a human. It doesn't understand nuance, politics, or team morale. It's a glorified text processor. You still need a good product owner, a scrum master, and engineers who talk to each other.
- It makes mistakes. LLMs hallucinate. Transcriptions can be wrong. It might misunderstand who a ticket should be assigned to. That's why everything is a draft that requires human approval. You must check its work.
- It can't read minds. If the information isn't in your chat logs, on your board, or said in a meeting, it doesn't exist for Freya. Garbage in, garbage out.

## Ping us if this is right up your alley

It’s not finished. There are bugs. The UI is basic. The integration with Google Workspace is probably broken right now.

But it’s already saving me and my team a few hours a week. That's enough for me to think it might be useful to others. I'm looking for feedback from other teams who feel this same pain.

If you're interested, try it out [here](https://prism-chi-lovat.vercel.app/).

Let us know what you think. Especially if it breaks.
