---
type: source
summary: "取得を試みたが access できなかった source の list。人間の手動取得を待つ。"
raw_sources:
  - (各 attempted URL 自身)
---

# Wishlist (fetch help needed)

取得を試みたが access できなかった source を記録。手動で fetch + `raw/` に置けば、後続の ingest で取り込める。

WebSearch / WebFetch の許可されたドメインが現状: plurality.net / github.com / scrapbox.io (実際は plurality-japanese scrapbox は 403) / dlt.kitetu.com のみ。それ以外のドメインは sandbox の permission denied。

## 1. 集英社新書プラス連載「Plurality を読み解く」全話

[[plurality-in-japan-overview]] で既に ④ ([[駒村圭吾]]) が言及されている。① ② ③ ⑤ etc. のページ URL を推定して fetch を試みたが、`shinsho-plus.shueisha.co.jp` ドメインは sandbox 未許可。

### https://shinsho-plus.shueisha.co.jp/news/31459
### https://shinsho-plus.shueisha.co.jp/news/31460
### https://shinsho-plus.shueisha.co.jp/news/31461
### https://shinsho-plus.shueisha.co.jp/news/31462 (= 駒村圭吾 ④、既知)
### https://shinsho-plus.shueisha.co.jp/news/31463 (推定 ⑤)

- **Expected content**: 日本知識人層の Plurality 規範論層の網羅。憲法学・政治学・哲学・社会学の論者による解説連載。集英社新書サイドが意図した思想紹介と批判のラインナップ
- **Attempted**: 2026-05-28 via WebFetch
- **Result**: Permission denied (`shinsho-plus.shueisha.co.jp` not in allowed domains)
- **Help action**: 手動で fetch + `raw/` に置く。URL 番号は連番推定なので、実 URL を確認しつつ。可能なら連載全話 + 著者・公開日を整理してから ingest

## 2. デジタル民主主義 2030 publications (web / blog 部分)

OSS 系の GitHub repository (`github.com/digitaldemocracy2030/*`) は github.com ドメイン経由で fetch 成功。しかし `dd2030.org` 本体の web / publications / blog 部分は未取得。

### https://dd2030.org/
### https://dd2030.org/kouchou-ai/
### https://dd2030.org/idobata/
### https://dd2030.org/publications/ (存在するなら)
### https://note.com/digitaldemocracy/n/nb228136123f4 (Plurality PMF レポート、[[plurality-in-japan-overview]] で既知)
### https://note.com/digitaldemocracy/ (デジタル民主主義 2030 note 全体)

- **Expected content**: 広聴 AI / いどばたの運用レポート、PMF 議論文書、台湾訪問レポート、研究ユニット成果物の note 連載
- **Attempted**: 2026-05-28
- **Result**: dd2030.org / note.com ドメインは sandbox 未許可
- **Help action**: 特に Plurality PMF レポート (`note.com/digitaldemocracy/n/nb228136123f4`) は本書 post-book 文脈の中心的議論文書なので優先的に手動取得を希望

### https://github.com/digitaldemocracy2030/broad-listening-book/blob/main/<原稿ファイル>
- **Expected content**: 書籍『選挙を変えたブロードリスニング』本体原稿 (CC BY-NC 4.0)
- **Attempted**: organization 一覧のみ取得済、個別ファイル名は未確認
- **Help action**: 個別 markdown ファイル一覧と内容を取得すれば、刊行前の早期 ingest が可能

## 3. 鈴木健 2025-2026 post-book 寄稿・講演

[[鈴木健]] の post-book 独立発言を網羅したい。

### https://twitter.com/kensuzuki (X / Twitter アカウント)
### https://note.com/ken_suzuki/ (note 推定 URL)
### https://substack.com/@kensuzuki (Substack 推定 URL)

- **Expected content**: 「双子の書籍」位置づけ後の独立議論、Plurality / なめらかな社会 / SmartNews / ファン国家 の post-book 統合論
- **Attempted**: 2026-05-28 via WebFetch / WebSearch
- **Result**: WebSearch permission denied (sandbox 全 search 不可)。Twitter / note / substack ドメインも sandbox 未許可
- **Help action**: 手動で SNS タイムラインを参照、note / Substack を確認。特に [[Plurality伊藤穰一鈴木健石川裕也対談]] の補足情報・「PMF (プロダクトマーケットフィット)」議論の単独寄稿があれば優先

