# NOTICE — Kanseki Repository 底本に関する表示

本リポジトリのテキストデータは、Kanseki Repository（漢籍リポジトリ、Kanripo）が公開するデータを底本とする再加工物である。CC BY-SA 4.0の条件（帰属表示・改変明示・同一ライセンス継承）に基づき、以下の通り出典と加工内容を表示する。

## 1. 底本の出典と版本情報

| 項目 | 内容 |
|---|---|
| 底本 | Kanseki Repository（1文献1リポジトリ構成） |
| 配布元 | https://github.com/kanripo |
| 採用ブランチ | master（全件。ブランチ名と取得時コミットSHAは catalog.csv の witness・commit 列に記録） |
| 分類・書誌の典拠 | kanripo/KR-Catalog（コミット 781711923e2ce6f82f6dacfb8576cd80774b7ec0）の KR/KR2a.txt〜KR2o.txt |
| 取得日 | 2026-10-07 |
| 収録範囲 | KR2史部（正史類・編年類・紀事本末類・別史類・雜史類・詔令奏議類・傳記類・史鈔類・載記類・時令類・地理類・職官類・政書類・目錄類・史評類）の目録581件のうち、リポジトリのある579件 |

masterブランチの底本は、各本文ファイル冒頭のプロパティ（BASEEDITION）によれば、四庫全書文淵閣本（WYG）530件、四部叢刊（SBCK）47件、tls 1件、MJSY 1件である（catalog.csv の baseedition 列参照）。KR-Catalog の版本欄が WYG であっても master の底本が SBCK である文献が35件あり、catalog.csv の review_flag 列に記した。

底本表示が tls または MJSY の2件は次の通りである。いずれも標点つきの本文で、ほかの577件（底本表示が WYG・SBCK のもの。無標点の本文）とは性質が異なる。

| ID | 題名（目録） | 底本表示 | 内容 |
|---|---|---|---|
| KR2a0001 | 史記 | tls | TLS 由来の本文。現代の標点と見出しを含む（目録の版本欄は WYG） |
| KR2b0041 | 十八史略 | MJSY | 句点つきの本文と注。冒頭に明治四十三年七月付の日本語の解題（重野安繹の署名）がある。底本は上流の Readme の表示による（版本欄に「MJSY」「明治書院」とある） |

この2件のリポジトリ（master ブランチのファイル、KR2a0001 の tls ブランチのファイル、およびGitHub上のリポジトリのページ）には、個別のライセンス表示・権利表示は無かった（2026-10-07確認）。

## 2. 底本のライセンス

Kanseki Repositoryは、そのコンテンツを **CC BY-SA 4.0**（Creative Commons 表示–継承 4.0 国際）で公開している。典拠は以下の通り（2026-10-07確認）。

- GitHub組織プロフィール（https://github.com/kanripo ）:「Comprehensive collection of premodern Chinese texts. Licensed as CC BY SA 4.0.」

なお、収録テキストの原典（史書とその注釈書など）は著作権保護期間を満了した公有文献であり、CC BY-SA 4.0が及ぶのはKanripoによる翻刻・校正・構造化等の作成部分である。

## 3. 本リポジトリでの加工内容

- mandoku形式のメタデータ行（行頭が「#」の行）・画像リンクの除去（プレーンテキスト化）
- 頁マーカー `<pb:...>` の【　】形式への変換・保持
- 原本行末記号「¶」の除去と物理行の連結
- 巻ファイルの作品単位への統合、書誌情報の catalog.csv への集約
- 本文の文字そのものには改変を加えていない（異体字・外字参照・上流に残る記法もそのまま）

## 4. 本リポジトリのライセンス

底本の条件を継承し、CC BY-SA 4.0 で公開する。ライセンス全文は同梱の `LICENSE` を参照。

- ライセンス正文: https://creativecommons.org/licenses/by-sa/4.0/legalcode
- Kanseki Repository: https://github.com/kanripo
