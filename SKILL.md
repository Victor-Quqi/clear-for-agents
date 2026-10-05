---
name: clear-for-agents
description: >-
  MUST read before drafting or revising any text an agent will later read:
  subagent and delegation prompts, resume and handoff messages,
  CLAUDE.md/AGENTS.md, skills, tool descriptions, and reference docs.
---

# Clear for agents

Write only the additional information needed to complete the task, accounting for the recipient's existing context and capabilities.

This skill applies to content the current task requires writing or revising. Preserve the purpose and organization of documents shared by humans and agents.

## Decide whether it needs to be written

Remove information already clear in the recipient's visible context, common knowledge the model already has, and steps it would take by default.

For every paragraph, sentence, and modifier, ask: what necessary information would the recipient lose, or what specific judgment would go wrong, if this were removed? If you cannot name its function, delete it.

Check whether the remaining text implies unsupported priorities, restricts possible solutions, or shifts the original task.

## Add only what the actual context lacks

When resuming the same session with an unchanged task and available context, send only `continue` by default. Add information only for new requirements, changed state, or confirmed gaps in context.

For subagent assignments and handoffs, fill gaps based on the context the recipient actually inherits. Include objectives, status, material locations, work ownership, and delivery requirements only where missing.

Summaries retain only the decisions, state, and unfinished work needed to continue, distinguishing verified results from assumptions. Make completion criteria checkable when the task needs them; leave implementation details to the recipient.

## Leave room for judgment in review, exploration, and research

Provide the subject or question, actual constraints, and necessary task context. Let the recipient determine focus, approach, and conclusions through inspection and evidence.

For independent review, never request a focus on particular changes merely because they were just made. Preserve the user's specified scope; provide evidence such as recorded failures as facts.

Include guesses in exploratory tasks only when grounded in evidence specific to the task and useful to the investigation. Label them as hypotheses to verify. Check examples and suggested directions for premature constraints on the answer.

When delegating web research, omit background knowledge both agents likely share. The main agent's judgments from pretrained knowledge, unverified online, must not become research premises, mandatory checklists, or predetermined conclusions. Let retrieved evidence guide the research direction.

## Make information easy to find

Keep one authoritative statement of each point, with a concept's definition, requirements, and exceptions together. Organize longer content around how it will be used. Keep shared requirements in the main text and separate branch details as needed.

When referencing material, state what it contains, when to read it, and an accessible location. Apply the same approach to skill descriptions and document pointers so the recipient can decide when to read them.

For information that is easy to find in the environment and likely to change, prefer a lookup pointer.

## Limit what gets persisted

Repository documents describe what is currently valid and relevant to their purpose. Keep task progress, attempted approaches, provisional judgments, and validation records from the current run in the conversation or necessary handoffs. When the user requests process records or the project has a dedicated mechanism, use the corresponding location.

Retain decision rationale only when omitting it would affect usage or maintenance judgments. Keep it brief and beside the relevant rule or design. Use the project's existing mechanisms for historical tracking.

Integrate current conclusions into the existing locations within the task's scope, replacing outdated statements instead of appending a running history of edits. Include dates or versions only when they affect interpretation.
