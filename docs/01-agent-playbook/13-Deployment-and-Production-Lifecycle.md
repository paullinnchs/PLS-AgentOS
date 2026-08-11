# Deployment and Production Lifecycle

## Purpose

This document explains how an agent moves from development into a production environment where it can perform real business work.

Building an agent is only part of the lifecycle.

A production agent must be deployed, configured, secured, monitored, maintained, and improved.

---

# 1. Development

Development is where the agent is created and initially tested.

This may include:

- Agent specification
- Instructions
- Skills
- Tools
- Knowledge
- Memory
- Guardrails
- Evaluation criteria
- Code

Development should use test or dummy data whenever appropriate.

---

# 2. Testing

Before production, the agent should be tested against expected and unexpected scenarios.

Examples:

- Normal inputs
- Missing information
- Incorrect information
- Tool failures
- Permission failures
- Edge cases
- Human approval
- Stop conditions

Testing asks:

"Does the system behave as designed?"

---

# 3. Environment

An environment is where software runs.

Common environments include:

## Local

Runs on the developer's computer.

Useful for:

- Building
- Experimenting
- Debugging

## Development / Test

A separate environment used for controlled testing.

## Staging

An environment designed to closely resemble production before release.

## Production

The live environment where the agent performs real business work.

Remember:

LOCAL → TEST → STAGING → PRODUCTION

Not every small project requires every environment, but production systems should separate experimentation from live business operations.

---

# 4. Deployment

Deployment means making the agent available in an environment where it can run.

Deployment may place the agent on:

- Cloud infrastructure
- Server
- Container
- Serverless platform
- Agent platform
- Enterprise infrastructure

The deployment method depends on the architecture and business requirements.

---

# 5. Invocation

Once deployed, something must start the agent.

This is called invocation or triggering.

Examples:

## Human Trigger

A user requests work.

## Event Trigger

A business event occurs.

Example:

Contract signed.

## Schedule

Agent runs at a defined time.

Example:

Review customer risk every Monday.

## API Call

Another application requests the agent.

## Webhook

Another system sends an event notification.

Example:

ATS sends notification when a new candidate applies.

---

# 6. Configuration

Production settings should generally be separated from the core agent logic.

Examples:

- Model selection
- API endpoints
- Tool access
- Thresholds
- Approval rules
- Environment settings

This allows behavior to be changed without rewriting the entire system.

---

# 7. Secrets

Sensitive credentials should not be stored directly in source code.

Examples:

- API keys
- Passwords
- Access tokens
- Database credentials

These should be managed securely using appropriate environment or secrets-management systems.

Never commit secrets to GitHub.

---

# 8. Permissions

Production agents should receive only the permissions required to perform their responsibilities.

Example:

Customer Health Agent

Needs:

READ CRM

READ support data

CREATE internal task

May not need:

DELETE CRM record

CHANGE contract

ISSUE refund

Least privilege reduces risk.

---

# 9. Monitoring

Once deployed, the system must be monitored.

Examples:

- Is it running?
- Is it failing?
- Are tools working?
- How long does execution take?
- How much does it cost?
- How often does it escalate?
- Are outputs meeting quality standards?

Deployment is not the end of the lifecycle.

---

# 10. Versioning

Agents change over time.

Changes may include:

- Instructions
- Skills
- Tools
- Models
- Business rules
- Knowledge
- Guardrails
- Code

Versions allow teams to know which configuration produced which behavior.

Example:

CustomerHealthAgent v1.0

↓

CustomerHealthAgent v1.1

↓

CustomerHealthAgent v2.0

---

# 11. Rollback

A production change may create unexpected problems.

Rollback means returning to a previously known working version.

This is one reason version control and deployment discipline matter.

---

# 12. Cost Management

Agent systems consume resources.

Possible costs include:

- Model usage
- API calls
- Compute
- Storage
- Databases
- Agent platforms
- Monitoring
- Third-party tools

A technically successful agent that costs more than the value it creates may be a poor business solution.

---

# 13. Maintenance

Production agents require maintenance.

Examples:

- Update instructions
- Update skills
- Replace deprecated APIs
- Refresh knowledge
- Fix tool integrations
- Improve evaluation
- Adjust guardrails
- Change models
- Resolve failures

Agents are operational systems, not one-time projects.

---

# 14. Production Lifecycle

BUSINESS PROBLEM

↓

SPECIFICATION

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

---

# Build vs Buy

Organizations do not always need to build the complete agent infrastructure themselves.

Two broad approaches exist.

## Build

Create and control more of the architecture directly.

Potential advantages:

- Greater control
- Greater customization
- Greater portability

Potential tradeoffs:

- More engineering
- More infrastructure
- More maintenance

## Managed Platform

Use an agent platform that provides portions of the harness and production infrastructure.

Potential advantages:

- Faster deployment
- Less infrastructure work
- Built-in capabilities

Potential tradeoffs:

- Platform dependency
- Cost
- Less architectural control
- Portability considerations

Neither approach is automatically better.

The business and technical requirements should determine the architecture.

---

# Production Readiness

Before calling an agent production-ready, ask:

- Is its purpose clearly defined?
- Has it been tested?
- Are permissions appropriate?
- Are guardrails implemented?
- Are secrets secure?
- Is human oversight defined?
- Can its actions be observed?
- Can failures be detected?
- Can failures be handled safely?
- Can changes be versioned?
- Can we roll back?
- Can we measure business value?

---

# Key Principle

Deployment does not make an agent production-ready.

Production readiness comes from the complete operational system surrounding the agent.

---

# Key Takeaway

Build = Create the system.

Deploy = Make it available to run.

Invoke = Start the work.

Observe = See what happens.

Evaluate = Determine whether it works.

Maintain = Keep it working.

Improve = Make it better over time.