---
title: "OpenClawのおすすめスキル34選：AIエージェントを強化する必須ツール"
emoji: "🧩"
type: "tech"
topics: ["openclaw", "ai", "productivity", "automation"]
published: true
---

# OpenClawのおすすめスキル34選

OpenClawをインストールしただけでは、AIエージェントは基本的な機能しか持っていません。本当の力を発揮するには、**スキル**を追加する必要があります。

OpenClawで使える34の公式スキルをカテゴリ別に整理し、おすすめ度とともに徹底解説します。

## スキルとは

スキルは、OpenClawのAIエージェントに新しい能力を与えるアドオンです。例えば：

- 📧 メールを送受信する
- 🎵 音楽を再生する
- 📝 メモを取る
- 🔍 Web検索する
- 💡 スマートホームを操作する

これらを組み合わせることで、あなた専用のAIアシスタントを作れます。

---

## 🌟 トップおすすめ（最初に入れるべき5選）

### 1. 🔊 sag - 音声読み上げ

**おすすめ度：⭐⭐⭐⭐⭐**

テキストを自然な音声で読み上げます。ElevenLabs APIを使用。

**用途例：**
- ニュース記事を読み聞かせ
- 物語をナレーション
- リマインダーの音声通知

**必要なもの：**
- ElevenLabs API Key

```bash
# インストール
clawhub install sag
```

---

### 2. 📧 himalaya - メール管理

**おすすめ度：⭐⭐⭐⭐⭐**

ターミナルからメールを送受信。Gmail、Outlook対応。

**用途例：**
- 重要メールの通知
- 定型文の自動返信
- メール要約

**必要なもの：**
- メールアカウント（IMAP/SMTP設定）

```bash
clawhub install himalaya
```

---

### 3. 🧾 summarize - テキスト要約

**おすすめ度：⭐⭐⭐⭐⭐**

長文を短く要約。URLからWebページを要約することも可能。

**用途例：**
- 長い記事の要点把握
- 会議議事録の要約
- PDF文書の要約

```bash
clawhub install summarize
```

---

### 4. 📦 mcporter - MCP サーバー管理

**おすすめ度：⭐⭐⭐⭐⭐**

MCP（Model Context Protocol）サーバーを簡単に管理。外部APIやツールと連携。

**用途例：**
- Notion連携
- Slack連携
- カスタムAPI統合

```bash
clawhub install mcporter
```

---

### 5. 🧩 clawhub - スキル管理

**おすすめ度：⭐⭐⭐⭐⭐**

ClawHubから新しいスキルを検索・インストール。スキルのアップデートも管理。

**用途例：**
- コミュニティスキルの探索
- スキルのバージョン管理
- 自作スキルの公開

```bash
clawhub install clawhub
```

---

## 📝 ノート・タスク管理

### 🍎 apple-notes

**おすすめ度：⭐⭐⭐⭐**

Apple純正のメモアプリと連携。

```bash
clawhub install apple-notes
```

**用途：**
- アイデアメモの作成
- 買い物リスト管理
- プロジェクトノート

---

### ⏰ apple-reminders

**おすすめ度：⭐⭐⭐⭐**

Apple純正のリマインダーアプリと連携。

```bash
clawhub install apple-reminders
```

**用途：**
- タスク追加
- 期限付きリマインダー
- 買い物リスト

---

### 🐻 bear-notes

**おすすめ度：⭐⭐⭐**

Bear Notes アプリと連携。Markdownメモアプリ。

```bash
clawhub install bear-notes
```

---

### 💎 obsidian

**おすすめ度：⭐⭐⭐⭐**

Obsidian と連携。知識管理・Zettelkasten向け。

```bash
clawhub install obsidian
```

**用途：**
- ナレッジベース管理
- リンク付きノート作成
- デイリーノート

---

### ✅ things-mac

**おすすめ度：⭐⭐⭐⭐**

Things 3（タスク管理アプリ）と連携。

```bash
clawhub install things-mac
```

**用途：**
- タスクの追加・完了
- プロジェクト管理
- 今日やることの確認

---

## 🔊 音声・メディア

### 🎤 openai-whisper

**おすすめ度：⭐⭐⭐⭐**

音声をテキストに変換（文字起こし）。OpenAI Whisper使用。

```bash
clawhub install openai-whisper
```

**用途：**
- 会議の文字起こし
- ポッドキャストのテキスト化
- 音声メモの記録

**必要なもの：**
- OpenAI API Key

---

### 🎬 video-frames

**おすすめ度：⭐⭐⭐**

動画からフレームを抽出。

```bash
clawhub install video-frames
```

**用途：**
- 動画のサムネイル作成
- 特定シーンの抽出
- 動画解析

---

### 🌊 songsee

**おすすめ度：⭐⭐⭐**

音楽の波形表示・解析。

```bash
clawhub install songsee
```

---

### 🔊 sonoscli

**おすすめ度：⭐⭐⭐**

Sonos スマートスピーカーを操作。

```bash
clawhub install sonoscli
```

**用途：**
- 音楽再生・停止
- ボリューム調整
- 複数ルームの同期

---

### 📸 camsnap

**おすすめ度：⭐⭐⭐**

Webカメラで写真撮影。

```bash
clawhub install camsnap
```

**用途：**
- セキュリティ監視
- タイムラプス作成
- 画像認識の入力

---

## 💬 コミュニケーション

### 📨 imsg

**おすすめ度：⭐⭐⭐⭐**

iMessage でメッセージ送信。

```bash
clawhub install imsg
```

**用途：**
- 緊急連絡の自動送信
- 定期通知
- 家族へのメッセージ

