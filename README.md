# gh-skill

GitHub CLI extension for installing [Claude Code](https://claude.ai/code) skills from any GitHub repository.

## Install the extension

```bash
gh extension install gaebalai/gh-skill
```

## Usage

```bash
gh skill install <owner/repo>
```

Copies all `commands/*.md` files from the specified repository to `~/.claude/commands/`, then restart Claude Code to activate.

### Options

| Option | Description |
|--------|-------------|
| `--dir <path>` | Override install directory (default: `~/.claude/commands/`) |

## Example

```bash
# Install the claude-security-scan skill set
gh skill install gaebalai/cc-security-scan
```

Installs `/security-review`, `/full-scan`, and `/security-scan` into Claude Code.

## Environment variables

| Variable | Default | Description |
|----------|---------|-------------|
| `CLAUDE_COMMANDS_DIR` | `~/.claude/commands/` | Override install directory |
