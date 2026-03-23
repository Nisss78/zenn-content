---
title: "OpenClawでZenn記事を書いてXに自動投稿する完全ガイド"
emoji: "🤖"
type: "tech"
topics: ["openclaw", "zenn", "x", "自動化", "ai"]
published: false
---

# OpenClawでZenn記事を書いてXに自動投稿する完全ガイド

「技術記事を書きたいけど、時間がかかる...」
「Zennに投稿した後、X（Twitter）にも宣伝したいけど一手間...」

こんな悩みを解決するのが **OpenClaw** です。

この記事では、OpenClawを使って：
- **Zenn記事を自動生成・投稿**
- **X（Twitter）に宣伝投稿**

これらを一気に実現する方法を、初心者向けに**実際のコマンド例**を交えて解説します。

:::message
この記事は実際にOpenClawを使って作成されました。OpenClawに「記事書いて」と頼むだけで、ここまで自動化できます。
:::

## 🎯 この記事でできるようになること

- OpenClawに「Zenn記事書いて」と頼むだけで記事が完成
- GitHub連携でZennに自動投稿
- X APIを使って宣伝投稿も自動化
- 繰り返し使えるワークフローを構築

## 📋 前提条件

始める前に以下を準備してください：

| 項目 | 説明 | 取得方法 |
|------|------|----------|
| **OpenClaw** | AIアシスタント | [公式サイト](https://openclaw.ai)からインストール |
| **Zennアカウント** | 技術ブログプラットフォーム | [zenn.dev](https://zenn.dev)で無料作成 |
| **GitHubアカウント** | Zenn連携用 | [github.com](https://github.com)で無料作成 |
| **X開発者アカウント** | X投稿用API | [developer.twitter.com](https://developer.twitter.com)で申請 |

> 💡 **注意**: Xの開発者アカウントは審査があるため、早めに申請しておくのがおすすめです（通常1〜3日で承認）。

---

## 🚀 Step 1: Zenn環境のセットアップ

### 1-1: Zenn CLIのインストール

まず、Zennの記事を管理するためのCLIツールをインストールします。

```bash
# Node.jsがインストールされていることを確認
node --version  # v18以上推奨

# Zenn CLIをグローバルインストール
npm install -g zenn-cli

# インストール確認
zenn --version
```

### 1-2: GitHubリポジトリの作成

ZennはGitHubリポジトリと連携して記事を管理します。

```bash
# リポジトリ用ディレクトリを作成
mkdir ~/zenn-content
cd ~/zenn-content

# Git初期化
git init

# Zennを初期化
zenn init
```

以下のような構造が作成されます：

```
zenn-content/
├── articles/          # 記事ファイル（Markdown）
│   └── .keep
├── books/             # 本（チェプター形式）
│   └── .keep
├── README.md
└── .gitignore
```

### 1-3: GitHubでリポジトリ作成＆連携

1. [GitHub](https://github.com/new)で新しいリポジトリを作成
   - リポジトリ名: `zenn-content`（任意）
   - Public/Private: どちらでもOK（Public推奨）

2. ローカルリポジトリをプッシュ

```bash
cd ~/zenn-content

# リモートリポジトリを追加
git remote add origin https://github.com/あなたのユーザー名/zenn-content.git

# 初期コミット
git add .
git commit -m "Initial commit: Zenn setup"

# プッシュ
git branch -M main
git push -u origin main
```

### 1-4: ZennとGitHubを連携

1. [Zenn Dashboard](https://zenn.dev/dashboard/setup)にアクセス
2. 「GitHubから連携」をクリック
3. 先ほど作成したリポジトリを選択
4. 連携完了！

これで、GitHubにプッシュするだけでZennに記事が反映されるようになります。

---

## 🤖 Step 2: OpenClawで記事を作成

### 2-1: 記事作成コマンド

OpenClawを起動して、チャットでこう頼むだけ：

```
「TypeScriptの型安全性について、初心者向けにZenn記事を書いて。
サンプルコードを3つ以上含めて。」
```

OpenClawは以下を実行します：

1. 記事の構成を考える
2. Markdownで本文を生成
3. Zennのフロントマター（タイトル、トピックなど）を追加
4. ファイルを保存

### 2-2: 記事のプレビュー

記事が生成されたら、プレビューで確認しましょう。

```bash
cd ~/zenn-content

# プレビューサーバー起動
zenn preview

# 出力例:
# 👀 Preview: http://localhost:8000
```

ブラウザで `http://localhost:8000` を開くと、実際の表示を確認できます。

### 2-3: 記事の編集・修正

プレビューを見て修正したい場合は、OpenClawに追加で指示します：

```
「コードブロックに説明を追加して」
「結論をもっと明確にして」
「画像を追加して」
```

---

## 📤 Step 3: Zennに投稿

### 3-1: 記事を公開

記事を公開するには、フロントマターの `published` を `true` に変更します。

```markdown
---
title: "TypeScriptの型安全性入門"
emoji: "🛡️"
type: "tech"
topics: ["typescript", "初心者向け"]
published: true  # ← これを true に
---
```

### 3-2: GitHubにプッシュ

```bash
cd ~/zenn-content

# 変更をステージング
git add articles/

# コミット
git commit -m "Add: TypeScriptの型安全性入門"

# プッシュ（自動的にZennに反映）
git push
```

プッシュ後、数秒〜数分でZennに記事が表示されます。

### 3-3: 記事URLの確認

記事のURLは以下の形式になります：

```
https://zenn.dev/あなたのユーザー名/articles/スラッグ
```

スラッグは記事ファイル名から拡張子を除いたものです。

例：`articles/typescript-type-safety.md` → 
`https://zenn.dev/nisss/articles/typescript-type-safety`

---

## 🐦 Step 4: X（Twitter）に宣伝投稿

### 4-1: X APIの取得

Xへの投稿にはAPIキーが必要です。

1. [X Developer Portal](https://developer.twitter.com/)にアクセス
2. プロジェクトを作成
3. Appを作成し、以下のキーを取得：
   - API Key（Consumer Key）
   - API Secret（Consumer Secret）
   - Access Token
   - Access Token Secret

> ⚠️ **注意**: Free tierは月1,500件投稿まで。個人利用なら十分です。

### 4-2: OpenClawの設定

X APIの情報をOpenClawに設定します。環境変数に追加するか、OpenClawの設定ファイルに記述します。

```bash
# ~/.bashrc または ~/.zshrc に追加
export X_API_KEY="あなたのAPIキー"
export X_API_SECRET="あなたのAPIシークレット"
export X_ACCESS_TOKEN="あなたのアクセストークン"
export X_ACCESS_TOKEN_SECRET="あなたのアクセストークンシークレット"
```

### 4-3: 投稿実行

OpenClawにこう頼むだけ：

```
「Xに記事の宣伝投稿して。
URLは https://zenn.dev/nisss/articles/typescript-type-safety
ハッシュタグも付けて。」
```

OpenClawが自動的に：
1. キャッチーな投稿文を作成
2. APIを使ってXに投稿
3. 投稿URLを返す

---

## 🔄 Step 5: ワークフローの自動化

### 5-1: 一連の流れをスクリプト化

以下のようなシェルスクリプトを作成すると、コマンド一発で全自動化できます。

```bash
#!/bin/bash
# ~/scripts/publish-article.sh

# 記事ファイルのパス
ARTICLE_PATH=$1

# 公開設定に変更
sed -i 's/published: false/published: true/' "$ARTICLE_PATH"

# Zennに投稿
cd ~/zenn-content
git add "$ARTICLE_PATH"
git commit -m "Publish article"
git push

# Xに投稿（OpenClaw経由）
ARTICLE_URL="https://zenn.dev/nisss/articles/$(basename "$ARTICLE_PATH" .md)"
echo "Xに投稿: $ARTICLE_URL"

# 投稿完了通知
echo "✅ 記事を公開しました: $ARTICLE_URL"
```

使い方：

```bash
chmod +x ~/scripts/publish-article.sh
~/scripts/publish-article.sh ~/zenn-content/articles/my-article.md
```

### 5-2: OpenClawのheartbeatで定期実行

OpenClawには「heartbeat」という定期チェック機能があります。これを使うと：
- トレンドをチェックして記事ネタを収集
- ニュースを自動要約
- 定期的な投稿を自動化

詳しくは [OpenClaw ドキュメント](https://docs.openclaw.ai)を参照。

---

## ⚠️ 注意点とトラブルシューティング

### よくあるエラーと解決策

| エラー | 原因 | 解決策 |
|--------|------|--------|
| `zenn: command not found` | CLIがインストールされていない | `npm install -g zenn-cli` |
| `Git remote not found` | リモートリポジトリ未設定 | `git remote add origin <URL>` |
| `Authentication failed` | X APIキーが間違っている | キーを再生成して設定し直す |
| 記事が反映されない | ZennとGitHubが未連携 | Dashboardで連携設定 |

### 記事の品質を保つコツ

1. **必ずプレビューで確認** - 自動生成でもミスはある
2. **コードブロックを活用** - 読みやすさが段違い
3. **画像を追加** - 説明画像があると理解度が上がる
4. **結論を明確に** - 最後に「まとめ」セクションを入れる

### X投稿のベストプラクティス

良い投稿例：

```
🔔 新着記事公開！

「TypeScriptの型安全性入門 - 初心者がつまずきやすい5つのポイント」

型エラーに悩む初心者向けに、よくあるミスと対策を解説しました！

https://zenn.dev/nisss/articles/typescript-type-safety

#TypeScript #プログラミング学習
```

悪い投稿例：

```
記事書きました。見てね。
```

**ポイント:**
- 絵文字で目を引く
- 記事のタイトルを入れる
- 読者へのメリットを一言で
- 関連ハッシュタグを2〜3個

---

## 🎉 まとめ

この記事では、OpenClawを使って：
- ✅ Zenn記事を自動生成・投稿
- ✅ Xに宣伝投稿
- ✅ ワークフローを自動化

これらを実現する方法を解説しました。

最初のセットアップは少し手間ですが、一度構築すれば「記事書いて」と頼むだけで全自動。コンテンツ作成の時間を大幅に短縮できます。

あなたもOpenClawで、効率的な技術発信を始めてみませんか？

---

## 📚 参考リンク

- [OpenClaw 公式ドキュメント](https://docs.openclaw.ai)
- [OpenClaw GitHub](https://github.com/openclaw/openclaw)
- [Zenn 公式ドキュメント](https://zenn.dev/zenn/articles/what-is-zenn)
- [Zenn CLI ガイド](https://zenn.dev/zenn/articles/zenn-cli-guide)
- [X API ドキュメント](https://developer.twitter.com/en/docs)

---

**筆者:** OpenClaw愛用中のエンジニア。「自動化が趣味」と言いながら、実は手動で書いている部分もある（笑）
