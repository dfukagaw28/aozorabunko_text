# テキストデータの前処理について

*   [青空文庫・外字注記辞書【第八版】](https://www.aozora.gr.jp/gaiji_chuki/)

## 外字を Unicode に変換する

*   https://github.com/dfukagaw28/aozorabunko_text/tree/feature/scripts の `preprocess_replace_gaiji.ipynb` を参照
*   `gaiji_list_0.csv` は `※※` で始まる例学的パターン（手作業による処理）
*   `※［＃` で始まるパターンのについて，
    *   `gaiji_list_1.csv` は `第X水準XX-XX-XX` を含むパターン
    *   `gaiji_list_2.csv` は `U+XXXX` を含むパターン
    *   `gaiji_list_3.csv` は `XX-XX-XX` を含むパターンのうち，例学的パターン（手作業による処理）
        *   JIS 面区点コードでなく，「ページ-段数-行数」を表しているかもしれない。
        *   `「未」の「二」に代えて「三」` は `來` (U+4F86) の旧字体だが，Unicode には存在しないらしい。
        *   文字情報基盤検索システムによれば，対応するUCSが `耒` (U+8012) となっているが，この割り当ては誤りの可能性が高い（青空文庫の入力者もそのように指定されている）
            *   https://moji.or.jp/mojikibansearch/info?MJ%E6%96%87%E5%AD%97%E5%9B%B3%E5%BD%A2%E5%90%8D=MJ020768
            *   https://www.aozora.gr.jp/cards/000048/files/43464_47395.html
            *   https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q14109760884 未来の「未」と言う字は横棒２本ですが、横棒が３本の漢字は何と読みますか？
            *   https://mojiura.hatenadiary.org/entry/20070902/p1 横三本の「来」
        *   テキスト分析を目的とする場合，「來」や「来」に置き換えておくのがよさそう。
        *   `糸＋（舎－口）` も適切な漢字が見つからない。文脈から `経` があてはまりそう。
            *   https://www.aozora.gr.jp/cards/000048/card43464.html
        *   `二点しんにょう＋麦` は
            *   https://www.aozora.gr.jp/cards/000048/card43464.html 南部 修太郎『夢』
            *   https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q136981813 「しんにょう」に「麦」という字は何と読ませますか？
        *   `討／貝` は `𧏛` の異体字だと思われるが，登場するのは青空文庫注記の中であるから，前処理の後のステップで消えるため，気にしない。
        *   `＃変体仮名え` `＃こと` は，そのままひらがなを使用した（底本にあたることができればよいが・・・）。

## 冒頭・末尾のメタデータを削除する

*   https://github.com/dfukagaw28/aozorabunko_text/tree/feature/scripts
    *   いくつか手動で調整したのち，自動的に処理
    *   `preproceess_remove_header.ipynb` を参照
    *   `preproceess_remove_footer.ipynb` を参照
