# Guardrails, Permissions, and Human-in-the-Loop

## Purpose

This document explains how boundaries, permissions, and human oversight control what an AI agent is allowed to do.

Enterprise agents should operate with defined authority rather than unlimited autonomy.

---

# 1. Guardrails

## What Are Guardrails?

Guardrails are rules and controls that constrain agent behavior.

They answer:

"What boundaries must the agent operate within?"

Examples:

- Do not expose confidential information
- Do not contact customers without approval
- Do not make financial commitments
- Do not modify protected records
- Stop after a defined number of failed attempts
- Escalate when confidence is below an acceptable threshold

Guardrails define acceptable behavior.

---

# 2. Permissions

## What Are Permissions?

Permissions define what systems, data, tools, and actions an agent is authorized to access.

They answer:

"What is this agent allowed to access and do?"

Examples:

READ customer record

CREATE support ticket

UPDATE CRM field

SEND internal Slack message

DO NOT delete customer record

DO NOT issue refund

---

# Least Privilege

A useful enterprise security principle is:

Give the agent only the access required to perform its responsibility.

Example:

If a Customer Health Agent only needs to analyze CRM data:

READ access may be sufficient.

It does not automatically need:

WRITE

DELETE

ADMIN

permissions.

More autonomy should not automatically mean more access.

---

# 3. Human-in-the-Loop

## What Is Human-in-the-Loop?

Human-in-the-Loop (HITL) means intentionally placing a person into the agent process when human judgment, approval, accountability, or intervention is required.

The human is part of the architecture.

---

# Example

Agent identifies a customer as high churn risk.

↓

Agent analyzes account.

↓

Agent recommends intervention.

↓

HUMAN REVIEW

↓

CSM approves strategy.

↓

Agent executes approved follow-up actions.

The agent performs much of the work.

The human retains authority over the consequential decision.

---

# When Should Humans Be Involved?

Common situations include:

## High Impact

The action could materially affect:

- Customer
- Employee
- Revenue
- Financial transaction
- Contract
- Reputation

## Low Confidence

The system is uncertain.

## Exceptions

The situation falls outside normal operating rules.

## Sensitive Data

The task involves protected or sensitive information.

## Irreversible Actions

The action cannot easily be undone.

## Accountability

A person must legally or operationally own the decision.

---

# Approval Gates

An approval gate prevents execution until an authorized person approves an action.

Example:

Agent drafts renewal proposal.

↓

Approval Required

↓

VP approves.

↓

Agent sends proposal.

Approval gates allow agents to prepare work without automatically authorizing every action.

---

# Escalation

Escalation transfers responsibility to a human when the agent reaches a defined boundary.

Examples:

- Confidence too low
- Tool repeatedly fails
- Customer becomes upset
- Policy conflict detected
- Unusual request
- Financial threshold exceeded

A well-designed agent should know when to stop.

---

# Autonomy Levels

Agent autonomy can exist on a spectrum.

## Level 1 — Recommend

Agent analyzes and recommends.

Human acts.

## Level 2 — Prepare

Agent performs work but requires human approval before execution.

## Level 3 — Act Within Limits

Agent can execute predefined low-risk actions independently.

Exceptions require human review.

## Level 4 — High Autonomy

Agent can independently make and execute broader decisions within established boundaries.

Higher autonomy requires stronger:

- Evaluation
- Monitoring
- Permissions
- Guardrails
- Auditability
- Error handling

---

# Example — Customer Success

## Low Risk

Create internal CRM task.

Agent may execute automatically.

## Medium Risk

Draft customer email.

Human approval may be required.

## Higher Risk

Offer customer a contract concession.

Agent should escalate to an authorized human.

Different actions inside the same workflow can have different autonomy levels.

---

# Guardrails vs Permissions

These are related but different.

GUARDRAIL

A rule governing behavior.

Example:

"Do not send customer communications without approval."

PERMISSION

Technical authority.

Example:

The agent does not have permission to call the email send function until approval is recorded.

Strong enterprise systems should not rely only on instructions when technical controls can enforce the boundary.

---

# Human Oversight vs Failure

Human involvement does not mean the agent failed.

A well-designed system intentionally determines:

What should AI do?

What should automation do?

What should a human decide?

The goal is appropriate autonomy, not maximum autonomy.

---

# Auditability

Enterprise systems should be able to reconstruct important agent actions.

Useful records may include:

- What objective was assigned?
- What information was used?
- What tools were called?
- What action was taken?
- Who approved it?
- What result occurred?
- When did it happen?

This supports troubleshooting, governance, compliance, and improvement.

---

# Key Principle

Capability does not equal authority.

An agent may technically be capable of performing an action while intentionally lacking permission to perform it autonomously.

---

# Key Takeaway

Guardrails = What boundaries must it follow?

Permissions = What is it technically allowed to access or do?

Human-in-the-Loop = Where must a person participate?

Escalation = When should the agent give control to a human?

Autonomy = How much can the agent independently decide and execute?