---
title: "LangGraph Intro"
description: "Low-level orchestration framework and runtime for building, managing, and deploying long-running, stateful agents."
slug: "langGraph-intro"
date: 2025-11-10T20:53:16-06:00
draft: false
categories:
  - "ai-agent"
tags:
  - "LangGraph"
image: "cover.png"
comments: true
---

## Fundamentals of Agents

### Agents and LangGraph

Agents come in many different forms, each with varying levels of autonomy and control. Understanding these distinctions is crucial for building effective AI systems.

![Different kinds of Agents](agent.png)

**Chain** is a set of steps before and after an LLM call. It's very reliable, with the same control flow every time.

**Router Agents** represent a type with low-level control. As shown in the diagram above, a router agent has a limited set of predefined options (e.g., choosing between step 2 or step 3) that the LLM can select from. The decision-making is constrained to these specific pathways.

**Autonomous Agents**, in contrast, operate with greater flexibility. They can navigate through any sequence of steps from a given set of options, or even dynamically generate their own next actions based on available resources and context. This autonomy allows for more adaptive behavior but also requires more sophisticated orchestration.

**LangGraph** is designed to help you build agents that balance reliability with control. The pillars of LangGraph include persistence, streaming, human-in-the-loop, and controllability. 


### LangGraph Key Components

**State** is a shared data structure that represents the current snapshot of your application. It's an object that gets passed between nodes and edges of the graph. It can be any data type, but is typically defined using a shared state schema.

**Nodes** are functions that encode the logic of agents. They receive the current state as input, perform logic operations, and return an updated state.

**Edges** are functions that determine which node to execute next based on the current state. They can be conditional branches or fixed transitions.

**State** holds the shared data, **nodes** do the work by updating the state, and **edges** tell what to do next based on the state.