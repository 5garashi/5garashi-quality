<!--
  ファイル名 / File: TESTING.md
  概要 / Description: 品質確認規定を変えたときに、何をどう確かめ、どう報告するか / How to check and report changes to the Quality Rules
  作成者 / Author: 5garashi.com設計事務所 / 5garashi.com Design Office
  作成日 / Created: 2026-11-03
  ライセンス / License: MIT
  SPDX-License-Identifier: MIT
-->
# 品質確認規定のテスト

このリポジトリを変えたら、この文書に従って確かめ、結果を報告します。変更を始める前に読んでください。

## 1. すべての変更で

1. **版**: 内容が変わるときは、`VERSION`・`CHANGELOG.md`・README の版の行を上げる(Identity 12-7 (10))。`python tools/check_version.py --stamp index.html` で本文に版を書き込み、`python tools/check_version.py` が `OK` になることを確かめる(品質確認規定 14-1 (1))。
2. **HTML のタグ**: `index.html` の開始と終了のタグが対応していること。Python の `html.parser` で、閉じていないタグと、対応しない終了タグが 0 件であることを確かめる。
3. **参照**: 条・節・項の番号を変えたときは、本文と Identity の中の参照(「6-4」「第15条 (7)」など)を検索し、今の番号と合っていることを確かめる。CHANGELOG に旧と新の対応を書く(Identity 12-7 (15))。

## 2. 表示を変えたとき(表、リンク、書式、CSS)

1. Microsoft Edge で、幅 320px に表示し、ページ全体に横のスクロールが出ないことを確かめる(Identity 7-7 (d))。表とコードの枠の中で横にスクロールするのはよい。長い URL をリンクの文字にすると、折り返せずにはみ出すので、リンクの文字は短い言葉にする。
2. 色を変えたときは、文字色と背景色の比を測り、Identity 第4条・7-1 の基準と比べる。比は CSS のコメントに書く。

## 3. 公開した後

`main` に入れると、GitHub Pages(https://5garashi.github.io/5garashi-quality/)と、タグ・Release が更新される。公開ページを開き、表紙の版(`data-version`)が `VERSION` と一致することを確かめる(品質確認規定 14-2 (8))。

## 4. 報告

1〜3 のどれを行い、結果はどうだったかを書きます。行っていない確認は「未実施」と書きます(例: 「版の確認 OK、タグの対応 OK、幅 320px は表示を変えていないため未実施」)。

---

**作成者 / Author**: 5garashi.com設計事務所 / 5garashi.com Design Office
**最終更新 / Last updated**: 2026-11-03 JST
