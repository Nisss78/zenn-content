---
title: "OpenClawのスラッシュコマンド完全ガイド"
emoji: "💻"
type: "tech"
topics: []
published: true
---

---
title: "OpenClawのスラッシュコマンド完全ガイド"
topics: ["openclaw", "ai", "cli", "automation"]
published_at: "2026-03-20 12:00"
---



OpenClawは強力なAIエージェントフレームワークですが、その真価はスラッシュコマンドにあります。この記事では、OpenClawの標準スラッシュコマンドを全て解説します。

## コマンドの基本

### テキストコマンドとネイティブコマンド

OpenClawには2種類のコマンドシステムがあります：

- **テキストコマンド**: `/`で始まるメッセージ（全プラットフォームで動作）
- **ネイティブコマンド**: Discord/Telegram/Slackのネイティブスラッシュコマンド

テキストコマンドはWhatsApp、Signal、iMessage、Google Chat、MS Teamsでも動作します。

### ディレクティブ

一部のコマンドは「ディレクティブ」として扱われます：

- `/think`、`/verbose`、`/reasoning`、`/elevated`、`/exec`、`/model`、`/queue`
- ディレクティブはメッセージから削除され、モデルには見えません
- ディレクティブのみのメッセージの場合、設定がセッションに永続化されます

## 基本コマンド

### ヘルプ・情報系

```bash
/help          # ヘルプを表示
/commands      # コマンド一覧を表示
/status        # 現在のステータス（使用量、モデル情報など）
/whoami        # 自分のSender IDを表示（エイリアス: /id）
```

### セッション管理

```bash
/reset         # 新しいセッションを開始
/new [model]   # 新しいセッションを開始（モデル指定可能）
/stop          # 実行中の処理を停止
```

### コンテキスト確認

```bash
/context                 # コンテキストの概要
/context list            # ファイル一覧
/context detail          # 詳細（ファイルごとのサイズ、ツール、スキル情報）
/context json            # JSON形式で出力
```

### エクスポート

```bash
/export-session [path]   # セッションをHTMLでエクスポート
/export [path]           # エイリアス
```

## AI制御コマンド

### 思考モード制御

```bash
/think off      # 思考なし
/think minimal  # 最小限の思考
/think low      # 低思考
/think medium   # 中程度の思考
/think high     # 高思考
/think xhigh    # 超高思考
# エイリアス: /thinking, /t
```

### 推論表示

```bash
/reasoning off    # 推論を非表示
/reasoning on     # 推論を表示（"Reasoning:"プレフィックス付き）
/reasoning stream # Telegramのドラフト機能を使用
# エイリアス: /reason
```

### 詳細モード

```bash
/verbose on   # 詳細表示を有効化
/verbose full # 完全な詳細表示
/verbose off  # 詳細表示を無効化
# エイリアス: /v
```

**注意**: グループチャットでは`/verbose`と`/reasoning`は注意して使用してください。内部の思考やツール出力が公開されます。

### 権限昇格

```bash
/elevated off   # 昇格なし
/elevated on    # 昇格あり（承認プロンプト付き）
/elevated ask   # 常に確認
/elevated full  # 承認なしで全権限
# エイリアス: /elev
```

### モデル選択

```bash
/model              # モデル選択画面を表示
/model list         # モデル一覧
/model 3            # 番号で選択
/model openai/gpt-5.2  # 直接指定
/model status       # 詳細ステータス（エンドポイント、APIモードなど）
# エイリアス: /models
```

Discordではインタラクティブなピッカーが表示されます。

### 実行設定

```bash
/exec                              # 現在の設定を表示
/exec host=sandbox                 # サンドボックスで実行
/exec host=gateway security=full   # ゲートウェイで完全権限
/exec ask=always                   # 常に承認を要求
```

### キュー制御

```bash
/queue                              # 現在の設定を表示
/queue debounce:2s cap:25 drop:summarize  # 詳細設定
```

## サブエージェント管理

### サブエージェント操作

```bash
/subagents list      # 実行中のサブエージェント一覧
/subagents kill <id> # サブエージェントを停止
/subagents log <id>  # ログを表示
/subagents info <id> # 詳細情報
/subagents send <id> <message>  # メッセージ送信
/subagents steer <id> <message> # ステアリング
/subagents spawn     # 新しいサブエージェントを起動
```

### 簡易コマンド

```bash
/kill <id>      # サブエージェントを即座に停止
/kill all       # 全サブエージェントを停止
/steer <id> <message>  # 実行中のサブエージェントを誘導
/tell <id> <message>   # エイリアス
```

### ACPエージェント

```bash
/acp spawn      # ACPセッション起動
/acp cancel     # キャンセル
/acp steer      # ステアリング
/acp close      # クローズ
/acp status     # ステータス確認
/acp sessions   # セッション一覧
```

## スキルコマンド

```bash
/skill <name> [input]  # スキルを実行
```

ユーザーが呼び出し可能なスキルは自動的にスラッシュコマンドとして登録されます。スキル名は`a-z0-9_`に変換され、最大32文字です。

## Discord専用コマンド

### スレッドバインディング

```bash
/focus <target>   # スレッドをセッション/サブエージェントにバインド
/unfocus          # バインディングを解除
/agents           # スレッドにバインドされたエージェント一覧
```

### セッション設定

```bash
/session idle <duration|off>     # 非アクティブ時の自動アンフォーカス
/session max-age <duration|off>  # 最大年齢での自動アンフォーカス
```

