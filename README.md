# opener

現在のプロジェクトディレクトリを、さまざまなアプリケーションやサービスで開く Claude Code スキルです。

## ターゲット一覧

| ターゲット | 説明 |
|-----------|------|
| `finder` | Finder で開く |
| `vscode` | VS Code で開く |
| `terminal` | Terminal.app で開く |
| `github` | GitHub リポジトリページを開く |
| `vercel` | Vercel ダッシュボードを開く |
| `pr` | 現在のブランチの Pull Request ページを開く |

## 使い方

```
/opener finder
/opener github
/opener pr
```

引数なしで `/opener` を実行すると、利用可能なターゲット一覧が表示されます。

## 必要なツール

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
- [GitHub CLI (`gh`)](https://cli.github.com/) — `github`・`pr` ターゲットに必要
- [VS Code CLI (`code`)](https://code.visualstudio.com/) — `vscode` ターゲットに必要

## インストール

`SKILL.md` を Claude Code のスキルディレクトリにコピーしてください：

```bash
mkdir -p ~/.claude/skills/opener
cp SKILL.md ~/.claude/skills/opener/
```

## ライセンス

MIT
