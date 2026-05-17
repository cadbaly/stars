# cadbaly's GitHub Stars

cadbalyがスターしたリポジトリを用途別にカテゴリ分けしたリンク集です。

---

## 目次

- [Claude Code リソース](#claude-code-リソース)
- [LLM / AI ツール](#llm--ai-ツール)
- [AI エージェント / スキル](#ai-エージェント--スキル)
- [スペック駆動開発](#スペック駆動開発)
- [セキュリティ / ネットワーク](#セキュリティ--ネットワーク)
- [ネットワーク / OS](#ネットワーク--os)
- [インフラ / IaC](#インフラ--iac)
- [開発環境 / ツール](#開発環境--ツール)
- [フォント](#フォント)
- [エミュレーター](#エミュレーター)

---

## Claude Code リソース

Claude Code（Anthropic の CLI エージェント）の活用に特化したリポジトリ群。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [anthropics/claude-code](https://github.com/anthropics/claude-code) | Claude Code 本体。ターミナルで動くエージェント型コーディングツール。コードベースを理解し、自然言語からタスク実行・コード解説・git ワークフローまでをこなす | Shell |
| [anthropics/claude-code-action](https://github.com/anthropics/claude-code-action) | GitHub Actions と Claude Code を統合する公式アクション。PR やイシューに AI レビュー・コード生成を組み込める | TypeScript |
| [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official) | Anthropic 公式が管理する高品質な Claude Code プラグイン（MCP・Skills）のディレクトリ | Python |
| [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | Claude Code に関するスキル・フック・スラッシュコマンド・エージェント等のキュレーション Awesome リスト | Python |
| [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) | Claude Code の設定・監視を行う CLI ツール。テンプレート管理に便利 | Python |
| [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) | Claude Code / Codex / Cursor 向けのエージェントハーネス最適化システム（スキル・記憶・セキュリティ） | JavaScript |
| [gastownhall/beads](https://github.com/gastownhall/beads) | コーディングエージェントの「メモリ拡張」ツール。Claude Code などに長期記憶を付与する | Go |
| [nilbuild/claude-statusline](https://github.com/nilbuild/claude-statusline) | Claude Code 用のシンプルなステータスライン設定。ターミナルに進捗を表示 | Shell |
| [GenerativeAgents/claude-code-book-chapter8](https://github.com/GenerativeAgents/claude-code-book-chapter8) | Claude Code 解説書の第8章サンプルコード | TypeScript |
| [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) | Andrej Karpathy の LLM コーディング観察に基づく CLAUDE.md 一枚。Claude Code の挙動を改善 | — |
| [Alishahryar1/free-claude-code](https://github.com/Alishahryar1/free-claude-code) | Claude Code を無料で使うための代替実装。ターミナル・VSCode 拡張・Discord 経由で利用でき、音声入力にも対応 | Python |

---

## LLM / AI ツール

大規模言語モデルの活用・統合・最適化に関するツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [BerriAI/litellm](https://github.com/BerriAI/litellm) | 100 以上の LLM API を OpenAI 形式で呼び出せる SDK／プロキシ（AI Gateway）。コスト追跡・ガードレール・ロードバランシング対応 | Python |
| [mlflow/mlflow](https://github.com/mlflow/mlflow) | エージェント／LLM／ML モデルのデバッグ・評価・監視・最適化を行う OSS の AI エンジニアリング基盤。LLMOps・MLOps を統合管理 | Python |
| [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp) | C/C++ 製の高速 LLM 推論エンジン。CPU・GPU・各種ハードウェアでローカル推論を実現するデファクト | C++ |
| [rtk-ai/rtk](https://github.com/rtk-ai/rtk) | LLM のトークン消費を 60〜90% 削減する CLI プロキシ。Rust 単一バイナリで依存ゼロ | Rust |
| [microsoft/markitdown](https://github.com/microsoft/markitdown) | PDF・Word・Excel などのファイルを Markdown に変換する Python ツール。RAG のデータ準備に活用できる | Python |

---

## AI エージェント / スキル

汎用 AI エージェントや、Claude Code・openclaw など複数プラットフォーム対応のエージェント／スキル。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [OpenHands/OpenHands](https://github.com/OpenHands/OpenHands) | AI 駆動の開発を実現するエージェントプラットフォーム。ブラウジング・コマンド実行・コード編集を自律的にこなす 🙌 | Python |
| [openclaw/openclaw](https://github.com/openclaw/openclaw) | 任意 OS／プラットフォームで動作する個人向け AI アシスタント。データ主権を重視 🦞 | TypeScript |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | Claude / Codex / OpenAI など複数バックエンドに対応する成長型エージェント | Python |
| [dahatake/skills](https://github.com/dahatake/skills) | エージェントプラグインとして提供される skills 集 | Python |
| [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) | Reddit・X・YouTube・HN・Polymarket・Web を横断調査して根拠付きで要約する AI エージェントスキル | Python |

---

## スペック駆動開発

仕様書（Spec）を起点として AI にコードを生成させる手法・ツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [github/spec-kit](https://github.com/github/spec-kit) | GitHub 公式のスペック駆動開発ツールキット。PRD から実装タスクを自動生成 | Python |
| [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec) | AI コーディングアシスタントのためのオープンなスペック駆動開発フレームワーク | TypeScript |
| [gotalab/cc-sdd](https://github.com/gotalab/cc-sdd) | 承認済みスペックから長時間の自律実装へ繋ぐ最小・汎用の SDD ハーネス。Claude Code・Codex・Cursor・Copilot 等の Agent Skills に対応 | TypeScript |
| [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | 著名ブランドのデザインシステムに着想を得た DESIGN.md コレクション。プロジェクトに置くだけでコーディングエージェントが整合した UI を生成 | — |

---

## セキュリティ / ネットワーク

シークレット漏洩検出・セキュアなネットワーク構築に関するツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [trufflesecurity/trufflehog](https://github.com/trufflesecurity/trufflehog) | Git リポジトリや各種ソースから API キー・パスワードなどの漏洩シークレットを検出・検証するツール | Go |
| [gitleaks/gitleaks](https://github.com/gitleaks/gitleaks) | Git の履歴・ステージングからシークレットを検出する軽量 CLI。CI/CD に組み込みやすい | Go |
| [netbirdio/netbird](https://github.com/netbirdio/netbird) | WireGuard ベースのオーバーレイ VPN。SSO・MFA・細粒度のアクセス制御付きでデバイス間を安全に接続（Zero Trust） | Go |

---

## ネットワーク / OS

ルーター・組込みデバイス向けの OS／ファームウェア。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [openwrt/openwrt](https://github.com/openwrt/openwrt) | ルーター・組込みネットワーク機器向けの Linux ディストリビューション。本リポジトリは公式 git の GitHub ミラー | C |

---

## インフラ / IaC

クラウドインフラの宣言的管理・プロビジョニングに関するツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [opentofu/opentofu](https://github.com/opentofu/opentofu) | Terraform からフォークされた OSS の IaC ツール。クラウドインフラを宣言的に管理。Linux Foundation 配下でコミュニティ主導 | Go |

---

## 開発環境 / ツール

ターミナル環境・dotfiles・仮想化・ライブラリなど開発生産性を高めるツール群。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [starship/starship](https://github.com/starship/starship) | あらゆるシェル向けの高速・最小・カスタマイズ可能なプロンプト。bash / zsh / fish / PowerShell などに対応 | Rust |
| [mozumasu/dotfiles](https://github.com/mozumasu/dotfiles) | macOS 向けの dotfiles 設定集。Neovim・WezTerm・zsh の設定が含まれる | Lua |
| [smol-machines/smolvm](https://github.com/smol-machines/smolvm) | ポータブルで軽量・自己完結型の仮想マシンをビルド・実行するツール（libkrun ベース） | Rust |
| [chenglou/pretext](https://github.com/chenglou/pretext) | 高速・高精度なテキスト計測＆レイアウトライブラリ。フォントメトリクスの精密な制御が必要な UI に有用 | TypeScript |

---

## フォント

プログラミング向けフォント。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [yuru7/HackGen](https://github.com/yuru7/HackGen) | 英数字に Hack、日本語に源柔ゴシックを合成したプログラミングフォント「白源」。日本語環境での可読性が高い | Shell |

---

## エミュレーター

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [shadps4-emu/shadPS4](https://github.com/shadps4-emu/shadPS4) | Windows / Linux / macOS / FreeBSD 向けの PlayStation 4 エミュレーター（C++23・Vulkan ベース） | C++ |

---

> 最終更新: 2026-05-17
