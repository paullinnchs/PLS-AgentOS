# Agent Orchestration and Agent Managers

## Purpose

This document explains how multiple agents, skills, tools, and workflows are coordinated to accomplish larger business objectives.

---

# What Is Agent Orchestration?

Agent Orchestration is the coordination of work across agents, tools, skills, systems, and humans.

It answers:

"What should happen next, and who or what should do it?"

Remember:

Orchestration = Traffic Control

---

# Why Is Orchestration Needed?

A single agent may be capable of completing an entire task.

But larger business processes often require different capabilities.

Example:

Customer onboarding may require:

- Contract analysis
- Customer data validation
- Account configuration
- Implementation planning
- Customer communication
- Reporting

Instead of creating one enormous agent responsible for everything, specialized capabilities can be coordinated.

---

# Single-Agent Architecture

A single agent owns the objective and uses multiple skills and tools.

Example:

CUSTOMER SUCCESS AGENT

↓

Customer Health Skill

QBR Preparation Skill

Renewal Risk Skill

↓

CRM + Support + Analytics Tools

This can be effective when one agent can reasonably own the objective.

---

# Multi-Agent Architecture

Multiple specialized agents collaborate toward a larger objective.

Example:

CUSTOMER ONBOARDING

↓

MANAGER / SUPERVISOR AGENT

↓

Contract Agent

↓

Implementation Agent

↓

Customer Communication Agent

↓

Reporting Agent

Each agent owns a narrower responsibility.

---

# What Is an Agent Manager?

An Agent Manager is an agent or control layer responsible for coordinating other specialized agents.

It may:

- Receive the overall objective
- Break work into tasks
- Determine which agent should handle each task
- Delegate work
- Review results
- Request additional work
- Handle exceptions
- Escalate to humans
- Determine when the objective is complete

Other common terms may include:

- Supervisor Agent
- Manager Agent
- Router
- Coordinator
- Orchestrator

The exact implementation varies by architecture.

---

# Example

Goal:

Prepare an enterprise customer for implementation.

↓

MANAGER AGENT

Determines what work is required.

↓

CONTRACT AGENT

Extracts requirements from the signed agreement.

↓

MANAGER

Reviews result and determines next action.

↓

IMPLEMENTATION AGENT

Creates implementation requirements and project plan.

↓

MANAGER

Determines customer communication is required.

↓

COMMUNICATION AGENT

Drafts kickoff communication.

↓

HUMAN APPROVAL

Communication is reviewed.

↓

MANAGER

Confirms required work is complete.

↓

COMPLETE

---

# Delegation

Delegation means assigning responsibility for a task to another agent or capability.

A manager may delegate based on:

- Agent specialization
- Required skill
- Available tools
- Permissions
- Business rules
- Current state

---

# Handoffs

A handoff occurs when responsibility moves from one agent to another.

A good handoff should include:

- Objective
- Relevant context
- Required inputs
- Work already completed
- Expected output
- Constraints

Poor handoffs create the same problems between AI agents that poor handoffs create between human teams.

---

# Routing

Routing determines where work should go.

Example:

Incoming customer request

↓

Billing question?

→ Billing Agent

Technical issue?

→ Support Agent

Implementation question?

→ Implementation Agent

Strategic issue?

→ Human CSM

Routing does not necessarily require an AI agent.

Simple routing rules may be deterministic automation.

---

# Manager Agent vs Deterministic Orchestration

Not every system needs an AI manager.

## Deterministic Orchestration

Use predefined logic when routing is predictable.

Example:

IF request_type = billing

THEN send to billing workflow.

## Agentic Orchestration

Use an agent when coordination requires interpretation, reasoning, or adaptation.

Example:

Review an ambiguous customer situation, determine which specialists are needed, coordinate their work, evaluate the results, and decide the next action.

Remember:

If the path is known beforehand, deterministic orchestration may be better.

If the path must be determined at runtime, agentic orchestration may be appropriate.

---

# Manager Agent vs Harness

These are different.

MANAGER AGENT

Coordinates the work.

HARNESS

Provides the environment in which the agents operate.

Remember:

Manager = Manager

Harness = Workplace / Operating Environment

---

# Manager Agent vs Skill

Do not create another agent simply because specialized knowledge is required.

Sometimes the correct architecture is:

ONE AGENT

+

MULTIPLE SKILLS

rather than:

MULTIPLE AGENTS

A separate agent becomes useful when a capability needs its own:

- Responsibility
- Context
- Tools
- Permissions
- Decision-making
- Guardrails
- Lifecycle

---

# Human Managers

Humans can remain part of the orchestration architecture.

Example:

Manager Agent

↓

Research Agent

↓

Analysis Agent

↓

Recommendation

↓

HUMAN DECISION

↓

Execution Agent

Multi-agent architecture does not mean removing humans.

---

# The Enterprise Model

BUSINESS OBJECTIVE

↓

ORCHESTRATION / MANAGER

↓

SPECIALIZED AGENTS

↓

SKILLS

↓

TOOLS + KNOWLEDGE

↓

ACTIONS

↓

RESULTS

↓

MANAGER EVALUATION

↓

Continue / Reassign / Escalate / Complete

↓

BUSINESS OUTCOME

---

# Key Principle

Do not build multiple agents simply because you can.

Use the simplest architecture capable of reliably accomplishing the business objective.

Start with:

Automation

Then consider:

Single Agent + Skills

Then consider:

Multiple Agents

Add complexity only when the business problem requires it.

---

# Key Takeaway

Agent orchestration coordinates work.

A Manager Agent can dynamically delegate and supervise work.

Specialized Agents own narrower objectives.

Skills provide reusable know-how.

Tools provide capabilities.

The Harness provides the operating environment.

Humans remain part of the system wherever judgment, approval, accountability, or risk requires them.