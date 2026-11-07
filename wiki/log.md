# Log

> 直近 7 日分のみ。全件 compact 履歴は [log.txt](log.txt)、それより古い entry の詳細は `git log -- wiki/log.md` で参照。
> 更新は `python3 scripts/refresh_logs.py` で log.txt と log.md を再生成する。

## [2026-11-07 20:30] file back | ページをまたいだ食い違いの監査（Codex gpt-6.1-sol、閉じる 3・現状更新 9・継続 66・人の判断待ち 11、本物 12・古い方が残っている 3・判定できない 6）

- grasp-nishio のセッションから、Codex にページ間の矛盾（数値・日付・決定・名前・状態）を探させ一次ソースでどちらが現状かを確かめさせ、別の Codex セッションが全件を敵対的に検証した。報告は raw/consistency-audit-2026-11-07.md・raw/consistency-verify-2026-11-07.md

## [2026-11-07 20:30] file back | Open Questions の現状突合（Codex gpt-6.1-sol、閉じる 3・現状更新 9・継続 66・人の判断待ち 11）

- grasp-nishio のセッションから、Codex に `## Open Questions` の各項目を一次ソース（git blame・Updates・log・参照先の repo）で突合させ、別の Codex セッションが全判定を敵対的に検証した。報告は raw/open-questions-triage-2026-11-07.md・raw/open-questions-verify-2026-11-07.md

## [2026-10-08 12:00] filing-back | 日本語版前文の日付の取り違えを訂正


- [[plurality-book]] の「日本語版の独自性」が、タンとワイルの両者が 2024-07-26 の [[日本科学未来館]] 訪問を語るとしていたのを訂正。タンの前文①は 1998-07-26 の MTG アジア太平洋選手権・i モード・調和を語り、未来館訪問を語るのはワイルの前文②のみ（raw/PLURALITY_Japanese.txt で確認）。2026-10-07 の wiki森横断の事実確認で見つかったもの。

## [2026-10-06 20:27] filing-back | 「技術が既存の制度を機能不全にする」論の出典はデューイ



- 西尾の問い「技術の進歩が社会構造を変え、既存のものを機能不全にするという話はデューイだっけ？」への答えを [[ジョン・デューイ]] の Updates に追記。本書 3-2 (日本語版 p.88-89) の該当箇所を引用し、オグバーン「文化的遅滞」・マルクスとの区別を付記した。原典との章対応は Open Questions に残す。
