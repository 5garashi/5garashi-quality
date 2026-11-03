<!--
  ファイル名 / File: CHANGELOG.md
  概要 / Description: 品質確認規定の改版履歴 / Revision history of the Quality Rules
  作成者 / Author: 5garashi.com設計事務所 / 5garashi.com Design Office
  作成日 / Created: 2026-10-13
  ライセンス / License: CC BY-ND 4.0
  SPDX-License-Identifier: CC-BY-ND-4.0
-->
# 改版履歴 / Changelog — 5garashi.com設計事務所 品質確認規定 / Quality Rules

版ごとの変更を、新しい版を上に書く(Design Office Identity 12-7 (9))。
Changes by version, newest first (Identity 12-7 (9)).

## 1.1.0 — 2026-11-03

TESTING.md を必ず作ることと、AI への共通の指示の置き方を定めた。
TESTING.md is now always created, and shared AI instructions have one source.

- 第11条 (9):TESTING.md がないときは、新しく作るとき・改版するときに、決める人に確かめずに作る。自動の試験がまだないときも、何で確かめるかを書く。試験のしかたを変えたら、同じ変更で直す。
  Art. 11 (9): create TESTING.md without asking when making or revising a product; describe the checks even without automated tests.
- 第12条 (8) を新設:AI への共通の指示は1つの正本に書き、使うすべての AI が、どのフォルダーで起動しても読む場所へ写す。リポジトリごとに写しを置かない。写す先を足した・変えたときは、新しい会話で読み込まれていることを確かめる。AI が決まりを守らなかったときは、まず読み込まれていたかを確かめる。VS Code の Copilot が共通の指示を読み込んでおらず、水平展開をしなかった実例(2026-11-03)を載せた。
  New Art. 12 (8): one source for shared AI instructions, copied to where every AI reads them, with a check that each AI loads them.
- 本リポジトリに TESTING.md を足した(第11条 (9) の当てはめ)。
  This repository now has a TESTING.md.

## 1.0.0 — 2026-11-03

未定の項目をすべて定め、正式版とした。
All undecided items are defined; this is the first official version.

- 第14条 リリース手順を定めた(14-1 は 0.9.0 から)。14-2 出す前の手順:変更全体を見る、版を上げる、git に入っているファイルだけで作る、作った物で試験する、出してよいか決める、配布物を確かめる、出す、出した物を使う人と同じ方法で取得して確かめる。14-3 不合格のまま出すとき:「重大」は出さない。「通常」「軽微」は判断した人・理由・影響と回避・直す予定を記録すれば出してよく、「通常」は CHANGELOG に既知の問題として書く。14-4 配布物の確認(必須の文書、版と名前、元のコミット、PC の情報や認証情報を入れない)。14-5 署名とストアへの提出(鍵を入れない、提出と公開は所有者、同じ版の番号で中身を変えない)。14-6 出荷の検査(電子回路・機器の全数)。14-7 出した後の不具合(受け付け、重さ、再現する試験と水平展開、知らせ)。mdEditor 1.0.12 の記録(手元にだけあったファイルでビルドが失敗した、出荷の判断の理由が書かれていなかった)を根拠にした。
  Art. 14 defined: release steps, releasing with failures (never with "critical" ones), distribution checks, signing and store submission, outgoing inspection for hardware, and defects after release.
- 6-6 を定めた:Web ページ(表示、リンク、通信、継続、公開の後)、コマンドラインのツール(引数、結果、文字とパス、作業を失わせない)、スクリプト(変える前に示す、何度流しても同じ、途中の失敗、権限と環境)。
  6-6 defined for web pages, command-line tools, and scripts.
- 9-2 (1) を暫定から正式にし、(d) から 14-3 を参照した。9-2 (8) を 14-3 によるとした。10-3 (6):記録と報告書は公開の場に置かなくてよく、置くときは PC の情報や使う人のデータが入っていないことを確かめる。
  9-2 (1) is no longer interim; 9-2 (8) and 10-3 (6) are defined.
