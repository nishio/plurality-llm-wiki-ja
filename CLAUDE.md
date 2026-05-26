# plurality-llm-wiki-ja

## テーマ
**日本語の Plurality 言説**における概念体系。ソースは Plurality 本日本語版、和訳コミュニティ議論、日本イベントの記録、Audrey 講演の和訳・要約など。

多言語 [plurality-llm-wiki](https://github.com/nishio/plurality-llm-wiki) wiki森 の一部。本 wiki は **自律的** であり、ページは en 側 wiki ([plurality-llm-wiki-en](https://github.com/nishio/plurality-llm-wiki-en)) の翻訳である必要も、対応している必要もない。

> 各言語は概念空間を異なる仕方で文節化する。その差異それ自体が、本 wiki森 の観察・分析対象 ── 差異が価値を生み出す。

## ディレクトリ構造

```
plurality-llm-wiki-ja/
├── CLAUDE.md                          # このファイル
├── raw/                               # 生のソース (gitignored)
├── wiki/
│   ├── index.md                       # 人間向け curated navigation
│   ├── index.txt                      # AI 向けフルカタログ (auto-generated)
│   ├── log.md                         # 人間向け直近 7 日 (full detail)
│   ├── log.txt                        # AI 向け全件 compact 履歴 (auto-generated)
│   ├── concepts/                      # 概念ページ
│   ├── entities/                      # 人物・ツール・プロジェクト
│   ├── sources/                       # ソースの要約
│   └── analyses/                      # 問いから生まれた考察
├── scripts/
│   ├── lint_wiki.py                   # wiki 健全性チェック
│   ├── build_index_txt.py             # index.txt を frontmatter から regenerate
│   └── refresh_logs.py                # log.txt と log.md (直近7日) を同期
├── quartz/                            # GitHub Pages 配信用 Quartz
├── quartz.config.ts / quartz.layout.ts
├── package.json / pnpm-lock.yaml
└── .github/workflows/deploy-pages.yml # main push で自動 deploy
```

## 言語間の対応

言語間の概念対応は parent の [correspondences.yaml](https://github.com/nishio/plurality-llm-wiki/blob/main/correspondences.yaml) に住む。Wikipedia の interlanguage link と同等 ── 行は「同じ/関連する話題」と主張するだけで、内容の等価性は主張しない。

新しい concept page を本 wiki に追加したら:
- `correspondences.yaml` に行を追加して en 側の概念と対応づける (片方は null = 対応なし)
- もしくは「対応なし (en: ~)」を明示的に記録 ── これは漏れではなく観察された事実

## ページルール

### 全ページ共通
- 冒頭に YAML frontmatter: `type`, `summary`, `sources`
- 出典は `[[source名]]より` で明示
- 矛盾・未解決の論点は `## Open Questions` で明示
- 更新は上書きせず `## Updates` で追記
- wikilink は `[[Page Name]]` (Wikipedia 形式の double brackets)

### フロントマター例
```yaml
---
type: concept
summary: 1 文で説明
sources:
  - source-page-name.md
---
```

## 操作

### Index メンテ (AI/人間分離, kouchou pattern)

- **`wiki/index.md`** — 人間向け curated nav。手動で編集。onboarding / Concepts / Entities の curated 入口を持つ
- **`wiki/index.txt`** — AI 向けフルカタログ。**手で編集しない**。ページ追加・rename・削除・frontmatter summary 変更後に regenerate:
  ```sh
  python3 scripts/build_index_txt.py
  ```

### Log メンテ (AI/人間分離, kouchou pattern)

- **`wiki/log.md`** — 人間向け直近 7 日 full detail, newest first。手動で先頭に `## [YYYY-MM-DD HH:MM] <type> | <title>` を追加
- **`wiki/log.txt`** — AI 向け全件 compact 履歴。**手で編集しない**。log.md に追記したあと regenerate:
  ```sh
  python3 scripts/refresh_logs.py
  ```

`refresh_logs.py` は lint type entry を除外し (無検出 lint は記録しない)、log.md から 7 日より古い entry を落とす (log.txt には残る)。

### Ingest (raw → wiki)
1. `raw/` の新ファイルを読む (必要なら意味のある名前に rename)
2. 既存 wiki ページと照合
3. 更新 or 新規作成 (frontmatter 必須)
4. ページ集合が変わったら `python3 scripts/build_index_txt.py`
5. log.md 先頭に `## [YYYY-MM-DD HH:MM] ingest | <description>` を追加
6. `python3 scripts/refresh_logs.py`
7. 新概念が en 側と対応しそうなら parent の `correspondences.yaml` を更新

### Query
1. `wiki/` を検索して回答
2. 有用な回答は `analyses/` に filing back
3. `filing-back` として log し `refresh_logs.py`

### Lint
1. 機械的: `python3 scripts/lint_wiki.py`
2. 意味的: 矛盾・stale claim・概念ページ不足・新質問の提案
3. 検出ありの lint のみ log 記録 (無検出は `refresh_logs.py` が自動で落とす)

## GitHub Pages

`main` への push で `.github/workflows/deploy-pages.yml` が Quartz ビルド + deploy: https://nishio.github.io/plurality-llm-wiki-ja/

## 運用方針

- ソースは「参考」であり無批判に採用しない
- en 側との翻訳整合を強制しない ── 差異こそが本 wiki森 の主題
- スキーマ (このファイル) も実験を通じて改善していく
