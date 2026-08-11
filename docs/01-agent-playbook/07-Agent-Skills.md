# Agent Skills

## Purpose

This document explains what an Agent Skill is, how it differs from tools and instructions and why reusable skills are important when designing agent systems.

---

# What Is an Agent Skill?

An Agent Skill is a reusable package of instructions, knowledge, procedures, and potentially tools that teaches an agent how to perform a specific type of work.

A skill represents:

"How do I perform this capability correctly?"

Examples:

- Analyze customer health
- Prepare a QBR
- Screen a candidate
- Perform account research
- Create an implementation handoff
- Analyze a business workflow

---

# Agent vs Skill

An Agent has:

- Identity
- Goal
- Responsibilities
- Decision-making authority
- Tools
- Guardrails

A Skill provides:

- Specialized instructions
- Procedures
- Domain knowledge
- Best practices
- Output requirements
- Supporting resources

The agent decides when a capability is needed.

The skill teaches the agent how to perform that capability.

---

# Skill vs Tool

These are different.

## Skill

Tells the agent:

HOW to perform work.

Example:

"How to evaluate customer health."

## Tool

Allows the agent to:

DO something in another system.

Example:

"Retrieve customer usage data from the CRM."

Remember:

Skill = HOW

Tool = DO

---

# Skill vs Prompt

A prompt provides instructions for a particular interaction or task.

A skill is a reusable capability that may contain multiple instructions, procedures, examples, knowledge sources, and tool guidance.

Remember:

Prompt = instruction

Skill = reusable capability

---

# What Can a Skill Contain?

A skill may include:

- Purpose
- When to use it
- When not to use it
- Required inputs
- Step-by-step procedure
- Decision rules
- Knowledge
- Tool instructions
- Examples
- Output format
- Guardrails
- Evaluation criteria

---

# Example — Customer Health Analysis Skill

Purpose:

Determine the health of a customer account.

Inputs:

- Product usage
- Support history
- Customer sentiment
- Renewal date
- Engagement history

Procedure:

1. Review product usage.
2. Review support issues.
3. Review customer engagement.
4. Identify risk indicators.
5. Identify positive indicators.
6. Determine health classification.
7. Explain reasoning.
8. Recommend next action.

Output:

- Health status
- Risk factors
- Positive indicators
- Recommended action
- Confidence

The same skill could potentially be used by multiple agents.

---

# Why Skills Matter

Without reusable skills, the same business logic gets recreated repeatedly.

Skills allow organizations to capture operational expertise once and reuse it across AI systems.

This creates:

- Consistency
- Reusability
- Portability
- Faster development
- Easier maintenance
- Better governance

---

# Portable Skills

Whenever practical, skills should describe the business capability independently from a specific model or framework.

Instead of:

"Claude performs these steps..."

Prefer:

"The agent performs these steps..."

This helps make the skill portable across:

- Different LLMs
- Different agent frameworks
- Different applications
- Future technology changes

---

# Agent + Skills + Tools

A useful mental model:

AGENT
= Who owns the work?

SKILL
= How does it know how to perform the work?

TOOL
= What can it use to perform the work?

---

# Example

Customer Success Agent

↓

Uses:

Customer Health Analysis Skill

QBR Preparation Skill

Renewal Risk Skill

↓

Uses Tools:

CRM

Product Analytics

Support Platform

Email

Slack

---

# Key Takeaway

Agents should not contain every business procedure directly inside their core instructions.

Reusable operational knowledge can be separated into Skills that agents invoke when needed.

This makes agent systems more modular, maintainable, and portable.