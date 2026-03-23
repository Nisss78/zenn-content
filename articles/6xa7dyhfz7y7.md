---
title: "テック系略語・Numeronym（ニューメロニム）完全辞典"
emoji: "📝"
type: "tech"
topics: []
published: false
---

---
title: "テック系略語・Numeronym（ニューメロニム）完全辞典"
emoji: "🔤"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["abbreviations", "vocabulary", "beginner"]
published: false
---



エンジニア界隈では `i18n` や `k8s` のような略語が飛び交います。これらは **Numeronym（ニューメロニム）** と呼ばれ、最初と最後の文字を残して間の文字数を数字で置き換えたものです。

この記事では、よく使われるテック系略語を体系的に整理して解説します。

---

## 🔢 Numeronym（数字を使った略語）

### ソフトウェア・ライブラリ

| 略語 | 元の言葉 | 文字数 | 解説 |
|------|----------|--------|------|
| **i18n** | internationalization | 18 | 国際化。多言語対応のこと |
| **l10n** | localization | 10 | 地域化。特定地域への適応 |
| **k8s** | Kubernetes | 8 | コンテナオーケストレーションプラットフォーム |
| **a11y** | accessibility | 11 | アクセシビリティ。障害者への配慮 |
| **o11y** | observability | 11 | オブザーバビリティ。システムの可観測性 |
| **c10k** | 10000 connections | - | 1万同時接続問題 |
| **c10m** | 10 million connections | - | 1000万同時接続問題 |

### インフラ・ネットワーク

| 略語 | 元の言葉 | 文字数 | 解説 |
|------|----------|--------|------|
| **nginx** | engine x | - | Webサーバー・リバースプロキシ |
| **sendmail** | send mail | - | メール転送エージェント（実はNumeronymではないが誤解されがち） |

### プログラミング言語・概念

| 略語 | 元の言葉 | 文字数 | 解説 |
|------|----------|--------|------|
| **w3c** | World Wide Web Consortium | - | Web標準化団体 |
| **x11** | X Window System version 11 | - | UNIX系のウィンドウシステム |

### データベース

| 略語 | 元の言葉 | 文字数 | 解説 |
|------|----------|--------|------|
| **p99** | 99th percentile | - | 99パーセンタイル。レイテンシ指標 |

---

## 🌐 Web・ネットワーク略語

### プロトコル

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **HTTP** | HyperText Transfer Protocol | Webページの通信プロトコル |
| **HTTPS** | HTTP Secure | 暗号化されたHTTP |
| **FTP** | File Transfer Protocol | ファイル転送プロトコル |
| **SSH** | Secure Shell | 暗号化リモートログイン |
| **TCP** | Transmission Control Protocol | 信頼性のある通信プロトコル |
| **UDP** | User Datagram Protocol | 高速だが信頼性の低いプロトコル |
| **IP** | Internet Protocol | インターネットアドレス指定 |
| **DNS** | Domain Name System | ドメイン名をIPアドレスに変換 |
| **SMTP** | Simple Mail Transfer Protocol | メール送信プロトコル |
| **POP3** | Post Office Protocol version 3 | メール受信プロトコル |
| **IMAP** | Internet Message Access Protocol | メール受信プロトコル（サーバー保存型） |
| **WebSocket** | - | 双方向リアルタイム通信 |
| **gRPC** | Google Remote Procedure Call | 高性能RPCフレームワーク |
| **REST** | Representational State Transfer | Web API設計原則 |
| **GraphQL** | - | Facebook製クエリ言語 |

### Web技術

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **HTML** | HyperText Markup Language | Webページの構造言語 |
| **CSS** | Cascading Style Sheets | スタイルシート言語 |
| **JS** | JavaScript | Webスクリプト言語 |
| **TS** | TypeScript | 型付きJavaScript |
| **DOM** | Document Object Model | HTML/XMLの構造モデル |
| **AJAX** | Asynchronous JavaScript And XML | 非同期通信技術 |
| **SPA** | Single Page Application | 単一ページアプリ |
| **SSR** | Server-Side Rendering | サーバーサイドレンダリング |
| **CSR** | Client-Side Rendering | クライアントサイドレンダリング |
| **SEO** | Search Engine Optimization | 検索エンジン最適化 |
| **CDN** | Content Delivery Network | コンテンツ配信ネットワーク |

