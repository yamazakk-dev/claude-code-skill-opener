# opener

Claude Code skill to open the current project directory in various applications and services.

## Targets

| Target | Description |
|--------|-------------|
| `finder` | Open in Finder |
| `vscode` | Open in VS Code |
| `terminal` | Open in Terminal.app |
| `github` | Open GitHub repository page |
| `vercel` | Open Vercel dashboard |
| `pr` | Open current branch's Pull Request |

## Usage

```
/opener finder
/opener github
/opener pr
```

Running `/opener` without arguments displays the available targets.

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
- [GitHub CLI (`gh`)](https://cli.github.com/) — required for `github` and `pr` targets
- [VS Code CLI (`code`)](https://code.visualstudio.com/) — required for `vscode` target

## Installation

Copy `SKILL.md` to your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/opener
cp SKILL.md ~/.claude/skills/opener/
```

## License

MIT
