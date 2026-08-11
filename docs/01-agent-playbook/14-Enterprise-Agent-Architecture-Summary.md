# Enterprise Agent Architecture Summary

## Purpose

This document consolidates the foundational concepts required to design, build, deploy, and operate enterprise AI agents.

The objective is not to use agents everywhere.

The objective is to select the simplest architecture capable of solving the business problem reliably and creating measurable value.

---

# 1. Start With the Business Problem

Do not begin with:

"What agent should we build?"

Begin with:

"What business problem are we trying to solve?"

Before coding, complete the PLS Agent Design Canvas.

Answer:

1. What does it do?
2. Why does it matter?
3. What does good look like?
4. What tools does it need?
5. Where does the output go?
6. What's the business impact?
7. What are the risks and guardrails?

---

# 2. Choose the Correct Architecture

Not every problem requires an agent.

## Automation

Use when the path is predetermined.

IF X → DO Y

Automation is primarily deterministic.

## Workflow

Defines how work moves from beginning to end.

A workflow may contain:

- Humans
- Automations
- AI Assistants
- Agents
- Business systems

## AI Assistant

Helps a human perform work.

The human remains responsible for deciding and acting.

## AI Agent

Owns an objective and can determine appropriate actions at runtime within defined boundaries.

---

# 3. The Enterprise Agent Stack

BUSINESS PROBLEM

↓

AGENT SPECIFICATION

↓

MODEL / INTELLIGENCE

↓

INSTRUCTIONS

↓

KNOWLEDGE + MEMORY

↓

TOOLS

↓

DECISION / ORCHESTRATION

↓

ACTION

↓

EVALUATION

↓

HUMAN OVERSIGHT

↓

BUSINESS OUTCOME

The LLM is one component of the system.

The LLM alone is not the agent.

---

# 4. Technical Building Blocks

LLM
= Intelligence / reasoning engine

Prompt / Instructions
= How the model should behave

API
= Software-to-software communication

MCP
= Standardized way to expose tools and context to AI applications

RAG
= Retrieve relevant knowledge

Memory
= Retain useful information

Tool Calling
= Request an external capability

Orchestration
= Coordinate what happens next

Agent Harness
= Operating environment around the agent

Evaluation
= Determine whether the system worked

---

# 5. Agent Execution Loop

GOAL

↓

OBSERVE

↓

REASON

↓

DECIDE

↓

ACT

↓

OBSERVE RESULT

↓

EVALUATE

↓

CONTINUE / ESCALATE / COMPLETE

Agentic behavior comes from controlled runtime decision-making toward an objective.

---

# 6. Agent Skills

AGENT
= Who owns the work?

SKILL
= How does it know how to perform the work?

TOOL
= What can it use to perform the work?

Skills package reusable operational know-how.

Whenever practical, skills should remain portable across models and frameworks.

---

# 7. Agent Harness

The harness provides the environment surrounding the agent.

It may manage:

- Models
- Instructions
- Context
- Skills
- Tools
- Knowledge
- Memory
- State
- Execution
- Guardrails
- Errors
- Logging
- Evaluation

The model provides intelligence.

The harness helps turn that intelligence into an operational system.

---

# 8. Orchestration and Agent Managers

Orchestration answers:

"What happens next, and who or what should do it?"

A Manager or Supervisor Agent may:

- Delegate
- Coordinate
- Review
- Reassign
- Escalate
- Determine completion

Do not create multiple agents unnecessarily.

Prefer:

Automation

↓

Single Agent + Skills

↓

Multiple Specialized Agents

↓

Manager + Specialized Agents

Add complexity only when the business problem requires it.

---

# 9. Context, State, Memory, and Knowledge

CONTEXT

What information is available to the agent right now?

STATE

Where is the process right now?

MEMORY

What should the system remember for later?

KNOWLEDGE

What information can the agent retrieve?

These concepts are related but not interchangeable.

---

# 10. Agent Control

GUARDRAILS

What boundaries must it follow?

PERMISSIONS

What can it access and do?

HUMAN-IN-THE-LOOP

Where must a person participate?

ESCALATION

When should control return to a human?

AUTONOMY

How much can the agent independently decide and execute?

Key principle:

Capability does not equal authority.

---

# 11. Evaluation and Observability

EVALUATION

Did it work correctly?

OBSERVABILITY

What happened?

RELIABILITY

Can we depend on it?

LOGGING

What events happened?

TRACING

What path did the execution take?

MONITORING

How does the system perform over time?

A demonstration proves the system can work.

Production requires evidence that it works reliably, safely, repeatedly, and economically.

---

# 12. Production Lifecycle

SPECIFY

↓

BUILD

↓

TEST

↓

DEPLOY

↓

RUN

↓

OBSERVE

↓

EVALUATE

↓

IMPROVE

↓

VERSION

↓

REDEPLOY

↓

REPEAT

Deployment is not the end of the lifecycle.

---

# 13. Build vs Managed Platform

Agent infrastructure can be built directly or provided partly by a managed platform.

## Build

Provides greater architectural control and customization but requires more engineering and maintenance.

## Managed Platform

Provides portions of the harness and infrastructure, potentially accelerating deployment while introducing platform dependency and other tradeoffs.

Architecture should be selected based on business requirements rather than platform popularity.

---

# 14. The PLS Architecture Principle

Always move:

BUSINESS PROBLEM

↓

WORKFLOW

↓

BOTTLENECK

↓

RIGHT INTERVENTION

↓

DESIGN

↓

BUILD

↓

TEST

↓

MEASURE

↓

DEPLOY

↓

IMPROVE

The intervention may be:

- Process improvement
- Deterministic automation
- AI Assistant
- Agent
- Agentic workflow
- Human process change
- Combination of approaches

AI is not the objective.

Business improvement is the objective.

---

# Final Principle

Use the simplest system capable of reliably producing the required business outcome.

Add intelligence, agency, autonomy, tools, memory, multiple agents, and infrastructure only when the business problem justifies the additional complexity.