### https://wired.jp/article/series-6-dialogues-for-smooth-societies-5/ (= [[plurality-in-japan-overview]] で既知)
### WIRED Japan の鈴木健関連記事全般
- **Expected content**: WIRED「なめらかな社会のための対話シリーズ」での鈴木健の post-book 議論
- **Attempted**: wired.jp ドメイン未許可
- **Help action**: WIRED Japan からの記事手動取得

## 4. 書評 / 学界応答 (法学・政治学・哲学界)

刊行後の批判・応答層を網羅したい。現状不足の領域。

### https://wired.jp/article/what-is-plurality-book/ (= [[team-mirai-manifesto]] 10 章で公式参照されている WIRED 日本語版解説記事)
### 中央公論 / 朝日新聞 / 日経 / Newsweek Japan の Plurality 書評
### https://okadaasa.theletter.jp/ ([[岡田麻沙]] の theletter 全体)
### https://diamond.jp/articles/-/370383 ([[李舜志]]『テクノ専制とコモンへの道』記事、既知)

- **Expected content**: 日本語版刊行 (2025-05) 後の批判層を網羅、現状不足
- **Attempted**: wired.jp / okadaasa.theletter.jp / diamond.jp 全て sandbox 未許可
- **Help action**: 各メディアサイトを手動で確認

### 法学者・政治学者・哲学者の Twitter / 学会誌 Plurality 言及
- **Expected content**: 東浩紀、宮台真司、駒村圭吾、岡田麻沙以外の言及。法学・政治学・哲学界の応答
- **Attempted**: WebSearch unavailable → 完全に attempt 不能
- **Help action**: 手動で関連学会誌・SNS を巡回。特に 2025-05 〜 2026-05 の 1 年で日本語版に応答した論者を新規 entity 化したい

## 5. チームみらい 政策ドキュメント深掘り (policy.team-mir.ai)

`github.com/team-mirai/manifesto-body` の MD ファイル経由でマニフェスト全 11 章を取得済 ([[team-mirai-manifesto]] 参照)。しかし以下は未取得:

### https://policy.team-mir.ai/policies/* (各政策の web 表示版)
### https://team-mir.ai/blog/* (チームみらい公式 blog 寄稿)
### https://kaigi.team-mir.ai/themes/* (みらいいどばた会議の個別議論テーマ)
### https://gikai.team-mir.ai/ (みらい議会本体)

- **Expected content**: マニフェスト本体 + 各政策の web 表示版での解説。blog 寄稿の安野貴博論説。みらいいどばた会議の議論ログ
- **Attempted**: policy.team-mir.ai / team-mir.ai / kaigi.team-mir.ai / gikai.team-mir.ai 全て sandbox 未許可
- **Help action**: github.com/team-mirai/manifesto-body の git 履歴を経由した content 取得は可能 (既に実施済)。web 側の動的コンテンツ (議論ログ・blog) は手動取得が必要

### https://github.com/team-mirai/policy (archived 2025-07-26)
- **Expected content**: マニフェスト v1.0 (archived) の旧版議論。5000+ PR の議論履歴
- **Attempted**: archived repository の API access は可能だが、5000+ PR の系統的取得は wishlist
- **Help action**: 特定 PR の議論 (例えば AI / Plurality 周辺の長い議論) を選択的に取得して、合意形成プロセスの記録として ingest

## 6. 安野貴博の単独寄稿・講演

[[team-mirai-manifesto]] からは党首としての公式声明は取得済だが、安野個人の post-book 単独寄稿は未網羅。

### https://twitter.com/takahiroanno
### https://note.com/takahiroanno
### YouTube「AI あんの」/「AI 安野」の最新動画

- **Expected content**: 党 / OSS コミュニティ分離 (2025-05 ボード辞職) の本人説明、SF 作家としての post-book 言説
- **Attempted**: Twitter / note / YouTube ドメイン未許可
- **Help action**: 手動取得

## まとめ

ほぼ全 web ドメインが sandbox で permission denied のため、本セッションでは:

- **成功**: github.com ドメイン (DD2030 / Team Mirai / Plurality book の GitHub repos) からの fetch のみ
- **失敗**: 集英社新書プラス / dd2030.org web / note.com / Twitter / WIRED / 朝日 / 日経 / theletter.jp / diamond.jp / その他主要メディア

このため、今回 ingest できた範囲は **GitHub 上の OSS 文書 (主にチームみらいマニフェスト 11 章 + DD2030 organization profile)** に限定された。web メディア / SNS / 連載記事の網羅は人間による手動取得を待つ。
