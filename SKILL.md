---
name: opener
description: 現在のプロジェクトをFinder、VSCode、Terminal、GitHub、Vercelなどで開く
argument-hint: "<finder|vscode|terminal|github|vercel|pr>"
allowed-tools: Bash
---

# opener

現在のプロジェクトディレクトリを指定したアプリケーションやサービスで開くスキル。

`$ARGUMENTS` に指定されたターゲットに応じて、以下のコマンドを実行してください。

## ターゲット一覧

### `finder`
Finderでプロジェクトディレクトリを開く。
```bash
open .
```

### `vscode`
VSCodeでプロジェクトを開く。
```bash
code .
```

### `terminal`
Terminal.appでプロジェクトディレクトリを開く。
```bash
open -a Terminal .
```

### `github`
GitHubリポジトリページをブラウザで開く。
```bash
gh browse
```

### `vercel`
Vercelダッシュボードのプロジェクトページを開く。

1. `.vercel/project.json` が存在するか確認する
2. 存在しない場合は「このプロジェクトにはVercelの設定がありません（.vercel/project.json が見つかりません）」と表示して終了
3. 存在する場合、ファイルから `projectId` を読み取る
4. 以下のコマンドでブラウザを開く：
```bash
open "https://vercel.com/~/projects/<projectId>"
```
※ `<projectId>` は実際の値に置き換える。

### `pr`
現在のブランチのPull Requestページをブラウザで開く。
```bash
gh pr view --web
```

## 引数なし・不明なターゲットの場合

`$ARGUMENTS` が空、または上記以外のターゲットが指定された場合、以下の一覧を表示してください：

```
利用可能なターゲット:
  finder   - Finderで開く
  vscode   - VSCodeで開く
  terminal - Terminal.appで開く
  github   - GitHubリポジトリページを開く
  vercel   - Vercelダッシュボードを開く
  pr       - 現在のブランチのPRページを開く

使い方: /opener <target>
```
