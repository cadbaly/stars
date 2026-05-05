# cadbaly's GitHub Stars

cadbalyがスターしたリポジトリを用途別にカテゴリ分けしたリンク集です。

---

## 目次

- [Claude Code リソース](#claude-code-リソース)
- [LLM / AI ツール](#llm--ai-ツール)
- [AI エージェント / スキル](#ai-エージェント--スキル)
- [スペック駆動開発](#スペック駆動開発)
- [セキュリティ / ネットワーク](#セキュリティ--ネットワーク)
- [開発環境 / ツール](#開発環境--ツール)
- [フォント](#フォント)
- [エミュレーター](#エミュレーター)

---

## Claude Code リソース

Claude Code（Anthropic の CLI エージェント）の活用に特化したリポジトリ群。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [anthropics/claude-code-action](https://github.com/anthropics/claude-code-action) | GitHub Actions と Claude Code を統合する公式アクション。PR やイシューに AI レビュー・コード生成を組み込める | TypeScript |
| [anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official) | Anthropic 公式が管理する高品質な Claude Code プラグイン（MCP・Skills）のディレクトリ | Python |
| [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | Claude Code に関するスキル・フック・スラッシュコマンド・エージェント等のキュレーション Awesome リスト | Python |
| [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) | Claude Code の設定・監視を行う CLI ツール。テンプレート管理に便利 | Python |
| [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) | Claude Code / Codex / Cursor 向けのエージェントハーネス最適化システム（スキル・記憶・セキュリティ） | JavaScript |
| [nilbuild/claude-statusline](https://github.com/nilbuild/claude-statusline) | Claude Code 用のシンプルなステータスライン設定。ターミナルに進捗を表示 | Shell |
| [GenerativeAgents/claude-code-book-chapter8](https://github.com/GenerativeAgents/claude-code-book-chapter8) | Claude Code 解説書の第8章サンプルコード | TypeScript |
| [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills) | Andrej Karpathy の LLM コーディング観察に基づく CLAUDE.md 一枚。Claude Code の挙動を改善 | — |

---

## LLM / AI ツール

大規模言語モデルの活用・統合・最適化に関するツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [BerriAI/litellm](https://github.com/BerriAI/litellm) | 100 以上の LLM API を OpenAI 形式で呼び出せる SDK／プロキシ（AI Gateway）。コスト追跡・ガードレール・ロードバランシング対応 | Python |
| [rtk-ai/rtk](https://github.com/rtk-ai/rtk) | LLM のトークン消費を 60〜90% 削減する CLI プロキシ。Rust 単一バイナリで依存ゼロ | Rust |
| [microsoft/markitdown](https://github.com/microsoft/markitdown) | PDF・Word・Excel などのファイルを Markdown に変換する Python ツール。RAG のデータ準備に活用できる | Python |

---

## AI エージェント / スキル

汎用 AI エージェントや、Claude Code・openclaw など複数プラットフォーム対応のエージェント／スキル。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [openclaw/openclaw](https://github.com/openclaw/openclaw) | 任意 OS／プラットフォームで動作する個人向け AI アシスタント。データ主権を重視 🦞 | TypeScript |
| [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) | Claude / Codex / OpenAI など複数バックエンドに対応する成長型エージェント | Python |
| [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill) | Reddit・X・YouTube・HN・Polymarket・Web を横断調査して根拠付きで要約する AI エージェントスキル | Python |

---

## スペック駆動開発

仕様書（Spec）を起点として AI にコードを生成させる手法・ツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [github/spec-kit](https://github.com/github/spec-kit) | GitHub 公式のスペック駆動開発ツールキット。PRD から実装タスクを自動生成 | Python |
| [Fission-AI/OpenSpec](https://github.com/Fission-AI/OpenSpec) | AI コーディングアシスタントのためのオープンなスペック駆動開発フレームワーク | TypeScript |

---

## セキュリティ / ネットワーク

シークレット漏洩検出・セキュアなネットワーク構築に関するツール。

| リポジトリ | 概要 | 言語 |
|---|---|---|
| [trufflesecurity/trufflehog](https://github.com/trufflesecurity/trufflehog) | Git リポジトリや各種ソースから API キー・パスワードなどの漏洩シークレットを検出・検証するツール | Go |
| [gitleaks/gitleaks](https://github.com/gitleaks/gitleaks) | Git の履歴・ステージングからシークレットを検出する軽量 CLI。CI/CD に組み込みやすい | Go |
| [netbirdio/netbird](https://github.com/netbirdio/netbird) | WireGuard ベースのオーバーレイ VPN。SSO・MFA・細粒度のアクセス制御付きでデバイス間を安全に接続（Zero Trust） | Go |

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

> 最終更新: 2026-05-05