---

## 💾 データ形式

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **JSON** | JavaScript Object Notation | 軽量データ記述言語 |
| **XML** | Extensible Markup Language | マークアップ言語 |
| **YAML** | YAML Ain't Markup Language | 設定ファイル形式 |
| **CSV** | Comma-Separated Values | カンマ区切りデータ |
| **TOML** | Tom's Obvious Minimal Language | 設定ファイル形式 |
| **Protobuf** | Protocol Buffers | Google製シリアライズ形式 |

---

## 🔐 セキュリティ

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **SSL** | Secure Sockets Layer | 暗号化プロトコル（現在はTLS） |
| **TLS** | Transport Layer Security | SSLの後継暗号化プロトコル |
| **JWT** | JSON Web Token | 認証トークン形式 |
| **OAuth** | Open Authorization | 認可フレームワーク |
| **OIDC** | OpenID Connect | 認証プロトコル |
| **2FA** | Two-Factor Authentication | 二要素認証 |
| **MFA** | Multi-Factor Authentication | 多要素認証 |
| **CORS** | Cross-Origin Resource Sharing | クロスオリジン通信許可 |
| **XSS** | Cross-Site Scripting | クロスサイトスクリプティング攻撃 |
| **CSRF** | Cross-Site Request Forgery | クロスサイトリクエストフォージェリ |
| **SQLi** | SQL Injection | SQLインジェクション攻撃 |
| **DDoS** | Distributed Denial of Service | 分散型サービス拒否攻撃 |
| **MITM** | Man-In-The-Middle | 中間者攻撃 |
| **PKI** | Public Key Infrastructure | 公開鍵基盤 |
| **HSM** | Hardware Security Module | ハードウェアセキュリティモジュール |

---

## ☁️ クラウド・インフラ

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **AWS** | Amazon Web Services | Amazonのクラウドサービス |
| **GCP** | Google Cloud Platform | Googleのクラウドサービス |
| **IaaS** | Infrastructure as a Service | インフラサービス |
| **PaaS** | Platform as a Service | プラットフォームサービス |
| **SaaS** | Software as a Service | ソフトウェアサービス |
| **FaaS** | Function as a Service | サーバーレス関数サービス |
| **VM** | Virtual Machine | 仮想マシン |
| **VPS** | Virtual Private Server | 仮想専用サーバー |
| **CI/CD** | Continuous Integration/Deployment | 継続的インテグレーション/デプロイ |
| **IaC** | Infrastructure as Code | コードによるインフラ管理 |

---

## 🐳 コンテナ・DevOps

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **OCI** | Open Container Initiative | コンテナ標準化団体 |
| **CRI** | Container Runtime Interface | コンテナランタイムIF |
| **CNI** | Container Network Interface | コンテナネットワークIF |
| **CSI** | Container Storage Interface | コンテナストレージIF |
| **Helm** | - | Kubernetesパッケージマネージャー |
| **ArgoCD** | - | GitOpsツール |

---

## 🧠 AI・機械学習

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **AI** | Artificial Intelligence | 人工知能 |
| **ML** | Machine Learning | 機械学習 |
| **DL** | Deep Learning | ディープラーニング |
| **NLP** | Natural Language Processing | 自然言語処理 |
| **CV** | Computer Vision | コンピュータビジョン |
| **GAN** | Generative Adversarial Network | 敵対的生成ネットワーク |
| **LLM** | Large Language Model | 大規模言語モデル |
| **RAG** | Retrieval-Augmented Generation | 検索拡張生成 |
| **RLHF** | Reinforcement Learning from Human Feedback | 人間のフィードバックによる強化学習 |
| **GPT** | Generative Pre-trained Transformer | OpenAIのLLM |
| **BERT** | Bidirectional Encoder Representations from Transformers | Googleの言語モデル |
| **YOLO** | You Only Look Once | 物体検出アルゴリズム |

---

