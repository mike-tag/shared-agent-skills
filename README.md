# Shared Agent Skills

Reusable Agent Skills maintained by [@mike-tag](https://github.com/mike-tag). The repository follows the open `SKILL.md` format and includes marketplaces for Codex and Claude Code.

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

## Install in Codex

Add this repository as a Codex marketplace:

```text
codex plugin marketplace add mike-tag/shared-agent-skills
```

Restart the ChatGPT desktop app, open **Plugins**, select **Mike Tag Skills**, and install **Design Planning**.

In Codex CLI or the IDE extension, type `$plan-design-decisions` to select the skill. You can also prompt it directly:

```text
Use $plan-design-decisions to interview me and create an implementation-ready design plan.
```

Codex can also select the skill automatically when a request matches its description.

Refresh the Codex marketplace with:

```text
codex plugin marketplace upgrade mike-tag-skills
```

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
├── .agents/
│   └── plugins/
│       └── marketplace.json
├── .claude-plugin/
│   └── marketplace.json
└── plugins/
    └── design-planning/
        ├── .claude-plugin/plugin.json
        ├── .codex-plugin/plugin.json
        └── skills/
            └── plan-design-decisions/
                ├── agents/openai.yaml
                └── SKILL.md
```

## Add another skill

1. Decide whether the skill belongs in an existing plugin or needs a new plugin.
2. Add it under `plugins/<plugin-name>/skills/<skill-name>/SKILL.md`.
3. For a new plugin, add both `.claude-plugin/plugin.json` and `.codex-plugin/plugin.json` inside its plugin directory.
4. Register a new plugin in both root marketplace files: `.claude-plugin/marketplace.json` and `.agents/plugins/marketplace.json`.
5. Keep each skill focused, make its trigger description specific, and place reusable details in supporting files only when needed.
6. Validate the Claude marketplace before publishing:

```text
claude plugin validate .
```

7. Parse both marketplace and plugin manifests, then commit and push. Claude retrieves the unpinned plugin from the latest Git commit; increment the Codex plugin version when releasing a changed plugin.

## License

MIT
