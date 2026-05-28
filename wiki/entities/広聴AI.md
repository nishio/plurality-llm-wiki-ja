---
type: entity
summary: デジタル民主主義 2030 が開発したオープンソース AI 分析ツール。Talk to the City をベースに日本の自治体・政治家の実務に合わせて改良。2025-03-16 公開。
sources:
  - plurality-in-japan-overview.md
---

# 広聴AI

[[デジタル民主主義 2030]] が開発した、ブロードリスニングを支援するオープンソース AI 分析ツール。

## 概要

> [[Talk to the City]] をベースに、日本の自治体や政治家の実務に合わせた改善を行ったもの ([[plurality-in-japan-overview]] より、dd2030.org/kouchou-ai/)

- 2025-03-16 公開
- 大量の自由記述・SNS 投稿・対話ログを AI でクラスタリング、要約、可視化

## 渋谷区トライアル (2025-07)

> 渋谷区は 2025 年 7 月、令和 6 年度区民意識調査の自由記述欄 6,037 件を広聴AIで分析し、自動要約、トピック分類、世代・地域別傾向分析を行った ([[plurality-in-japan-overview]] より、www.city.shibuya.tokyo.jp/kusei/hodo/hodo-2025/hodo_20250702.html)

Plurality 的な「多様な声を聞く」方向が、自治体の広聴業務に入り始めた最初期の事例。

## 関連
- [[ブロードリスニング]]
- [[Talk to the City]]
- [[デジタル民主主義 2030]]
- [[非決定権力]] (アルゴリズムの透明性と恣意性排除が課題)
- [[いどばた]] (「聞く」に対する「議論する」プラットフォーム)

## Updates

### 2026-05-28: v4.0.0 release / 機能拡張

GitHub README (`github.com/digitaldemocracy2030/kouchou-ai`, AGPL-3.0, 166 stars / 61 forks 2026-05 時点) より:

- v4.0.0 release: 2025-12-27
- Backend: Python (FastAPI) on port 8000
- Frontend: Next.js/TypeScript の **public viewer (port 3000) + admin interface (port 4000)** で分離
- Docker containerization、Optional GPU support with **Ollama for local LLM** (政府機関のオフライン要件への配慮)
- 計画機能: **Dense cluster extraction** (集中意見の抽出) / **Public comment analysis** / **Majority attack defense mechanisms** (パブコメ多数派工作対策)

「multi attack defense」機能の計画は [[team-mirai-manifesto]] 10 章の「**パブリックコメント制度では何個も同じ趣旨の投稿を繰り返す多数派工作などの存在がある**」という問題認識と直結している。本書 [[5-4 拡張熟議]] の課題認識を実装レベルで対処する試み。

### 2026-05-28: チームみらいでも使用、政党を超えた採用

[[team-mirai-manifesto]] 10 章でも「具体的なプロダクト: TTTC・**広聴 AI**」として明示参照。`github.com/team-mirai/kouchou-ai` という別 fork (21 stars) も存在し、政党と OSS コミュニティ間で fork ベースの相互運用が行われていることが観察される。
