---
title: "Claude Code 完全ガイド：全32スラッシュコマンド解説"
emoji: "🤖"
type: "tech"
topics: ["Claude", "ClaudeCode", "AI", "LLM", "開発ツール"]
published: true
---

Claude Code（claude.ai/code）の**全32個のビルトインスラッシュコマンド**を網羅的に解説します。

---

## 目次

1. [会話・セッション管理](#会話セッション管理)
2. [プロジェクト・設定管理](#プロジェクト設定管理)
3. [開発・外部連携](#開発外部連携)
4. [タスク実行・レビュー](#タスク実行レビュー)
5. [システム・その他](#システムその他)

---

## 会話・セッション管理（10コマンド）

### `/help`
ヘルプとコマンド一覧を表示

### `/clear`
会話履歴をクリアしてリセット

### `/compact`
会話を圧縮してコンテキストを節約

### `/context`
現在のコンテキスト（トークン）使用状況を表示

### `/cost`
セッションのトークン消費とコストを表示

### `/exit`
Claude Codeを終了（`/quit`のエイリアスあり）

### `/export`
会話履歴をファイルやクリップボードに出力

### `/rename`
セッション名を変更

### `/resume`
過去のセッションをIDや名前で検索して再開

### `/rewind`
直前の会話やコード変更を取り消し（`/checkpoint`のエイリアスあり）

---

## プロジェクト・設定管理（8コマンド）

### `/init`
プロジェクトを初期化、CLAUDE.mdを作成

### `/config`
設定インターフェースを開く

### `/memory`
CLAUDE.md（プロジェクト固有のルール）を編集

### `/model`
AIモデル（Sonnet, Opus, Haiku）を変更

### `/permissions`
ツール実行などの権限設定

### `/privacy-settings`
プライバシー設定の確認・更新（Pro/Max限定）

### `/add-dir`
AIが読み取れる作業ディレクトリを追加

### `/status`
現在のセッション状態を表示

---

## 開発・外部連携（7コマンド）

### `/mcp`
MCPサーバー（外部ツール連携）を管理

### `/ide`
エディタ（VSCodeなど）との統合を管理

### `/install-github-app`
リポジトリ用GitHub Actionsをセットアップ

### `/plugin`
プラグインを管理

### `/hooks`
ツールイベント用のフックを管理

### `/sandbox`
サンドボックス環境を有効化

### `/agents`
AIサブエージェントを管理

---

## タスク実行・レビュー（2コマンド）

### `/review`
コードのレビューを依頼

### `/pr-comments`
プルリクエストのコメントを読み込み表示

---

## システム・その他（5コマンド）

### `/doctor`
インストール状態や依存関係を診断

### `/bug`
Anthropicにバグを報告

### `/login`
アカウントのログイン・切り替え

### `/logout`
サインアウト

### `/release-notes`
最新のリリースノートを表示

---

## 全コマンド一覧

| コマンド | 説明 |
|---------|------|
| `/help` | ヘルプ表示 |
| `/clear` | 会話クリア |
| `/compact` | コンテキスト圧縮 |
| `/context` | トークン使用状況 |
| `/cost` | コスト表示 |
| `/exit` | 終了 |
| `/export` | 会話エクスポート |
| `/rename` | セッション名変更 |
| `/resume` | セッション再開 |
| `/rewind` | 巻き戻し |
| `/init` | プロジェクト初期化 |
| `/config` | 設定を開く |
| `/memory` | CLAUDE.md編集 |
| `/model` | モデル変更 |
| `/permissions` | 権限設定 |
| `/privacy-settings` | プライバシー設定 |
| `/add-dir` | ディレクトリ追加 |
| `/status` | ステータス表示 |
| `/mcp` | MCP管理 |
| `/ide` | IDE連携 |
| `/install-github-app` | GitHub App設定 |
| `/plugin` | プラグイン管理 |
| `/hooks` | フック管理 |
| `/sandbox` | サンドボックス |
| `/agents` | エージェント管理 |
| `/review` | コードレビュー |
| `/pr-comments` | PRコメント確認 |
| `/doctor` | 環境診断 |
| `/bug` | バグ報告 |
| `/login` | ログイン |
| `/logout` | ログアウト |
| `/release-notes` | リリースノート |

---

## モデルの使い分け

```
# 難しい問題
/model opus

# 日常開発（デフォルト）
/model sonnet

# 単純なタスク・高速
/model haiku
```

公式ドキュメント: https://docs.anthropic.com/claude-code

Happy Coding with Claude!
