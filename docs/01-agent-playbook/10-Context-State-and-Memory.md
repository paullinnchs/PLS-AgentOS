# Context, State, and Memory

## Purpose

This document explains the differences between Context, State, and Memory in an agent system.

All three help an agent understand its situation, but they serve different purposes.

---

# 1. Context

## What is Context?

Context is the information available to the agent for the current reasoning step.

It answers:

"What information do I have available right now?"

Examples:

- Current user request
- Agent instructions
- Retrieved documents
- Tool results
- Relevant conversation history
- Current customer information

Context is what the model can currently "see."

---

# Example

A Customer Success Agent is evaluating an account.

Its current context might include:

- Customer name
- Renewal date
- Product usage
- Three recent support tickets
- Health scoring instructions
- Current task

The model uses this information to reason about the account.

---

# Context Window

LLMs have limits on how much information they can process at one time.

This available space is commonly called the context window.

Therefore:

Having information stored somewhere does not automatically mean the model currently has that information in context.

The system must determine what information is relevant and provide it when needed.

---

# 2. State

## What is State?

State represents the current condition or position of an active process.

It answers:

"Where are we right now?"

Examples:

- Task started
- Contract validated
- Waiting for customer information
- Human approval required
- Tool execution completed
- Workflow complete

---

# Example

Implementation workflow:

Contract Received

↓

Requirements Extracted ✓

↓

Customer Record Created ✓

↓

Implementation Data Requested ✓

↓

WAITING FOR CUSTOMER ← CURRENT STATE

↓

Kickoff Scheduled

↓

Implementation Started

State allows the system to know where the process currently stands.

---

# 3. Memory

## What is Memory?

Memory is information retained so it can be useful later.

It answers:

"What should I remember?"

Examples:

- Customer preferences
- Previous decisions
- Prior interactions
- Historical outcomes
- User preferences
- Lessons from previous tasks

Memory provides continuity across interactions or processes.

---

# Example

A Customer Success Agent may remember:

"Customer prefers executive reviews on Tuesdays."

That preference may not be relevant to every task.

But when scheduling the next QBR, the system can retrieve that memory and place it into the current context.

---

# The Relationship

MEMORY

Stores useful information from the past.

↓

RETRIEVAL

Finds relevant information when needed.

↓

CONTEXT

Makes relevant information available to the model now.

↓

AGENT REASONS

↓

ACTION

↓

STATE CHANGES

↓

NEW INFORMATION MAY BECOME MEMORY

This creates continuity over time.

---

# Simple Example

Customer says:

"Always send my reports as PDFs."

## Memory

Customer prefers PDF reports.

Two months later:

"Prepare my monthly report."

## Context

The system retrieves the remembered PDF preference and provides it to the agent.

## State

Report preparation = In Progress.

The agent generates the report.

## State

Report preparation = Complete.

---

# Working Memory

Working memory generally refers to temporary information needed while completing the current task.

Example:

The agent is comparing three customer records during an analysis.

The information may only need to exist during that task.

---

# Long-Term Memory

Long-term memory persists beyond the immediate task or session.

Examples:

- Customer preferences
- Historical decisions
- Prior outcomes
- Important organizational information

Long-term memory should be intentional.

Not everything needs to be remembered.

---

# Why Not Remember Everything?

Unlimited memory creates problems.

Examples:

- Irrelevant information
- Outdated information
- Privacy risk
- Conflicting information
- Higher processing costs
- Poorer reasoning

Good agent architecture determines:

- What should be remembered?
- How long?
- Who can access it?
- When should it be retrieved?
- When should it be deleted?

---

# Context vs Knowledge

These are also different.

KNOWLEDGE

Information available to be retrieved.

CONTEXT

Information currently provided to the model.

Example:

A company may have 10,000 SOP documents in its knowledge base.

The agent does not need all 10,000 documents in context.

It retrieves the relevant SOP and places that information into context.

---

# State vs Memory

STATE

Where the process currently is.

MEMORY

Information retained for future use.

Example:

State:

Waiting for customer approval.

Memory:

Customer requires CFO approval for purchases over $25,000.

---

# Enterprise Importance

Context, state, and memory require governance.

Organizations must consider:

- Data privacy
- Data retention
- Access permissions
- Accuracy
- Security
- Auditability
- Regulatory requirements

An agent remembering information is not automatically beneficial.

Memory should exist because it improves the business process.

---

# Key Takeaway

Context = What does the agent know RIGHT NOW?

State = Where is the process RIGHT NOW?

Memory = What should the system REMEMBER for later?

Knowledge = What information CAN the agent retrieve?