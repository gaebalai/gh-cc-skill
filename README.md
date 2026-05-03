# gh-cc-skill

GitHub CLI extension for installing [Claude Code](https://claude.ai/code) skills from any GitHub repository.

> **Note:** GitHub now ships an official `gh skill` command (preview) that supports Claude Code via `gh skill install <owner/repo> --agent claude-code`. This extension predates that and uses a simpler convention (`commands/*.md` → `~/.claude/commands/`); prefer the official command for new setups.

## Install the extension

```bash
gh extension install gaebalai/gh-cc-skill
```

## Usage

```bash
gh cc-skill install <owner/repo>
```

Copies all `commands/*.md` files from the specified repository to `~/.claude/commands/`, then restart Claude Code to activate.

### Options

| Option | Description |
|--------|-------------|
| `--dir <path>` | Override install directory (default: `~/.claude/commands/`) |

## Example

```bash
# Install the cc-security-scan skill set
gh cc-skill install gaebalai/cc-security-scan
```

Installs `/security-review`, `/full-scan`, and `/security-scan` into Claude Code.

## Environment variables

| Variable | Default | Description |
|----------|---------|-------------|
| `CLAUDE_COMMANDS_DIR` | `~/.claude/commands/` | Override install directory |
