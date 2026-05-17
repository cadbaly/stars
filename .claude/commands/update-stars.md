---
description: cadbaly の最新 GitHub スターを取得し、差分（追加・削除）があれば README.md を更新して PR を作成する
---

# update-stars

cadbaly がスターしたリポジトリの最新一覧を取得し、`README.md` との差分（**追加されたスター・削除（un-star）されたスター**）があればブランチを切って更新 PR を作成します。

## 手順

以下を順に実行してください。各ステップの結果を確認しながら進めてください。

### 1. 最新スターを取得して差分を確認

GitHub API でスター一覧を取得します。`--paginate` で全ページを自動結合します。

```bash
gh api --paginate -H "Accept: application/vnd.github+json" "users/cadbaly/starred?per_page=100" \
  --jq '.[] | "\(.full_name)\t\(.html_url)\t\(.description // "")\t\(.language // "")"' > /tmp/stars-latest.tsv
wc -l /tmp/stars-latest.tsv
```

`README.md` を読み込み、現在掲載されているリポジトリ（`owner/repo` 形式）を抽出して、API 結果と双方向に比較し、以下を特定します。

- **追加分**: API にあるが README にない → 新規スター
- **削除分**: README にあるが API にない → un-star されたリポジトリ

両方ゼロ件なら「変更なし」と報告して終了します。削除分があった場合は、ユーザーに「以下を README から削除します」と一覧を提示し、確認を取ってから先に進んでください（誤検出時の被害を抑えるため）。

### 2. main ブランチを最新化

差分があった場合のみ実行します。未コミットの変更がある場合は処理を中止し、ユーザーに確認してください。

```bash
git status --porcelain  # クリーンであることを確認
git checkout main
git pull origin main
```

### 3. ブランチを作成

今日の日付（`date +%Y-%m-%d`）を使ってブランチを切ります。同名ブランチが既にある場合は連番（`-2`, `-3`）を付けてください。

```bash
git checkout -b update-stars-$(date +%Y-%m-%d)
```

### 4. README.md を更新

**追加分:** 新規リポジトリそれぞれについて、適切なカテゴリ（既存カテゴリのいずれか）を判断し、テーブルに追加します。
- 既存カテゴリに収まらない場合は、新カテゴリを目次・本文の両方に追加
- 各エントリは既存フォーマットを踏襲: `[owner/repo](url) | 概要（日本語） | 言語`
- 概要は GitHub API の description を踏まえて日本語で簡潔に（既存エントリのトーンに合わせる）

**削除分:** un-star されたリポジトリの行をテーブルから削除します。
- 削除によりカテゴリ内のエントリが 0 件になった場合は、そのカテゴリ自体（見出し・説明文・テーブル枠・目次のリンク）も削除
- 該当カテゴリが本文末尾の `---` 区切り含めて綺麗に消えるよう注意

**最終更新日:** ファイル末尾の `> 最終更新: YYYY-MM-DD` を今日の日付に更新

### 5. コミット & プッシュ

```bash
git add README.md
git commit -m "$(cat <<'EOF'
<件名: 例「Add N newly starred repos」または日本語で簡潔に>

<本文: 追加リポジトリのリストと、新カテゴリ追加など特記事項>

Co-Authored-By: Claude Opus 4.7 <noreply@anthropic.com>
EOF
)"
git push -u origin HEAD
```

### 6. PR を作成

過去 PR（#1, #2）と同じ日本語フォーマットで作成します。

```bash
gh pr create --title "<タイトル: 例「スター差分の反映（追加 N 件 / 削除 X 件）」>" --body "$(cat <<'EOF'
## Summary
- 新規スター N 件を追加: <リポジトリ名のリスト>
- un-star により X 件を削除: <リポジトリ名のリスト>
- <新カテゴリ追加・空になったカテゴリの削除など特記事項があれば>
- 既存カテゴリへの追加:
  - <カテゴリ名>: <repo>（<一言>）

合計 M リポジトリを K カテゴリに整理。

## Test plan
- [ ] README.md が GitHub 上で正しくレンダリングされる
- [ ] 目次のアンカーリンクが各セクションに正しく飛ぶ
- [ ] 全 M リポジトリが漏れなく掲載されている
- [ ] 削除したリポジトリが本文・目次の両方から消えている

🤖 Generated with [Claude Code](https://claude.com/claude-code)
EOF
)"
```

最後に PR の URL をユーザーに返してください。

## 注意

- 追加・削除の両方を対象とします。削除分は事前にユーザー確認を取ること
- `--paginate` を使えばページ漏れは起きないが、`wc -l` の件数が想定より極端に少ない場合は API レスポンスを直接確認すること
- 既存の表記・トーン・絵文字の有無を尊重してください
- 不明点（カテゴリ判断に迷うリポジトリなど）はユーザーに確認してから進めてください