### ボイスチャンネル

```bash
/vc join     # ボイスチャンネルに参加
/vc leave    # ボイスチャンネルから離脱
/vc status   # ステータス表示
```

※ネイティブコマンドのみ（テキストコマンドでは使用不可）

## プラットフォーム切り替え

```bash
/dock-telegram    # Telegramに切り替え
/dock-discord     # Discordに切り替え
/dock-slack       # Slackに切り替え
# エイリアス: /dock_telegram, /dock_discord, /dock_slack
```

## グループチャット設定

```bash
/activation mention   # メンション時のみ反応
/activation always    # 常に反応
```

## オーナー専用コマンド

### 設定管理

```bash
/config show                          # 全設定を表示
/config show messages.responsePrefix  # 特定の設定を表示
/config get messages.responsePrefix   # 値を取得
/config set messages.responsePrefix="[openclaw]"  # 設定変更
/config unset messages.responsePrefix # 設定削除
```

※`commands.config: true`が必要

### デバッグオーバーライド

```bash
/debug show                           # 現在のオーバーライドを表示
/debug set messages.responsePrefix="[test]"  # オーバーライド設定
/debug unset messages.responsePrefix  # オーバーライド削除
/debug reset                          # 全オーバーライドをクリア
```

※`commands.debug: true`が必要。オーバーライドは再起動でリセットされます。

### 送信制御

```bash
/send on      # 送信を有効化
/send off     # 送信を無効化
/send inherit # 親設定を継承
```

### 使用量表示

```bash
/usage off    # 使用量表示なし
/usage tokens # トークン数のみ
/usage full   # 詳細表示
/usage cost   # コスト概要を表示
```

### 再起動

```bash
/restart      # Gatewayを再起動
```

※デフォルトで有効。`commands.restart: false`で無効化可能

## Bashコマンド（ホストのみ）

```bash
! <command>        # シェルコマンドを実行
/bash <command>    # エイリアス
!poll [sessionId]  # 実行中のコマンドの状態を確認
!stop [sessionId]  # 実行中のコマンドを停止
```

※`commands.bash: true`と`tools.elevated`の許可リストが必要

## 許可リスト管理

```bash
/allowlist                    # 許可リストを表示
/allowlist add <entry>        # エントリを追加
/allowlist remove <entry>     # エントリを削除
```

※`commands.config=true`が必要

## 承認システム

```bash
/approve <id> allow-once    # 一回のみ許可
/approve <id> allow-always  # 常に許可
/approve <id> deny          # 拒否
```

実行承認プロンプトを解決します。

## コンパクション

```bash
/compact              # コンテキストを圧縮
/compact [instructions]  # 指示付きで圧縮
```

詳細は[/concepts/compaction](https://docs.openclaw.ai/concepts/compaction)を参照。

## TTS（テキスト読み上げ）

```bash
/tts off          # TTS無効
/tts always       # 常にTTS
/tts inbound      # 受信時のみ
/tts tagged       # タグ付きのみ
/tts status       # ステータス表示
/tts provider     # プロバイダー設定
/tts limit        # 制限設定
/tts summary      # 要約モード
/tts audio        # オーディオ設定
```

Discordではネイティブコマンドは`/voice`です（Discordが`/tts`を予約しているため）。テキストコマンド`/tts`は動作します。

## インラインショートカット

許可された送信者は、通常のメッセージ内でコマンドを使用できます：

```bash
ねえ /status 今どうなってる？
```

`/status`が実行され、「ねえ 今どうなってる？」が通常のフローで処理されます。

対応コマンド: `/help`、`/commands`、`/status`、`/whoami`（`/id`）

## コマンド構文のバリエーション

コマンドは`:`区切りも受け付けます：

```bash
/think: high
/send: on
/help:
```

## プラットフォーム別の注意点

### Discord
- インタラクティブなピッカー（モデル選択など）
- 動的オートコンプリート
- ボイスチャンネル制御（`/vc`）
- スレッドバインディング対応

### Telegram
- ネイティブコマンド対応
- ボタンメニュー（選択肢がある場合）

### Slack
- ネイティブコマンドは手動設定が必要
- `/status`の代わりに`/agentstatus`（Slackが予約）
- テキストコマンドは通常通り動作

### その他（WhatsApp、Signal、iMessage等）
- テキストコマンドのみ使用可能
- ネイティブコマンドは非対応

## セキュリティ考慮事項

1. **グループチャット**: `/reasoning`と`/verbose`は内部思考を公開する可能性があります
2. **権限**: オーナー専用コマンドは適切に保護されています
3. **承認**: `/elevated`で権限昇格を制御できます
4. **許可リスト**: `commands.allowFrom`でコマンド使用を制限できます

## まとめ

OpenClawのスラッシュコマンドは、AIエージェントを制御するための強力なインターフェースです。基本的な情報取得から、高度なサブエージェント管理、デバッグまで、すべてのコマンドを理解することで、OpenClawを最大限に活用できます。

特に重要なコマンド：
- `/status` - 現在の状態確認
- `/model` - モデル切り替え
- `/think` - 思考モード制御
- `/subagents` - サブエージェント管理
- `/context` - コンテキスト確認

これらを駆使して、効率的なAIエージェント運用を実現してください！

---

**参考リンク**
- [OpenClaw Documentation](https://docs.openclaw.ai)
- [OpenClaw GitHub](https://github.com/openclaw/openclaw)
- [OpenClaw Discord](https://discord.com/invite/clawd)
