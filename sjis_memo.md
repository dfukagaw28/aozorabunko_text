# 1バイト制御文字

*   水平タブ `0x09`
*   改行 LF `0x0a`
*   復帰 CR `0x0d`
*   改頁 FF `0x0c`
    *   https://www.aozora.gr.jp/cards/000125/files/667_42459.html
    *   `しばらく僕を静かに考えさせて下さい」` の直後が `0d 0a 0c 0d 0a`

# NEC 特殊文字

*   `Ⅰ` 8754 U+2160

# IBM 拡張文字

*   `ⅹ` FA49 U+2179
    *   [マルサス『人口論』](https://www.aozora.gr.jp/cards/001149/card43551.html) ギリシャ数字（他の箇所は ASCII の `x`）
*   `厓` FA8D U+5393
    *   [芥川龍之介『わが家の古玩』](https://www.aozora.gr.jp/cards/000879/card3798.html) `仙厓作（せんがいさく）鐘鬼図（しようきづ）一幀`
*   `賴` FBAE U+8CF4
    *   [ロラン ロマン『ジャン・クリストフ』](https://www.aozora.gr.jp/cards/001093/card42596.html) `僕は彼らのような不正な方法に賴ることが厭なばかりでなく`

# デコード不可能な文字

*   EB81
    *   [穂積 陳重『法窓夜話』](https://www.aozora.gr.jp/cards/000301/card1872.html) `ユ、モ埃エ伊イ阿オ兪ユ頭ノ語ニシテ、` と `アル者ハ、匐べ以下ノ単字頭ト知ルベシ` との間の 2 バイト。
    *   JIS X 0213 だと `EB 81` は「栱」だが， JIS X 0213:2004 は Shift-JIS (CP932) と互換性がない。文脈を考えても，あてはまらない。
    *   HTML ファイルを参考に修正した。
    *   詳細は [dfukagaw28/ColabNotebooks/青空文庫『法窓夜話』のテキストデータを利用する.ipynb](https://github.com/dfukagaw28/ColabNotebooks/blob/main/%E9%9D%92%E7%A9%BA%E6%96%87%E5%BA%AB%E3%80%8E%E6%B3%95%E7%AA%93%E5%A4%9C%E8%A9%B1%E3%80%8F%E3%81%AE%E3%83%86%E3%82%AD%E3%82%B9%E3%83%88%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E5%88%A9%E7%94%A8%E3%81%99%E3%82%8B.ipynb) を参照してください。
