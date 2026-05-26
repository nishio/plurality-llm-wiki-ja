# plurality-llm-wiki-ja

多言語 [plurality-llm-wiki](https://github.com/nishio/plurality-llm-wiki) wiki森 の **日本語版**。日本語 Plurality 言説における概念体系 ── Plurality 本日本語版、和訳コミュニティ議論、日本イベント、Audrey 講演の和訳・要約などをソースとする。

**公開サイト:** https://nishio.github.io/plurality-llm-wiki-ja/

## 兄弟 wiki との関係

本 wiki は **自律的**。ページは [en 側 wiki](https://github.com/nishio/plurality-llm-wiki-en) の翻訳である必要も、対応している必要もない。各言語は概念空間を異なる仕方で文節化し、その差異それ自体が parent wiki森 の観察・分析対象になる。

言語間の対応 (および明示的な欠落) は parent の [correspondences.yaml](https://github.com/nishio/plurality-llm-wiki/blob/main/correspondences.yaml) で追跡される。そこの行は Wikipedia の interlanguage link に相当する ── 「これらのページは同じ/関連する話題について」と主張するだけで、内容の等価性は主張しない。

## Repository 構成

```
wiki/
├── index.md             人間向け curated navigation
├── log.md               人間向け直近 7 日の activity log
├── concepts/            概念ページ
├── entities/            人物・ツール・プロジェクト
├── sources/             ソース要約
└── analyses/            問いから生まれた考察
```

`index.txt` / `log.txt` は AI 向けの auto-generated ファイル ── 手で編集しない。

## Contributor 向け

- 運用詳細・ページ規約・frontmatter schema: [CLAUDE.md](CLAUDE.md)
- ページ追加・rename・削除のあと: `python3 scripts/build_index_txt.py`
- log 追記のあと: `python3 scripts/refresh_logs.py`
- 機械的健全性チェック: `python3 scripts/lint_wiki.py`

## 運用方針

- ソースは「参考」であり無批判に採用しない
- en 側との翻訳整合を強制しない ── 差異こそが本 wiki森 の主題
- スキーマ (CLAUDE.md) も実験を通じて改善していく
