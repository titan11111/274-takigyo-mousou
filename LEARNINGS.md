# 274-takigyo-mousou 学び

## 2026-09-30 タイトルが開始できない

- 妄想データ `THOUGHTS` 15件・`COLD` 5件は `t`/`e` 必須あり。構文エラーはなし
- プレイ不能の原因はデータではなく `#title{pointer-events:none}`。画面タップがキャンバスへ抜け、`state==='play'` 以外では無視されていた
- 開始はタイトル全面の `pointerdown`（`setPointerCapture`）に変更。`#openBtn` は harness 用に残す

## 2026-09-30 タイトル演出・iOS・公開更新

- タイトル「滝行と煩悩」＋VHS風オープニング（本番未反映分を push）
- iOS: viewport 固定・overscroll 防止・ダブルタップ防止・`tg.274.mute`
- タップ開始は `#openBtn`（harness / iOS 両対応） ※直後にタイトル全面タップへ修正
