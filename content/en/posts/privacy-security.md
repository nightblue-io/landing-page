---
title: Privacy and security from day 1
image: /uploads/blog-00002-privacy-security-covered.png
date: 2025-06-12
tags:
  - product
---

##

For an AI automation engine to be useful, it needs context. Lots of it. But creating a centralized knowledge-base from your enterprise data raises an immediate, critical question: who gets to see what?

When we started building [Freya](https://nightblue.io/), our AI assistant for automating project management, we knew that simply slurping up data from GitHub, Slack, Jira, G-Workspace, etc. into a centralized bucket of contextual information was a non-starter. Trust is paramount, and that begins with respecting the security and access controls you already have in place.

That's why we built Freya to honor the source permission model from day one.

When Freya connects to your Google Workspace, for example, it doesn’t just ingest documents; it understands and inherits the existing permissions. If an engineer doesn't have access to a confidential strategy doc, that information will never be included in a summary Freya generates for them. A report for leadership won't leak details from a private 1:1.

This isn't an afterthought or a feature on a future roadmap. It's a core architectural principle. You shouldn't have to rebuild your entire permission system just to reduce administrative friction. The tool should adapt to your workflow, not the other way around.