- 表紙の「草案」の表示を外し、第15条 (2) を「1.0.0 から正式版」とした。第1条 (2) から未定の記述を外し、第15条の未定の項目の表を「未定の項目はない」とした。
  The draft label is removed; Art. 15 (2) states that 1.0.0 is the first official version.

## 0.9.0 — 2026-11-03

Identity から、確かめ方と記録の条を移した(Identity 4.22.0 と同時)。Identity には満たすべき条件を残し、本規定には確かめ方と記録を置く(Identity 1-4 (5))。
Verification and record-keeping articles moved here from Identity (together with Identity 4.22.0); Identity keeps the requirements.

- 6-4「文書(Markdown と図)」を定めた:3つを分けて確かめる、配る環境で確かめる(GitHub と mdEditor の両方、8-9 (8)(9) の文書の扱い)、確かめる項目、自動と目視を分けた記録、置き場所。Identity 8-9 (1)(5)(6) と MARKDOWN-CHECKLIST の 4 節から移した。
  6-4 "Documents (Markdown and diagrams)" defined, from Identity 8-9 (1)(5)(6) and checklist section 4.
- 6-5「公開する前のアクセシビリティの確認」を新設:Identity 7-7 の (a)〜(k) に判定(9-1)を付け、自動と人の確認を分け、10-4 (1) で記録する。Identity 7-7 の確認と記録から移した。
  New 6-5: confirm and record Identity 7-7 (a) to (k) with the 9-1 verdicts.
- 10-4「確認記録のひな形」を新設:(1) アクセシビリティの確認記録(Identity 9-5 から。結果の欄を 9-1 の判定にした)、(2) 文書の確認記録(チェックリストの 7 節から)。9-2 (7) の参照を 10-4 にした。
  New 10-4 record templates, from Identity 9-5 and checklist section 7; 9-2 (7) now refers to it.
- 14-1「版の確認とタグ」を新設:`check_version.py` による確認、Actions によるタグと Release、プルリクエストでの確認。Identity 12-7 (6)(11) から移した。第14条は「一部未定」とし、残りを 14-2 にまとめた。
  New 14-1 on version checks, tags, and Releases, from Identity 12-7 (6)(11); Art. 14 is now partly defined.
- 旧 6-4「ほかの種類」は 6-6 とし、Web ページ・コマンドラインのツール・スクリプトだけを未定に残した。第6条の表に「文書」の行と、画面を持つものに 6-5 を当てはめることを足した。1 (2) と第15条の未定の項目の表を合わせ、「Identity から確かめ方の条を移す」を表から外した。
  Former 6-4 becomes 6-6; the Art. 6 table, 1 (2), and the table of undecided items are updated.
- 10-4 のひな形を写せるよう、コードの枠の書式を足した(文字と背景は本文と同じ ink × paper)。
  A code-block style is added for the templates.

移した条の対応(Identity 12-7 (15)) / Mapping of moved articles:

| Identity 4.21.0 | 移り先 |
| :--- | :--- |
| 7-7 の「公開する前に確認する」ことと、確認の記録 | 品質確認規定 6-5。(a)〜(k) の条件は 7-7 に残した |
| 9-5 のアクセシビリティの確認記録のひな形 | 品質確認規定 10-4 (1) |
| 8-9 (1) の確かめ方、(5) 配る環境での確かめ方と記録、(6) 置き場所 | 品質確認規定 6-4 (1)〜(5)。8-9 (1)(5)(6) には要点と移り先を残した |
| MARKDOWN-CHECKLIST 4 節(描画と表示を確かめる) | 品質確認規定 6-4 (3) |
| MARKDOWN-CHECKLIST 7 節(確認記録のひな形) | 品質確認規定 10-4 (2) |
| 12-7 (6) 版の確かめ方 | 品質確認規定 14-1 (1) |
| 12-7 (11) のうち、Actions による自動化とプルリクエストでの確認 | 品質確認規定 14-1 (2)(3) |

