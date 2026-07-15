# Shared Agent Skills

Reusable Agent Skills maintained by [@mike-tag](https://github.com/mike-tag). The repository follows the open `SKILL.md` format and includes a Claude Code marketplace for straightforward installation.

## Available plugins

### Design Planning

Includes `plan-design-decisions`, an adaptive question-and-answer workflow that turns product and visual design decisions into an implementation-ready plan.

The workflow:

- inspects available product context before asking questions;
- asks one focused question at a time;
- distinguishes confirmed facts, assumptions, recommendations, and open questions;
- compares consequential alternatives and tradeoffs;
- produces sequenced implementation work, acceptance criteria, validation, and risks;
- plans without implementing unless implementation is separately authorized.

## Install in Claude Code

Add this repository as a marketplace:

```text
/plugin marketplace add mike-tag/shared-agent-skills
```

Install the design-planning plugin:

```text
/plugin install design-planning@mike-tag-skills
```

Run the skill directly:

```text
/design-planning:plan-design-decisions
```

Claude can also select the skill automatically when a request matches its description.

## Update

Refresh the marketplace, then update the plugin from Claude Code's plugin manager:

```text
/plugin marketplace update mike-tag-skills
```

## Repository structure

```text
shared-agent-skills/
├── .claude-plugin/
│   └── marketplace.json
└── plugins/
    └── design-planning/
        ├── .claude-plugin/
        │   └── plugin.json
        └── skills/
            └── plan-design-decisions/
                └── SKILL.md
```

## Add another skill

1. Decide whether the skill belongs in an existing plugin or needs a new plugin.
2. Add it under `plugins/<plugin-name>/skills/<skill-name>/SKILL.md`.
3. For a new plugin, add `.claude-plugin/plugin.json` inside its plugin directory and register the plugin in the root marketplace file.
4. Keep each skill focused, make its trigger description specific, and place reusable details in supporting files only when needed.
5. Validate the marketplace before publishing:

```text
claude plugin validate .
```

6. Commit and push. Because the plugin does not pin a version, each new Git commit can be retrieved as an update.

## License

MIT
