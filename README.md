<!--
  ファイル名 / File: README.md
  概要 / Description: 品質確認規定のリポジトリの案内 / About this repository
  作成者 / Author: 5garashi.com設計事務所 / 5garashi.com Design Office
  作成日 / Created: 2026-10-13
  ライセンス / License: CC BY-ND 4.0(tools/ と .github/workflows/ は MIT)
  SPDX-License-Identifier: CC-BY-ND-4.0
-->
# 5garashi.com設計事務所 品質確認規定 / Quality Rules

バージョン / Version: 1.0.0([改版履歴 / Changelog](CHANGELOG.md))

準拠 / Conforms to: Design Office Identity 4.22.0

作るもの(ソフトウェア、文書、電子回路・機器、ファームウェア)が、使う人の作業・環境・信頼を守ることを、作る段階から仕込み(作りこみ)、出す前に確かめ(試験)、記録に残すための決まりです。[Design Office Identity](https://5garashi.github.io/5garashi-identity/) が「満たすべき姿」を定めるのに対し、本規定は「満たしていることの作り方と確かめ方」を定めます。

Web で公開しています: https://5garashi.github.io/5garashi-quality/ 。1.0.0 から正式版です。

## ファイル

| ファイル | 内容 |
| :--- | :--- |
| `index.html` | 規定の本文。ブラウザーで開いて読む |
| `VERSION` | 版の番号(Identity 12-7) |
| `CHANGELOG.md` | 改版履歴 |
| `assets/` | Identity の公式アセット(ロゴタイプ・シンボルマーク)。CC BY-ND 4.0 |
| `tools/check_version.py` | 版の番号が `VERSION` と一致するかを確かめる(Identity から写した MIT のツール) |
| `.github/workflows/` | 版を上げたときにタグと Release を作る・プルリクエストで版を確かめる(Identity のひな形、MIT) |

## 改版のしかた

1. `index.html` を直す。
2. 内容が変わるときは `VERSION` を上げ、`CHANGELOG.md` に節を足し、この README の版の行を直す(Identity 12-7 (10))。
3. `python tools/check_version.py --stamp index.html` で本文の版を書き込み、`python tools/check_version.py` で確かめる。

## 関連

- 規定に沿って作った試験の道具: appAutoTester(非公開のリポジトリ 5garashi/appAutoTester)

---

**作成者 / Author**: 5garashi.com設計事務所 / 5garashi.com Design Office
**最終更新 / Last updated**: 2026-11-03 JST
