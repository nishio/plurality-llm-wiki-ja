# Log

> 直近 7 日分のみ。全件 compact 履歴は [log.txt](log.txt)、それより古い entry の詳細は `git log -- wiki/log.md` で参照。
> 更新は `python3 scripts/refresh_logs.py` で log.txt と log.md を再生成する。

## [2026-05-26 23:55] ingest | JA 言語の Audrey Tang / Glen Weyl 発言サーベイ


- 制約: WebSearch / WebFetch が一部ドメインのみ許可 (plurality.net / github.com / scrapbox.io)。汎用 web search は不可だったため、Phase 1 で既に取り込んだ [[plurality-japanese-scrapbox]] (1421 page) 内に保管されている JA Tang/Weyl 発言群を 2 次的に source 化することで Phase 2 の意図 (JA Tang/Weyl の主要発言を網羅) を満たすアプローチに切り替えた。
- 新規 source ページ 6 件を作成: [[Glen in Japan Keynote]] (2024-01-03 Glen 来日 Keynote 詳細対訳)、[[2024-01-08 Audrey and Glen Weyl QA]] (2024-01-08 タン×ワイル Q&A、1972 行記録)、[[Meetup with Audrey and Glen]] (2024-07-23 Plurality Tokyo Discord 主催 meetup)、[[サイボウズ式ブックス刊行記念トークイベント]] (2025 タン×ワイル日本語版刊行記念)、[[デジタル民主主義の未来]] (2025 タン×松尾豊×上野山勝也対談)、[[Plurality伊藤穰一鈴木健石川裕也対談]] (鈴木健の Plurality 出会い経路の本人解説)
- 追加で日本語コミュニティ独自の Plurality 解説として [[Pluralityとは-DeepResearch-nishio|Pluralityとは(Deep Research+nishio)]] (2025-02, CC-0) も source 化
- 既存ページ 4 件に追加情報を Updates / sources にて反映: [[オードリー・タン]] (新 source 5 件を追加)、[[グレン・ワイル]] (新 source 4 件を追加)、[[鈴木健]] (3 者対談 link)、[[安野貴博]] (松尾研系列の人脈情報)、[[プルラリティ]] (タンの「垂直 vs 水平」新定式の引用)
- index.md に「Audrey Tang / Glen Weyl 日本での発言・対談 (時系列)」セクションを追加
- 観察された差異: 日本の AI 戦略言説 (松尾豊 = AI 戦略会議議長) との接続で、[[オードリー・タン]] が「AI の垂直な高度化ではなく水平な価値配分」という [[plurality-book]] にない新しい定式化を導入していた ([[デジタル民主主義の未来]]より)。これは Plurality の対象読者特化バージョン管理の興味深い例

## [2026-05-26 23:30] ingest | plurality-japanese Scrapbox の selective ingest



- source ページ 3 件を作成: [[plurality-japanese-scrapbox]] (1421 page export 全体)、[[Audrey Tang Keynote in Plurality Tokyo]] (2023-04-14 keynote 対訳)、[[第139回 民主主義を発展させるためのテクノロジー「Plurality」]] (関治之 Software Design 寄稿)
- concept ページ 4 件を作成: [[プルラリティの訳語]] (2023-2024 の訳語論争)、[[シンギュラリティ]] (Plurality と対置される概念)、[[協調的多様性]] (Tang の言い換え)
- entity ページ 9 件を作成: [[Plurality Tokyo]]、[[Glen in Japan]]、[[Code for Japan]]、[[nishio]]、[[サイボウズ]]、[[Dos Monos]]、[[伊藤穰一]]、[[Funding the Commons Tokyo]]、[[高木俊輔]]、[[関治之]]
- 既存ページ 6 件に Updates セクションで supplementary material を追加: [[鈴木健]] (なめ敵会・Plurality 比較講演・伊藤穰一対談)、[[オードリー・タン]] (Plurality Tokyo Keynote・真鶴視察・Dos Monos 楽曲)、[[グレン・ワイル]] (来日経緯・Twitter 翻訳公募・衛谷倫の日本名)、[[日本科学未来館]] ("@miraikan ... most allied to Plurality" 評)、[[Polis]] (日本コミュニティでの受容)、[[RadicalxChange]] (日本コミュニティ接続)、[[プルラリティ]] (訳語経緯と Tang による別定式化)
- index.md に新規ページの navigation 追加
- 取り組みの中心仮説: 「日本語コミュニティでは Plurality を [[シンギュラリティ]] への対概念として説明する語り口が他言語圏より強調されている」── [[plurality-japanese-scrapbox]] のテキスト密度から観察された傾向

