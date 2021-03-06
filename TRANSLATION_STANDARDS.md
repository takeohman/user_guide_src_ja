# ユーザガイド日本語版執筆基準

## ファイル

* 改行コードは本家同様 LF を使う。変更しない。誤って LF 以外のコードが使われている場合は、改行コードのみを修正してコミットするか revert する
* 文字コードは UTF-8
* 必ず原文ファイルと行数を合わせる（ただし、日本語の単語の途中では改行しない）

## コミット

* 原則、1ファイルごとにコミットする
* 「追加された文章の翻訳」と「既存の翻訳の修正」は分けてコミットすることが望ましい
* 用語の統一のような複数ファイルにまたがる変更は、複数ファイルをまとめてコミットする

## 表記

* 句点は「、」読点は「。」を使う
* 中黒「・」は使わない
* 英数字は半角を使う
* ASCII にある記号は半角を使う。ただし、地の文では丸括弧「（」「）」と「！」「？」は全角を使う
* 英単語の前後は半角スペースを入れる
  1. この式は FALSE として評価されます
  2. 初回アクセス時には、Web ページが読み込まれます（※句読点の後ろには半角スペースを入れない）
  3. ユーザエージェント（Web ブラウザ）を返します（※全角丸括弧の内側には半角スペースを入れない）
* 訳注は以下のフォーマットで入れる
```
 [ 訳注: 注意書き ]
```

## 表記の統一

|使用する表記    |使用しない表記|注                                                    |
|----------------|--------------|------------------------------------------------------|
|たとえば        |例えば        |                                                      |
|おすすめ        |お勧め、お薦め|                                                      |
|すでに          |既に          |                                                      |
|すべて          |全て          |                                                      |
|なぜ            |何故          |                                                      |
|かわりに        |代わりに      |                                                      |
|Web             |web           |原文では「web」ですが、日本語訳では「Web」で統一します|
|フォームヘルパー|Form ヘルパー |                                                      |
|オプション      |オプショナル  |                                                      |

## 訳語の統一

|英語           |日本語訳                                                      |
|---------------|--------------------------------------------------------------|
|function       |オブジェクトでは「メソッド」、オブジェクトでない場合は「関数」|
|common function|共通関数                                                      |
|first parameter|第1引数                                                       |
|parenthesis    |丸括弧                                                        |
|bracket        |角括弧                                                        |
|brace          |波括弧                                                        |

## 長音の統一

* 長音記号（長音符号あるいは音引き）については、原則として “3音ルール” を使用する。
  * 3音ルールについて: [技術文書での長音記号の扱い方 － 実践テクニカルライティングセミナー](http://www.yamanouchi-yri.com/yrihp/techwrt-2-4s/t-2-4s07fa-1.htm)

紛らわしい、あるいは例外的に 3音ルールを適用しない場合は、以下にその例を記述します。

|使用する表記|使用しない表記|注          |
|------------|--------------|------------|
|ユーザ      |ユーザー      |            |
|ヘルパー    |ヘルパ        |例外的な使用|
|ヘッダ      |ヘッダー      |            |

## 外部Webページへのリンク

* 日本語以外の外部ページへのリンクについては、公式の日本語訳ページへのリンクに改変する。
公式の日本語訳ページが無い場合は、リンクは改変せず原文のままにする。

```
<a href="http://www.php.net/manual/en/intro.pdo.php" target="_blank">PDO</a>
↓
<a href="http://www.php.net/manual/ja/intro.pdo.php" target="_blank">PDO</a>
```
