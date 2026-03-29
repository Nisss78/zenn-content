---
title: "OpenClawのおすすめスキル34選：AIエージェントを強化する必須ツール"
emoji: "🧩"
type: "tech"
topics: ["openclaw", "ai", "productivity", "automation"]
published: true
---

# OpenClawのおすすめスキル34選

OpenClawをインストールしただけでは、AIエージェントは基本的な機能しか持っていません。本当の力を発揮するには、**スキル**を追加する必要があります。

この記事では、OpenClawで使える34の公式スキルをカテゴリ別に整理し、おすすめ度とともに徹底解説します。

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

**必要なもの：** ElevenLabs API Key

```bash
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

```bash
clawhub install mcporter
```

---

### 5. 🧩 clawhub - スキル管理

**おすすめ度：⭐⭐⭐⭐⭐**

ClawHubから新しいスキルを検索・インストール。

```bash
clawhub install clawhub
```

---

## 📝 ノート・タスク管理

### 🍎 apple-notes
Apple純正のメモアプリと連携。

```bash
clawhub install apple-notes
```

### ⏰ apple-reminders
Apple純正のリマインダーアプリと連携。

```bash
clawhub install apple-reminders
```

### 🐻 bear-notes
Bear Notes アプリと連携。

```bash
clawhub install bear-notes
```

### 💎 obsidian
Obsidian と連携。知識管理・Zettelkasten向け。

```bash
clawhub install obsidian
```

### ✅ things-mac
Things 3（タスク管理アプリ）と連携。

```bash
clawhub install things-mac
```

---

## 🔊 音声・メディア

### 🎤 openai-whisper
音声をテキストに変換（文字起こし）。

```bash
clawhub install openai-whisper
```

### 🎬 video-frames
動画からフレームを抽出。

```bash
clawhub install video-frames
```

### 🌊 songsee
音楽の波形表示・解析。

```bash
clawhub install songsee
```

### 🔊 sonoscli
Sonos スマートスピーカーを操作。

```bash
clawhub install sonoscli
```

### 📸 camsnap
Webカメラで写真撮影。

```bash
clawhub install camsnap
```

---

## 💬 コミュニケーション

### 📨 imsg
iMessage でメッセージ送信。

```bash
clawhub install imsg
```

### 📱 wacli
WhatsApp と連携。

```bash
clawhub install wacli
```

---

## 🏠 生活・IoT

### 💡 openhue
Philips Hue スマート照明を操作。

```bash
clawhub install openhue
```

### 📍 goplaces
位置情報・地図検索。

```bash
clawhub install goplaces
```

### 🛵 ordercli
フードデリバリー注文（地域限定）。

```bash
clawhub install ordercli
```

### 🛌 eightctl
睡眠トラッカー「Eight Sleep」と連携。

```bash
clawhub install eightctl
```

---

## 🛠 開発・ツール

### 🧵 tmux
tmuxセッションをリモート操作。

```bash
clawhub install tmux
```

### 📄 nano-pdf
PDF操作（読み込み・テキスト抽出）。

```bash
clawhub install nano-pdf
```

### 🧲 gifgrep
GIF画像を検索。

```bash
clawhub install gifgrep
```

---

## 🌐 サービス連携

### ✨ gemini
Google Gemini AI と連携。

```bash
clawhub install gemini
```

### 🐦 xurl
X(Twitter) のURLを展開・解析。

```bash
clawhub install xurl
```

### 🫐 blucli
Bluetooth機器の管理。

```bash
clawhub install blucli
```

### 🎮 gog
GOG.com（ゲームストア）と連携。

```bash
clawhub install gog
```

---

## 🔍 情報・分析

### 🧿 oracle
予測・意思決定支援。

```bash
clawhub install oracle
```

### 👀 peekaboo
画面監視・変更検知。

```bash
clawhub install peekaboo
```

### 📜 session-logs
セッション履歴の記録・分析。

```bash
clawhub install session-logs
```

### 📊 model-usage
AIモデルの使用量・コスト追跡。

```bash
clawhub install model-usage
```

### 📰 blogwatcher
ブログの更新監視。

```bash
clawhub install blogwatcher
```

---

## 🔐 セキュリティ

### 🔐 1password
1Password と連携。パスワード管理。

```bash
clawhub install 1password
```

---

## スキルのインストール方法

### 方法1: 対話形式

```bash
openclaw setup
```

### 方法2: ClawHubから

```bash
clawhub search <keyword>
clawhub install <skill-name>
```

### 方法3: 手動インストール

スキルフォルダを `~/.openclaw/skills/` に配置。

---

## まとめ

### 初心者におすすめ

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
