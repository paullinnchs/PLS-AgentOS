# The Enterprise Agent Stack

## Purpose

The Enterprise Agent Stack is a mental model for understanding how a business problem becomes an AI-enabled business outcome.

Each layer has a distinct responsibility.

---

# 1. Business Problem

What operational problem are we trying to solve?

Examples:

- Customer onboarding is too slow
- Recruiters spend too much time on manual screening
- Renewal risk is identified too late
- Implementation handoffs are inconsistent

Everything starts here.

---

# 2. Agent Specification

What should the system actually do?

This is where the PLS Agent Design Canvas is used.

It defines:

- Purpose
- Scope
- Stakeholders
- Success criteria
- Inputs
- Outputs
- Tools
- Risks
- Guardrails
- Business impact

No coding should begin before this is clear.

---

# 3. Model / Intelligence

What provides the reasoning capability?

Usually this is a Large Language Model (LLM).

Examples:

- OpenAI models
- Claude
- Gemini

The model provides language understanding and reasoning capability.

The model alone is not the agent.

---

# 4. Instructions

How should the system behave?

Instructions define:

- Role
- Objective
- Rules
- Constraints
- Expected behavior
- Output requirements

These instructions guide the model toward the intended business objective.

---

# 5. Knowledge

What information can the agent reference?

Examples:

- SOPs
- Policies
- Product documentation
- Customer records
- Company knowledge
- Contracts
- Help documentation

Knowledge is information the agent retrieves when needed.

---

# 6. Memory

What information should the agent retain?

Examples:

- Previous interactions
- Decisions already made
- Workflow state
- Customer preferences
- Task history

Memory provides continuity.

Knowledge = what the agent can look up.

Memory = what the agent remembers.

---

# 7. Tools

What systems can the agent use?

Examples:

- CRM
- Email
- Slack
- Calendar
- Database
- ATS
- APIs
- Internal systems

Tools allow the agent to interact with the outside world.

Without tools, the agent can reason but cannot perform meaningful operational work.

---

# 8. Decision / Orchestration

How does the system determine what happens next?

This layer may decide:

- Which tool to use
- Which task happens next
- Whether another agent should be involved
- Whether the workflow should stop
- Whether a human needs to review something

This is where coordination happens.

---

# 9. Action

What does the system actually do?

Examples:

- Update CRM
- Send a message
- Create a task
- Generate a report
- Schedule a meeting
- Escalate an issue
- Update a database

This is the execution layer.

---

# 10. Evaluation

Did the system complete the task correctly?

Evaluation may measure:

- Accuracy
- Quality
- Completeness
- Confidence
- Policy compliance
- Business KPI achievement

Evaluation helps determine whether the work was successful.

---

# 11. Human Oversight

Where should a person remain involved?

Examples:

- Approval before customer communication
- Approval before financial action
- Review of low-confidence decisions
- Escalation of unusual situations

Human oversight is part of the architecture, not a failure of automation.

---

# 12. Business Outcome

Did the system create measurable value?

Examples:

- Time saved
- Cost reduced
- Revenue protected
- Revenue increased
- Risk reduced
- Faster service
- Better customer experience

The business outcome determines whether the system was worth building.

---

# The Stack

Business Problem

↓

Agent Specification

↓

Model / Intelligence

↓

Instructions

↓

Knowledge + Memory

↓

Tools

↓

Decision / Orchestration

↓

Action

↓

Evaluation

↓

Human Oversight

↓

Business Outcome

---

# Key Principle

An AI agent is not one technology.

It is a system made up of multiple layers working together to achieve a business objective.

Technologies and frameworks will change.

The architectural responsibilities represented by these layers remain much more durable.