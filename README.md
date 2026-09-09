# clear-for-agents

[简体中文](README.zh-CN.md)

A skill for writing content that other agents will use. Include only the additional information the recipient needs to complete the task.

The motivation is simple: resuming a session with an unchanged task and available context usually needs just `continue`. Agents often add task restatements, progress summaries, and reminders. These distract from the work and can even change an otherwise clear task.

The same problem appears in subagent prompts, review assignments, research tasks, and repository documentation. This skill asks one question to decide whether text earns its place:

> If this were removed, what necessary information would the recipient lose, or what specific judgment would go wrong?

## Scope

Prompts, subagent assignments, session resumes and handoffs, skills, tool descriptions, and reference documents. Applies to temporary messages, persistent files, and content shared by humans and agents.

It addresses several recurring problems:

- **Repeated context.** Omit requirements the recipient already knows, common knowledge, and steps it would take by default. Resume the same task with just `continue` by default.
- **Predetermined review focus.** Keep independent reviews within the task's scope and let the reviewer decide what deserves attention through inspection.
- **Restricted research direction.** Give web research the question, actual constraints, and necessary background. Let retrieved evidence guide the direction.
- **Process logs in documentation.** Keep intermediate state in the conversation or necessary handoffs. Update repository documentation in place with current conclusions, using existing project mechanisms for process records.

Preserve the purpose and organization of shared documents, with edits limited to the current task's scope.

## Installation and usage

Install from GitHub with the [skills CLI](https://github.com/vercel-labs/skills):

```sh
npx skills add Victor-Quqi/clear-for-agents -g
```

Follow the prompts to select your agent. `-g` installs globally for use across projects; omit it to install in the current project.

Environments that support automatic skill selection can match it to relevant tasks. You can also invoke it explicitly with `/clear-for-agents` or `$clear-for-agents`, depending on your environment's syntax.

See [SKILL.md](SKILL.md) for the full instructions.

## License

[MIT](LICENSE)
