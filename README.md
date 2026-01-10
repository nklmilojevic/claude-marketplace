# Claude Code Plugin Marketplace

A collection of Claude Code plugins for development workflows.

## Plugins

### spec-interviewer

Interview users about their specifications to uncover hidden requirements, edge cases, and tradeoffs before implementation begins.

**Trigger phrases:**
- "interview me about my spec"
- "review my specification"
- "help me flesh out my spec"
- "find gaps in my specification"

### plugin-development

Development toolkit for creating Claude Code plugins with scaffolding commands, validation, and best practices guidance.

**Commands:**
- `/plugin-development:init` - Scaffold a new plugin
- `/plugin-development:add-command` - Add a slash command
- `/plugin-development:add-skill` - Add a skill
- `/plugin-development:add-agent` - Add a sub-agent
- `/plugin-development:add-hook` - Add a hook
- `/plugin-development:validate` - Validate plugin structure

## Installation

```bash
# Add the marketplace
/plugin marketplace add nkl/claude-marketplace

# Install a plugin
/plugin install spec-interviewer@nkl-plugins
/plugin install plugin-development@nkl-plugins
```

## Repository Structure

```
├── .claude-plugin/
│   └── marketplace.json          # Marketplace configuration
├── .github/
│   └── workflows/
│       └── validate-plugins.yml  # CI/CD validation
├── docs/                         # Documentation
└── plugins/
    ├── spec-interviewer/         # Spec interview skill
    └── plugin-development/       # Plugin development toolkit
```

## License

MIT
