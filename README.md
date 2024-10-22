# aozorabunko_text (UTF8版)

青空文庫( https://www.aozora.gr.jp )のサーバ内にある青空文庫形式のテキストのみをテキスト形式のまま集めたものです。

*   主な元データは [aozorahack/aozorabunko_text](https://github.com/aozorahack/aozorabunko_text) です。
*   不足分（最近追加されたもの）を [aozorabunko/aozorabunko](https://github.com/aozorabunko/aozorabunko) から補いました。
*   1つの作品（作品Noが同一のもの）に対して複数の版のテキストデータがある場合は 1 つだけ（原則として最新のもの）を残して他を削除しました。
*   青空文庫の公式テキストデータは文字エンコーディングに Shift-JIS を採用していますが，より扱いやすい UTF-8 に変換しました。

## ダウンロード

[Download ZIP](https://github.com/dfukagaw28/aozorabunko_text/archive/refs/heads/utf8.zip) (約280MB)

zip形式のファイルで欲しい場合、上記からダウンロードできます。
なお、テキストファイルは全てcardsディレクトリ内にあります。それ以外は無視してください。

gitレポジトリの取得については、ふつうのgithub repoなので git pullで持ってきてもらえばいいのですが、履歴不要で最新版だけ欲しい場合は以下のコマンドの方が早いはずです。

```console
$ git clone --depth 1 https://github.com/dfukagaw28/aozorabunko_text.git
```

### 個別のテキストファイルへのアクセス

個別のファイルには、`https://github.com/dfukagaw28/aozorabunko_text/raw/refs/heads/utf8/cards/000081/files/45630_txt_23610/45630_txt_23610.txt`のようなURLでアクセスできます。

※ zip内のテキストファイルはタイトルに合わせたファイル名が命名されているのですが、このレポジトリではzipファイル名に合わせたファイル名にしています。
例えば、`cards/000005/files/53194_ruby_44732.zip`内のテキストなら`cards/000005/files/53194_ruby_44732/53194_ruby_44732.txt`というパスになります。

異なるファイル名にしているのは、元のテキストファイル名は「作家別作品一覧CSV」などにも書かれておらず、確認するにはzipファイルの中身を見ないといけないためです。

## 動作のしくみ

頻繁に更新する予定はありません。最新のテキストデータは公式データセット [aozorabunko/aozorabunko](https://github.com/aozorabunko/aozorabunko) を参照してください。

## 権利関係

cardsディレクトリ内のファイルについては、[「青空文庫収録ファイルの取り扱い規準」](https://www.aozora.gr.jp/guide/kijyunn.html)の元でご利用ください。

著作権保護期間が終了しておらず、クリエイティブ・コモンズ・ライセンス等による許諾の元で再配布されているファイルも含まれています。ご注意ください。