## 🗄️ データベース

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **DB** | Database | データベース |
| **RDBMS** | Relational Database Management System | 関係データベース |
| **SQL** | Structured Query Language | データベースクエリ言語 |
| **NoSQL** | Not Only SQL | 非関係データベース |
| **ACID** | Atomicity, Consistency, Isolation, Durability | トランザクション特性 |
| **CRUD** | Create, Read, Update, Delete | 基本的な4操作 |
| **ORM** | Object-Relational Mapping | オブジェクト関係マッピング |

---

## 🧪 テスト・品質

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **TDD** | Test-Driven Development | テスト駆動開発 |
| **BDD** | Behavior-Driven Development | 振舞駆動開発 |
| **E2E** | End-to-End | 結合テスト・総合テスト |
| **UT** | Unit Test | 単体テスト |
| **IT** | Integration Test | 結合テスト |
| **QA** | Quality Assurance | 品質保証 |

---

## 📐 設計・アーキテクチャ

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **API** | Application Programming Interface | アプリケーションIF |
| **SDK** | Software Development Kit | 開発キット |
| **MVC** | Model-View-Controller | 設計パターン |
| **MVVM** | Model-View-ViewModel | 設計パターン |
| **DDD** | Domain-Driven Design | ドメイン駆動設計 |
| **SOA** | Service-Oriented Architecture | サービス指向アーキテクチャ |
| **CQRS** | Command Query Responsibility Segregation | コマンドクエリ責任分離 |
| **DIP** | Dependency Inversion Principle | 依存性逆転の原則 |
| **SOLID** | SRP, OCP, LSP, ISP, DIP | 5つの設計原則 |
| **YAGNI** | You Ain't Gonna Need It | 必要以上の実装を避ける原則 |
| **DRY** | Don't Repeat Yourself | 重複を避ける原則 |
| **KISS** | Keep It Simple, Stupid | シンプルに保つ原則 |

---

## 🔧 開発ツール

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **IDE** | Integrated Development Environment | 統合開発環境 |
| **VCS** | Version Control System | バージョン管理システム |
| **PR** | Pull Request | プルリクエスト |
| **MR** | Merge Request | マージリクエスト（GitLab） |
| **CI** | Continuous Integration | 継続的インテグレーション |
| **CD** | Continuous Delivery/Deployment | 継続的デリバリー/デプロイ |

---

## 📱 モバイル

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **APK** | Android Package | Androidアプリファイル |
| **IPA** | iOS App Store Package | iOSアプリファイル |
| **PWA** | Progressive Web App | ネイティブライクなWebアプリ |
| **SDK** | Software Development Kit | 開発キット |

---

## 🏢 ビジネス・プロセス

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **MVP** | Minimum Viable Product | 最小実用製品 |
| **POC** | Proof of Concept | 概念実証 |
| **KPI** | Key Performance Indicator | 重要業績評価指標 |
| **OKR** | Objectives and Key Results | 目標と主要成果 |
| **SLA** | Service Level Agreement | サービス品質保証 |
| **ROI** | Return on Investment | 投資収益率 |

---

## 🎮 その他よく使われる略語

| 略語 | 完全形 | 解説 |
|------|--------|------|
| **OTOH** | On The Other Hand | 一方で |
| **AFAIK** | As Far As I Know | 私の知る限り |
| **IMO** | In My Opinion | 私の意見では |
| **TL;DR** | Too Long; Didn't Read | 長すぎて読まない（要約） |
| **FYI** | For Your Information | 参考までに |
| **WIP** | Work In Progress | 作業中 |
| **LGTM** | Looks Good To Me | よさそうに見える（レビュー承認） |
| **PTAL** | Please Take A Look | 見てください |
| **RFC** | Request For Comments | コメント募集 |
| **AKA** | Also Known As | またの名を |

---

## 📚 まとめ

エンジニアリングで使われる略語は非常に多く、これらを理解することでドキュメントや会話の理解が深まります。

特によく見る Numeronym は以下のパターンで作られています：

```
最初の文字 + 間の文字数 + 最後の文字
```

例：
- `internationalization` → `i` + `18文字` + `n` → **i18n**
- `Kubernetes` → `K` + `8文字` + `s` → **k8s**

このパターンを知っていれば、初見の略語でも推測しやすくなります！

---

間違いや追加すべき略語があればコメントで教えてください！

---

#tech #abbreviations #vocabulary #beginner #dictionary