## 0.8.0 — 2026-11-03

appAutoTester と mdEditor(1.0.21〜1.0.22)で実際に使っている決まりを取り入れた。
Practices in use in appAutoTester and mdEditor (1.0.21 to 1.0.22) adopted.

- 本規定を Web で公開した(https://5garashi.github.io/5garashi-quality/)。正式版(1.0.0)までは草案とし、改版で内容が変わる。第15条 (2)、表紙、README を合わせた。未定の項目の期限「正式版(1.0.0)の公開まで」を「正式版(1.0.0)まで」とし、Identity から確かめ方の条を移すことを未定の項目(次の版)に加えた。README からこの PC のフォルダーの場所を外した。公開のリポジトリ(5garashi/5garashi-quality)は本版から始め、0.7.0 までのコミットの履歴は非公開のリポジトリに残した。
  The Quality Rules are now published on the web as a draft until 1.0.0; Art. 15 (2), the cover, and the README are updated. The public repository starts at this version; the commit history up to 0.7.0 is kept in a private repository.
- 4-2「変更に応じて流す試験を選ぶ」を新設:差分から呼び出し元と共有の状態を操作の入口までたどって範囲を決め、起動の試験を必ず加える。たどれない・共通の部分・削除や改名・判断できないときは全件とし、この条件は製品ごとの表に優先する。対応する試験がないときは、全件に加えて試験を足し、全件の合格だけで変更を確かめたことにしない。範囲の表は製品ごとに決める。製品の操作に関わらない試験の道具の変更は自己試験で確かめてよい。流す前に範囲を伝え、長い全件は承認を得てから流す。流した範囲を必ず書く。範囲を絞った版も、出す前に全件を1回流し、省かない。全件になる変更を絞るのは、決める人がその差分を認めたときだけ(一回限り)。繰り返すときは全件の条件そのものを見直す。appAutoTester の「テストの範囲の決め方」による。
  New 4-2 "Choose the tests to run for each change": trace callers and shared state to the user's entry points; run everything when tracing fails or shared parts change; per-product tables; self-tests for tooling that does not drive the product; announce the scope before running; ask before a long full run; always state the scope; a full run before every release is never skipped; one-off exceptions only with explicit approval.
- 3-8 (4) 水平展開を新設:不具合を直したら、原因を一般化し、コードと入力の両方で同じ形を探し、直したものも直さないと決めたものも例を集めた試験(コーパス)に足し、探した結果を報告する。8 (3) から参照した。mdEditor の `test_written_elsewhere.py` による。
  New 3-8 (4) on extending each fix to the same kind of defect, with a corpus test that keeps fixed and deliberately unfixed examples; 8 (3) refers to it.
- 3-10「受け入れる入力の範囲」を新設:意図どおりに扱う入力の範囲を根拠とともに README に書き、どこでも正しくない書き方と、前の版の不具合で崩れて保存されたものには合わせない。範囲の外の報告は理由とともに記録する。自動の修正と形式の変換が、正しい入力の意味と仕様で保つと定めた情報を壊さないことを試験で確かめる。mdEditor の「対応する書き方の方針」による。
  New 3-10 "Range of accepted input": state the supported input with its basis, do not accommodate input that is correct nowhere or saved broken by an earlier bug, and test that automatic fixes never break correct input.
- 9-2 (9)「試験を減らすとき」を新設:消す・まとめる・skip・ケースを減らすことも記録の対象とし、原因を確かめずに緩めない、今の出力に合わせるだけの期待値の変更をしない、代わりの確認がなければ減らさない、人の目に置き換えたら結果を記録する。第12条 (3) から参照し、機能の変更に伴う試験の整理は AI に判断させてよいとした。appAutoTester の「テストの追加・変更・削除」による。
  New 9-2 (9) on reducing tests: record it, never loosen a failing test before finding the cause, never change expectations just to match output, never remove a check without a replacement; Art. 12 (3) lets the AI maintain tests within these limits.
- 第11条 (9) を新設:製品ごとに TESTING.md を置き、変える前に読む。範囲の表や件数は書き写さず、正本を参照する。第12条 (6)(7) を新設:判断できないときや共通の部品・環境を守る仕組みを変えるときは先に確かめさせる。TESTING.md を読ませ、範囲を決めて伝えてから流させる。
  New Art. 11 (9): a TESTING.md per product that points to the source of the rules; new Art. 12 (6)(7) on what the AI must confirm first and on choosing and announcing the scope.
- 6-1 に「画面の変更」(決めた幅・全言語・夜の配色で写して目で確かめ、色を変えたら比を測る)と「訳」(項目、差し込む値の名前・回数・書式、混じる文字、画面の名前を機械で確かめる)の行、13-1 に「訳」(別の人か AI が意味を見る。依頼文はそれだけで読めるように書く)の行を足した。
  6-1 adds rows for screen changes and translations; 13-1 adds translation review with a self-contained request.
- 10-3 (6) を定めた:出した版ごとの記録(`records/<製品>-<版>.md`)を版の管理の下に残し、件数・結果・未実施・判断を載せる(件数と結果は報告書から自動で作れるようにすることを目指す)。画面写真つきの報告書は git に入れなくてよいが、記録から場所を引けるようにする。公開の場に置くかは第14条で定める。未定の項目の表から外した。
  10-3 (6) is now defined: a per-release record kept under version control, pointing to the larger reports; the table of undecided items is updated.
- 第15条 (5) を「実情に合わせて見直す」に改め、Identity 1-4 (3)(製品を作る・直す・出すたびに、品質と効率を基準に見直し、減らすことも必ず検討する)を本規定にも当てはめた。(6) を新設し、Identity 1-4 (2) に加えて第5条と安全に関わる決まりを、効率だけを理由に減らさないものとした。旧 (6) は (7) とし、測るものに決まりを守る手間を加えた。旧 (7) は (8)。(9) を新設:製品は従う本規定と Identity の版を README に書き、参照は次の改版のときに直す。本規定自身も README に従う Identity の版を書く。節を移す・消すときは CHANGELOG に旧と新の対応を書く(Identity 4.21.0 の 12-7 (14)(15))。手すりの参照先を Identity 1-3 から 1-4 に直した。
  Art. 15 (5) applies Identity 1-4 (3) (review by quality and efficiency, always consider reducing); new (6) adds Art. 5 and safety rules to those never reduced for efficiency alone; former (6) becomes (7) and measures effort; former (7) becomes (8); new (9) on conformance versions and old-to-new mapping. The handrail reference is corrected from Identity 1-3 to 1-4.
- README に「準拠 / Conforms to: Design Office Identity 4.21.0」を足した。
  README states the Identity version this document follows.
- 5 (8) に、途中で止めても後片付けを飛ばさないことを足した。4-1 (3)、3-6、第5条に実例を足した。
- 別の AI によるレビュー(2026-11-03)の指摘を反映した:第15条の番号の振り直しの案内(CHANGELOG の対応で足りるとした)、3-10 (4) の「書き換えない」を「壊さない」に、4-2 の全件の条件と表の優先順位、対応する試験がないとき、README の準拠の版、6-1「訳」の差し込む値、第15条と Identity 1-4 の重なり、10-3 (6) の書き写し。
  Findings from an independent AI review (2026-11-03) applied.

## 0.7.0 — 2026-10-17

- 3-9 (2) を「復帰で勝手に動かない」から「安全な範囲で自動で復帰し、使用を続けられるようにする」に改めた。自動で戻るのは、異常の原因がなくなったことを自己診断と状態の読み直しで確かめ、戻る先の動作の条件がそろい、当てはまる法令や規格が使う人の操作による再開を求めていないときに限る。自動での復帰の回数と間隔に上限を設け、上限を超えたら安全な状態で止まって知らせる。部品の故障など自然には解消しない異常からは戻らない。復帰とその原因を記録する。6-3 の「電源」の行を合わせた。
  3-9 (2) now favors safe automatic recovery to keep the product in use: resume only when the cause is confirmed cleared, the conditions to resume hold, and no applicable standard requires a manual restart; limit retries, stop safely and notify beyond the limit, never auto-recover from faults that do not clear by themselves, and record each recovery. The power row of 6-3 is aligned.

## 0.6.0 — 2026-10-14

- 4-1 (2)「測定系が正しいことを確かめる(測る前の校正)」を新設:測る前に、ゼロ(測る対象のない状態)と値の分かっている基準を、実際と同じ測定系・設定で測り、ずれや雑音が許容の範囲を超えたら測り始めない。ハードウェアの例(オシロスコープで 0 V・無波形を必ず確かめ、基準信号で倍率・時間軸・極性を確かめる)と、ソフトウェアの例(何もないときに0件、わざと1件起こしたときに1件を捉える、道具そのものの時間を先に測る)を示した。
  New 4-1 (2) "Verify the measurement system before measuring": measure zero and a known reference with the same setup first, and do not start if offset or noise exceeds the limit; hardware (0 V, no waveform on an oscilloscope) and software (zero events when idle, exactly one when one is injected) examples.
- 4-1 (4):確かめ直すとき(測定系の設定や接続を変えたとき、長い試験の途中と終わり、結果が予測と合わないとき)を新設。旧 (2) は (3)、旧 (3) は (5) へ。6-2 (2) を 4-1 (2) の実機での具体とした。
  New 4-1 (4) on when to re-verify; former (2) and (3) become (3) and (5); 6-2 (2) is now the hardware detail of 4-1 (2).

## 0.5.0 — 2026-10-14

外部のレビュー(2026-10-14)の10件の提案を反映した。
Ten proposals from an external review (2026-10-14) applied.

- 9-2 (1):出してよい条件を、第14条ができるまでの暫定として補った(自動の試験に1回合格、必須の項目がすべて判定済み、重大な不合格・異常・判定不能が残っていない、未実施・逸脱・通常以下の不合格を残すときは判断した人・日付・理由を記録)。
  9-2 (1): interim release conditions until Art. 14 is defined.
- 9-2 (7):人による確認の記録は必須としないまま、自動にできない項目(画面読み上げソフト、フォーカスの順序、言葉の分かりやすさなど)は「未実施」として必ず挙げ、出荷のときの判断者を残す。第4条と第13条の記述をそろえた。
  9-2 (7): human checks stay optional, but unautomatable items are always listed as not tested with the release decision-maker recorded; Arts. 4 and 13 aligned.
- 9-1:「判定不能」を追加。9-3「重さ(重大度)」を新設し(重大・通常・軽微)、試験の優先順位、出してよいかの判断、レビューの指摘(13-4)に共通で使う。9-2 (3):合否が揺れるときは製品側の競合状態の可能性も調べる。
  9-1 adds "undecidable"; new 9-3 severity scale shared by prioritization, release decisions, and review findings; 9-2 (3) also considers race conditions in the product.
- 第4条:「結合」の層を追加(層の番号を振り直し)。第5条:分けた場所での試験を原則とし、共有の設定の変更は例外として、控え・排他・戻せないときの処置を定めた(項目の番号を振り直し)。
  Art. 4 adds an integration layer; Art. 5 makes isolation the rule and shared-setting changes an exception with backup, exclusivity, and failure handling.
- 第6条:作るものの種類ごとに当てはめる節の表。6-2 (9):不確かさの幅が限界をまたぐときの扱いを試験前に決める。
  Art. 6: applicability table; 6-2 (9): decide in advance how to judge results near limits.
- 第7条 (2)(6)(7):1回通すだけでは順序と並行処理を網羅できない限界、重さによる優先順位、構成の組み合わせの絞り方(ペアワイズを目安、外した理由を記録)。
  Art. 7: limits of single-pass coverage, severity-based priority, and pairwise narrowing with recorded exclusions.
- 第8条:「とても大きい」などを仕様の上限とその前後の値に改め、8-1「試験を設計する技法」(境界値、同値分割、決定表、状態遷移、探索的な試験)を新設。
  Art. 8: reproducible limit values; new 8-1 on test design techniques.
- 第15条 (6)(7):改訂の効果の測り方と、未定の項目の期限・担当の表。
  Art. 15: measures of revision effectiveness and deadlines and owners for open items.

## 0.4.0 — 2026-10-14

対象を電子回路・基板・機器・ファームウェアに広げた。
Scope widened to electronic circuits, boards, equipment, and firmware.

- 第1条 (1)(4)(5):作るものに電子回路・機器・ファームウェアを加え、型式と版(回路図・基板・部品表・ファームウェア)で識別すること、法令や規格が試験を定めるときはその要求を優先し、本規定は規格が定めない部分を補うことを定めた。
  Art. 1: hardware and firmware in scope, identified by model and revisions; legal and standard requirements take precedence, and these rules fill the gaps.
- 第3条 3-9「電子回路・機器・ファームウェアの作りこみ」を新設:安全側に倒れる、単一の故障で危険にならない、復帰で勝手に動かない、定格の余裕、保護の協調、測れる作り、識別、ファームウェアの書き換え失敗からの復帰。
  New 3-9: fail safe, single-fault safety, no unintended restart, derating, protection coordination, testability, identification, firmware update recovery.
- 第4条:試験の層に「実機」を追加。第6条 6-3「電子回路・機器で必ず確かめる項目」を新設(識別、基本の動作、電源、保護、単一の故障、絶縁と接地、温度、EMC、環境と機械、誤使用と断線、ファームウェア、表示と説明書、出荷の検査)。旧 6-3 は 6-4 へ。
  Art. 4 adds a hardware layer; new 6-3 lists required hardware checks; former 6-3 becomes 6-4.
- 第8条:実機のいじわる試験(逆接続、半端な差し込み、断線、停電と復電、電源の上下限、静電気、書き換え中の電源断など)と、中止の条件を決めてから行うこと。
  Art. 8: adversarial tests for hardware, run only with stop conditions set.
- 第11条を「試験コードと手順書の書き方」に改め、(8) 実機の手順書を追加。第13条:回路図・基板・部品表のレビューの観点。第14条:出荷の検査を項目に追加。
  Art. 11 renamed and gains (8) hardware test procedures; Art. 13 adds schematic, board, and BOM review; Art. 14 lists production inspection.

## 0.3.0 — 2026-10-14

電気製品の認証試験で使われている試験データ管理の実務から、ソフトウェアにも通じる考え方を取り入れた。
Practices from test-data management for electrical product certification, generalized for software as well.

- 第2条:先に予測して結果と比べる(一致しても並べて残す、不一致ならすぐに合否を決めない)、一度に一つだけ変える、再現しなかった異常も記録を消さない。
  Art. 2: predict before testing and compare; change one thing at a time; keep records of anomalies that did not recur.
- 第4条 4-1「試験の前に確かめること」を新設:試験する物を実物で照合する、試験の道具そのものを結果の分かっている入力で確かめる、共通の条件を変えたときに影響する試験を記録する。
  New 4-1: verify the item under test against the actual build, verify the test tooling with known inputs, record the impact of changes to shared conditions.
- 第5条 (8):ヒヤリハット(被害のなかった危うい事象)を、人を責めずに記録する。
  Art. 5 (8): record near misses, blame-free.
- 第6条 6-2「実機・測定を伴う試験」を新設(測定点の番号、測定系の事前確認、設定と生データの保存、有効桁、時刻合わせ、安全、試験前後の機能確認)。旧 6-2 は 6-3 へ。
  New 6-2 for hardware and measurement tests; former 6-2 becomes 6-3.
- 第7条 (7)〜(9):構成の組み合わせ、適用しない組み合わせも根拠付きで残す、試験の名前の単位で完了扱いにしない。
  Art. 7 (7)-(9): configuration combinations, keep non-applicable rows with reasons, no completion by test-group name.
- 第9条を 9-1「判定の区分と用語」(合格・不合格・未実施・適用外、異常、逸脱)と 9-2「出してよい条件と記録」に分け、結果を消さない・最良の回だけを選ばない・異常のデータを分けるを追加。
  Art. 9 split into 9-1 (verdicts P/F/N/T/N/A, anomaly, deviation) and 9-2 (release condition and records), adding: never delete results, never pick only the best run, keep anomaly data separate.
- 第10条を 10-1〜10-3 に分け、略語、共通の情報の置き方、要求事項との対応表、試験の番号・実施番号・やり直しの番号(R1)・証跡の名前・ひな形と結果の分け方・空のフォルダーの保持を追加。
  Art. 10 split into 10-1 to 10-3, adding abbreviations, shared records, a requirements traceability table, and naming of runs, reruns, evidence, and templates.
- 第11条 (7):規格の値と社内の管理値を区別し、確かめられない値を推定で埋めない。第13条:試験報告書と証跡の照査を観点に追加。第14条:提出物のチェックリストを項目に追加。
  Art. 11 (7): separate standard values from internal limits and never fill unknown values with guesses. Art. 13 adds review of reports and evidence. Art. 14 lists a submission checklist.

## 0.2.0 — 2026-10-13

- 第13条「レビュー」を定めた:対象と観点(コード・試験コード・文書・画面)、いつ行うか(変更ごと・出す前)、誰が行うか(書いた人以外の目。見る人がいないときは AI を使ってよいが、書いた AI 自身に見させて終わりにしない。AI の指摘には根拠と確かさを付けさせ、最終の判断は人)、指摘の書き方(重大・通常・提案)と扱い・記録。
  Art. 13 "Review" defined: what and what for, when, who (another pair of eyes; AI may stand in, but never the authoring AI alone; AI findings carry evidence and certainty, and a person decides), how to write findings, and how to answer and record them.
- 第15条:本文のライセンスを CC BY-ND 4.0 に確定した。当面は日本語だけで作る。
  Art. 15: the text is licensed CC BY-ND 4.0; Japanese only for now.

## 0.1.0 — 2026-10-13

最初の草案。非公開。
First draft, not public.

- 第1〜2条:目的と範囲、基本の考え方(人と同じ操作で確かめる、使う人の環境を壊さない、状態を待つ、まず試験を疑う、合格の範囲を示す、試験はコードと一緒に作る、安易に止めない)。
  Arts. 1-2: purpose, scope, and principles.
- 第3条「作りこみ」:エラー処理、エラーログとイベントログ、状態とイベントの設計、keepAlive と watchDog、状態がずれたときの再同期、サービスの継続、ヘルプ、試験コードを一緒に作ること。
  Art. 3 "Building quality in": error handling, error and event logs, states and events, keepAlive and watchDog, resynchronization, continuity, help, and writing tests alongside code.
- 第4〜12条:試験の層、使う人の環境を守る決まり、必ず確かめる項目(デスクトップアプリ)、状態とイベントの総当たり、いじわる試験、合否と記録(自動の試験に1回合格。人による確認は任意で、行ったら記録)、試験報告書、試験コードの書き方、AI エージェントに任せるとき。
  Arts. 4-12: test layers, protecting the user's environment, required checks for desktop apps, state-event coverage, adversarial tests, pass criteria and records (one passing run; human checks optional but recorded), reports, test code, and AI agents.
- 第13条レビュー・第14条リリース手順は項目だけを挙げた(未定)。
  Arts. 13 (review) and 14 (release) list topics only (to be decided).
- 第15条:版の管理、公開(完成まで非公開)、英語版とライセンス(未定)。
  Art. 15: versioning, publication (private until complete), English edition and license (to be decided).
