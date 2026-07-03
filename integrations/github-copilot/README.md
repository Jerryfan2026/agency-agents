# GitHub Copilot Integration (VS Code Friendly)

The Agency works with GitHub Copilot out of the box. No conversion needed —
agents use the existing `.md` + YAML frontmatter format.

## Prerequisites / 前置条件

- VS Code installed
- GitHub Copilot extension installed and signed in
- This repository cloned locally

## Install

```bash
# Copy all agents to your GitHub Copilot agent directories
./scripts/install.sh --tool copilot

# Or manually copy one division (example: engineering)
cp engineering/*.md ~/.github/agents/
cp engineering/*.md ~/.copilot/agents/
```

After install, the default paths are:

- `~/.github/agents/`
- `~/.copilot/agents/`

## Use in VS Code / 在 VS Code 里使用

1. Open VS Code
2. Open Copilot Chat (or Agent mode)
3. Start a new chat and call an agent by name

Example prompts:

```text
Activate Frontend Developer and help me build a React component.
```

```text
Use the Reality Checker agent to verify this feature is production-ready.
```

## Troubleshooting / 常见问题排查

### Agent not showing in VS Code / 看不到新 agent

1. Run `Developer: Reload Window`
2. Verify files exist in `~/.github/agents/` or `~/.copilot/agents/`
3. In VS Code Settings, confirm `chat.agentFilesLocations` includes your install path
4. Restart VS Code if needed

### Installed but still not discovered / 已安装但未被识别

- Re-run installer: `./scripts/install.sh --tool copilot`
- Check file format: each file should remain `.md` with valid frontmatter
- Make sure you are signed in to the correct GitHub account in VS Code

## Agent Directory

Agents are organized into divisions. See the [main README](../../README.md) for
the full current roster.
