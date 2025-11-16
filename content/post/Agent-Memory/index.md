---
title: "Agent Memory with LangGraph"
description: "Remember past interactions so it can make better decisions in the future."
slug: "agent-memory"
date: 2025-11-16T07:00:50-06:00
draft: false
categories:
  - "ai-agent"
tags:
  - "agent-memory"
  - "LangGraph"
image: "cover.png"
comments: true
---

Memory lets AI agents remember past interactions so they can learn, adapt to user preferences, and work more efficiently. As tasks and conversations get more complex, this becomes essential for a smoother and more satisfying user experience.

There are mainly two types of memory

![memory types](memory.png)

## Short-term memory

Short-term memory in LangGraph lets an application remember interactions within a single conversation thread by storing conversation history and other state (like files or retrieved documents) in thread-scoped checkpoints. While this gives the bot full context for each thread, long histories can exceed an LLM’s context window, slow responses, increase cost, and reduce accuracy. Because chat messages accumulate over time, applications often need strategies to trim or forget stale information to keep the context efficient and relevant.

A few techniques for managing short-term memory include:
- **Trim Messages**: Keep only the most recent messages (or tokens) so the history fits within the model’s context window.

- **Delete Messages**: Explicitly remove specific messages or wipe the entire history when it becomes irrelevant.

- **Summarize History**: Convert older messages into a compact summary; keep the summary + latest messages to preserve context while saving tokens.

- **Use Checkpoints**: Store, inspect, or delete conversation checkpoints to control state over time (not for token reduction, but for thread management).

- **Custom Filtering**: Apply your own logic (e.g., drop tool messages, remove low-value content) before trimming or summarizing.


## Long-term memory

Short-term memory in LangGraph lets stores user specific or application level data across sessions and is shared across conversational threads. Memories are scoped to any custom namespace, more than just single thread id. Long-term memory allows an application to retain information **across sessions** and **across conversation threads**.

A few key techniques and considerations for managing long-term memory include:

- **Memory type**: Decide what kind of information you want to store:  
  - **Semantic** – facts or knowledge from past interactions (e.g., user prefers short answers).  
  - **Episodic** – experiences or past actions (e.g., few-shot example prompting, agent previously handled this task).  
  - **Procedural** – instructions or rules, a combination of model weights, agent code, and agent’s prompt that collectively determine the agent’s functionality (e.g., how the agent should update prompts).  

- **Memory update timing**: Choose between immediate or deferred writes:  
  - **Real-Time Updates**: Memory is written synchronously during the interaction; ensures immediate availability but can slow responses.  
  - **Background Updates**: Memory is written asynchronously to avoid latency but may not be available immediately.

- **Memory storage structure**: Long-term memory is stored in a ***store*** using namespaces (e.g., user ID + app context) and keys (unique per memory item). Common patterns include:  
  - **Profile approach**: Maintain a single document per user that accumulates structured facts.  
  - **Collection approach**: Store many small, discrete memory items for modular retrieval (e.g., each fact as its own document).


## Examples

### Short-term Memory Example


### Long-term Memory Example