## [2026-05-26 19:45] ingest | brief-mention pages の backfill





- entity ページ 19 個を作成: [[アイザック・アシモフ]], [[アイン・ランド]], [[イアン・バンクス]], [[イーロン・マスク]], [[ゲオルク・ジンメル]], [[サム・アルトマン]], [[ジャロン・ラニアー]], [[ジョン・デューイ]], [[ニック・ボストロム]], [[ニール・スティーヴンスン]], [[ノーバート・ウィーナー]], [[バラジ・スリニバサン]], [[ピーター・ティール]], [[レイ・カーツワイル]], [[孫文]], [[Cortico]], [[Join]], [[東京都知事選]], [[総統杯ハッカソン]]
- concept ページ 14 個を作成: [[AGI]], [[DAO]], [[GFM]], [[PICSY]], [[⿻管理プロトコル]], [[クリエイティブなコラボレーション]], [[ステークホルダー企業]], [[テクノクラート]], [[デュベルジェの法則]], [[リバタリアン]], [[分人民主主義]], [[国家]], [[資本主義]], [[日本語コミュニティ]]
- 各ページは冒頭で本書での扱いを 1 文で明示してから、外部知識から事実情報を簡潔に添えるパターンを採用
- 残る broken wikilink は章節リンク (1-0 〜 7-1) と [[日本語版刊行に寄せて]] / [[日本語版解説]] の意図的未作成のみ

## [2026-05-26 18:30] ingest | Plurality 本（日本語版）の full ingest






- source ページ [[plurality-book]] を作成（書誌、章立て、CC0、日本語版独自の前文・解説の構造を明記）
- concept ページ 28 個を作成: [[プルラリティ]], [[數位]], [[社会的差異を超えたコラボレーションのための技術]], [[一元論的アトム主義]], [[リバタリアニズム]], [[テクノクラシー]], [[つながった社会]], [[失われた道]], [[狭い回廊]], [[スーパーモジュラリティ]], [[反社会]], [[中央集権]], [[玉山からの眺め]], [[デジタル民主主義]], [[デジタル民主主義 2030]], [[なめらかな社会とその敵]], [[分人]], [[クアドラティック投票]], [[クアドラティック資金調達]], [[液体民主主義]], [[多元投票]], [[拡張熟議]], [[ブロードリスニング]], [[ポスト表象コミュニケーション]], [[没入型共有現実]], [[適応型管理行政]], [[社会市場]], [[データ連合]]
- entity ページ 16 個を作成: [[オードリー・タン]], [[グレン・ワイル]], [[鈴木健]], [[山形浩生]], [[安野貴博]], [[日本科学未来館]], [[台湾]], [[ハンナ・アーレント]], [[ダニエル・アレン]], [[ヘンリー・ジョージ]], [[J・C・R・リックライダー]], [[g0v]], [[vTaiwan]], [[Polis]], [[Talk to the City]], [[RadicalxChange]]
- 出典: akinorioyama/plurality_tentative の CC0 リリースをもとに、サイボウズ式ブックスから 2025 年刊行された日本語版 PDF
- 日本語版独自の文節化: 「[[プルラリティ]]」のカタカナ表記＋「（多元性）」補足、Unicode ⿻ 記号の使用、[[安野貴博]] の 2024 年都知事選事例の本文組み込み、[[鈴木健]] による [[日本語版解説]] と [[なめらかな社会とその敵]] との「双子の書籍」位置づけ、[[日本科学未来館]] の象徴的役割。
