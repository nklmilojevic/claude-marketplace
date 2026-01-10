# nkl-plugins

Claude Code plugin marketplace.

## Plugins

| Plugin | Description |
|--------|-------------|
| [spec-interviewer](https://github.com/nklmilojevic/claude-spec-interviewer) | Interview users about specifications to uncover hidden requirements, edge cases, and tradeoffs |

## Installation

```bash
# Add the marketplace
/plugin marketplace add nklmilojevic/claude-marketplace

# Install a plugin
/plugin install spec-interviewer@nkl-plugins
```

## How it works

This marketplace references plugins hosted in separate GitHub repositories. A GitHub Action runs hourly to check for new releases and automatically creates PRs to update versions.

## Adding a plugin

1. Create a GitHub repository for your plugin with `.claude-plugin/plugin.json`
2. Add an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "my-plugin",
  "description": "What it does",
  "version": "1.0.0",
  "author": { "name": "Your Name" },
  "source": {
    "source": "github",
    "repo": "owner/repo-name"
  }
}
```

3. Create releases in your plugin repository to trigger version updates

## License

MIT
