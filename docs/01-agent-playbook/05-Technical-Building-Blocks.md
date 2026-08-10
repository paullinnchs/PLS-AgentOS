# Technical Building Blocks of Enterprise Agents

## Purpose

This document maps common AI technologies and concepts to the Enterprise Agent Stack.

The goal is not to memorize products.

The goal is to understand what problem each technology solves and where it belongs in the architecture.

---

# 1. LLM — Large Language Model

## What is it?

The LLM provides the core language understanding and reasoning capability.

Examples:

- OpenAI models
- Claude
- Gemini

## What does it do?

It can:

- Interpret language
- Generate language
- Analyze information
- Reason about problems
- Generate structured outputs

## Where does it fit?

MODEL / INTELLIGENCE

## Remember

LLM = the reasoning engine.

An LLM by itself is not an agent.

---

# 2. Prompt / Instructions

## What is it?

Instructions tell the model what role it has, what objective it should accomplish, and what rules it must follow.

## Where does it fit?

INSTRUCTIONS

## Remember

Prompt = directions for the intelligence.

---

# 3. API — Application Programming Interface

## What is it?

An API allows one software system to communicate with another software system.

Example:

An agent needs customer information from Salesforce.

The API provides a defined way to request that information.

## Where does it fit?

TOOLS / INTEGRATIONS

## Remember

API = software talks to software.

---

# 4. MCP — Model Context Protocol

## What is it?

MCP is a standard way for AI applications to connect with external tools, data, and capabilities.

Instead of creating a unique integration approach for every AI application, MCP provides a common protocol for exposing capabilities to AI systems.

## Where does it fit?

TOOLS / INTEGRATIONS

## Remember

API = how software systems communicate.

MCP = a standardized way to make tools and context available to AI applications.

---

# 5. RAG — Retrieval-Augmented Generation

## What is it?

RAG allows an AI system to retrieve relevant information from external knowledge before generating its response.

Example:

Question:

"What is our refund policy?"

Instead of relying only on what the LLM learned during training, the system retrieves the company's current refund policy and provides that information to the model.

## Where does it fit?

KNOWLEDGE

## Remember

RAG = retrieve relevant knowledge before answering.

---

# 6. Memory

## What is it?

Memory allows an agent to retain useful information across interactions or workflow steps.

Examples:

- Previous conversation
- Previous decision
- Customer preference
- Current workflow state

## Where does it fit?

MEMORY

## Remember

RAG retrieves knowledge.

Memory preserves context.

---

# 7. Tool Calling

## What is it?

Tool calling allows the model to request that a defined tool perform an operation.

Example:

The model determines:

"I need the customer's account information."

It calls:

get_customer_account()

The application executes the tool and returns the result.

## Where does it fit?

TOOLS + ACTION

## Remember

Tool calling = the model can request capabilities beyond generating text.

---

# 8. Orchestration

## What is it?

Orchestration coordinates the sequence and routing of work.

It determines things such as:

- What happens next?
- Which tool should run?
- Which agent should handle this?
- Should the process continue?
- Should a human become involved?

## Where does it fit?

DECISION / ORCHESTRATION

## Remember

Orchestration = traffic control.

---

# 9. Agent Framework / Harness

## What is it?

A framework or harness provides infrastructure for building and running agents.

It may manage:

- Model calls
- Tools
- Instructions
- State
- Agent handoffs
- Execution loops
- Guardrails
- Tracing

Examples will be evaluated later in the curriculum.

## Where does it fit?

ACROSS MULTIPLE LAYERS

## Remember

The model provides intelligence.

The harness provides the operating environment around the intelligence.

---

# 10. Evaluation

## What is it?

Evaluation measures whether the agent's behavior and outputs meet defined expectations.

Examples:

- Was the answer accurate?
- Did it use the correct tool?
- Did it follow policy?
- Did it accomplish the objective?
- Did the business outcome improve?

## Where does it fit?

EVALUATION

## Remember

Evaluation = prove that the system works.

---

# Simple Mental Map

LLM
= Think

Prompt
= Instructions

API
= Software connection

MCP
= Standardized AI-to-tool/context connection

RAG
= Retrieve knowledge

Memory
= Remember context

Tool Calling
= Use capabilities

Orchestration
= Coordinate what happens

Agent Harness
= Environment that runs the agent

Evaluation
= Measure whether it worked