---

### 📱 wacli

**おすすめ度：⭐⭐⭐**

WhatsApp と連携。

```bash
clawhub install wacli
```

---

## 🏠 生活・IoT

### 💡 openhue

**おすすめ度：⭐⭐⭐⭐**

Philips Hue スマート照明を操作。

```bash
clawhub install openhue
```

**用途：**
- 照明のオン/オフ
- 明るさ・色の調整
- シーン設定

**必要なもの：**
- Philips Hue Bridge

---

### 📍 goplaces

**おすすめ度：⭐⭐⭐**

位置情報・地図検索。

```bash
clawhub install goplaces
```

**用途：**
- 近くの店を検索
- 移動経路の提案
- 現在地の共有

---

### 🛵 ordercli

**おすすめ度：⭐⭐**

フードデリバリー注文（地域限定）。

```bash
clawhub install ordercli
```

---

### 🛌 eightctl

**おすすめ度：⭐⭐⭐**

睡眠トラッカー「Eight Sleep」と連携。

```bash
clawhub install eightctl
```

---

## 🛠 開発・ツール

### 🧵 tmux

**おすすめ度：⭐⭐⭐⭐**

tmuxセッションをリモート操作。

```bash
clawhub install tmux
```

**用途：**
- ターミナルセッション管理
- 長時間実行タスクの監視
- リモート開発

---

### 📄 nano-pdf

**おすすめ度：⭐⭐⭐**

PDF操作（読み込み・テキスト抽出）。

```bash
clawhub install nano-pdf
```

**用途：**
- PDFからのテキスト抽出
- 書類の解析
- レポート生成

---

### 🧲 gifgrep

**おすすめ度：⭐⭐⭐**

GIF画像を検索。

```bash
clawhub install gifgrep
```

**用途：**
- チャット用GIF検索
- プレゼンテーション素材

---

## 🌐 サービス連携

### ✨ gemini

**おすすめ度：⭐⭐⭐⭐**

Google Gemini AI と連携。

```bash
clawhub install gemini
```

**用途：**
- 高精度な画像認識
- 長文処理
- マルチモーダルタスク

**必要なもの：**
- Google AI API Key

---

### 🐦 xurl

**おすすめ度：⭐⭐⭐**

X(Twitter) のURLを展開・解析。

```bash
clawhub install xurl
```

---

### 🫐 blucli

**おすすめ度：⭐⭐⭐**

Bluetooth機器の管理。

```bash
clawhub install blucli
```

**用途：**
- デバイスのペアリング
- 接続状態の確認

---

### 🎮 gog

**おすすめ度：⭐⭐**

GOG.com（ゲームストア）と連携。

```bash
clawhub install gog
```

---

## 🔍 情報・分析

### 🧿 oracle

**おすすめ度：⭐⭐⭐**

予測・意思決定支援。

```bash
clawhub install oracle
```

---

### 👀 peekaboo

**おすすめ度：⭐⭐⭐**

画面監視・変更検知。

```bash
clawhub install peekaboo
```

**用途：**
- Webサイトの更新検知
- 価格変動の通知

---

### 📜 session-logs

**おすすめ度：⭐⭐⭐**

セッション履歴の記録・分析。

```bash
clawhub install session-logs
```

---

### 📊 model-usage

**おすすめ度：⭐⭐⭐⭐**

AIモデルの使用量・コスト追跡。

```bash
clawhub install model-usage
```

**用途：**
- API使用量の確認
- コスト管理
- 予算アラート

---

### 📰 blogwatcher

**おすすめ度：⭐⭐⭐**

ブログの更新監視。

```bash
clawhub install blogwatcher
```

**用途：**
- お気に入りブログの更新通知
- 情報収集の自動化

---

## 🔐 セキュリティ

### 🔐 1password

**おすすめ度：⭐⭐⭐⭐**

1Password と連携。パスワード管理。

```bash
clawhub install 1password
```

**用途：**
- パスワードの取得
- 秘密情報の安全な管理
- ログイン自動化

---

## スキルのインストール方法

### 方法1: 対話形式

```bash
openclaw setup
```

矢印キーでスキルを選択し、スペースでチェック、Enterで確定。

### 方法2: ClawHubから

```bash
# スキルを検索
clawhub search <keyword>

# インストール
clawhub install <skill-name>
```

### 方法3: 手動インストール

スキルフォルダを `~/.openclaw/skills/` に配置。

---

## まとめ

### 初心者におすすめの組み合わせ

```
✅ summarize      # 要約
✅ himalaya       # メール
✅ apple-reminders # タスク
✅ sag            # 音声
✅ mcporter       # 連携
```

### パワーユーザーにおすすめ

```
✅ tmux           # 開発
✅ obsidian       # 知識管理
✅ openhue        # スマートホーム
✅ gemini         # 高性能AI
✅ model-usage    # コスト管理
```

### クリエイターにおすすめ

```
✅ openai-whisper # 文字起こし
✅ video-frames   # 動画処理
✅ obsidian       # アイデア管理
✅ summarize      # リサーチ
✅ sag            # ナレーション
```

---

スキルは組み合わせることで、あなた専用のAIアシスタントに進化します。まずはおすすめの5つから始めて、徐々に機能を拡張していきましょう！

**参考リンク**
- [OpenClaw公式ドキュメント](https://docs.openclaw.ai)
- [ClawHub - スキルマーケットプレイス](https://clawhub.com)
- [OpenClaw GitHub](https://github.com/openclaw/openclaw)
- [OpenClaw Discord](https://discord.com/invite/clawd)
