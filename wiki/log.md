# Log

> 直近 7 日分のみ。全件 compact 履歴は [log.txt](log.txt)、それより古い entry の詳細は `git log -- wiki/log.md` で参照。
> 更新は `python3 scripts/refresh_logs.py` で log.txt と log.md を再生成する。

## [2026-09-30 23:59] filing-back | wiki森の横断照合で見つかった食い違い 6 件を修正


- wiki森の public wiki 12個を grasp `cross-project-spreads` で同名 handle ごとに束ね、Gemini（3.8 Flash medium / 3.1 Pro）に wiki をまたぐ食い違いを挙げさせ、Claude が原文と照らして判定した（2026-09-30、galleria の taskF）。Gemini の修正案はそのまま当てていない。
- 章番号: [[Polimoney]] / [[Futarchy]] / [[デジタル民主主義 2030]] の「5-2 投票」「6-2 メディア」を目次 ([[plurality-book]]) に合わせ [[5-6 多元投票]] / 6-3 メディアへ。
- [[Futarchy]]: 「本書に直接的言及はない」→ 英語版 5-6 の本文と脚注に Hanson の提案として出る (上流 repo で確認、日本語版の訳語は未確認)。
- [[reversealignment-jp]]: 「DD2030 系は入っていない」→ 日本からの賛同者 [[鈴木健]] は DD2030 共同設立者。実践の担い手は入っていない、に修正 ([[鈴木健]] の Updates と整合)。
- [[拡張熟議]]: Polis を「[[g0v]] が開発した OSS」→ Computational Democracy Project の OSS (vTaiwan は g0v 発のプロセス)。
- [[オードリー・タン]] 年表: 2024 年に退いたのは数位発展部部長 (22 行の本書引用は触らない)。
- [[ブロードリスニング]]: DD2030 で安野・鈴木が「実験」中の現在形に、安野の 2025-05 ボード辞職 ([[安野貴博]]) を反映。

## [2026-09-24 00:27] ingest | リバースアライメント (Weyl/Evans/White 2026-07) と日本の位置



[[nishio]] の X 投稿 (2026-09-24 00:04) とその解説を起点に、web 原文 2 件を直接取得して ingest。

新規 source: [[reverse-alignment-noema]] (Noema 2026-07-21、原文取得)、[[reversealignment-jp]] (公式サイト日本語版、2026-09-24 取得)。
新規 concept: [[リバースアライメント]]、[[道具のかたちをした制度]]。
Updates 追記: [[ブロードリスニング]] / [[グレン・ワイル]] / [[チームみらい]] / [[鈴木健]] / [[nishio]]。

ja 言説の観察として記録したこと:

- 論考は日本の [[ブロードリスニング]] を "Japan's political broad listening movement" として、[[チームみらい]] を "Japan's fastest-growing political party" として 12 課題の実例に引く。日本語の新語が英語に戻るとき翻訳されず broad listening のまま戻る
- **訳語未定着**: 公式日本語サイトは「Reverse Alignment」をラテン文字のまま置き、[[nishio]] はカタカナ。[[プルラリティの訳語]] と同型の初期局面
- 日本語版の課題見出し 006「共通点の可視化」は原文 Communal Sensemaking より狭く carve され直している
- **事例としての日本と作り手としての日本の非対称**: 連合賛同者 26 名中、日本から掲載は [[鈴木健]] 1 名のみ
- ingest 元の解説にあった「超知能を人間+AI+制度の集合知能として作る」という読みは、**原文 V 節に対応する定式が無い**ことを確認し、Open Question として分離した
- 同語の競合用法 (Harrison 2026, AI & SOCIETY = 人間の側が機械可読な指標へ単純化される危険) は書誌のみ確認、本文は購読壁で未読と明記

correspondences.yaml に 2 行追加 (en: ~ は言説の void ではなく **en 側 ingest の穴** と注記)。
