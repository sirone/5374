#多摩市版 5374.jp 解説

5374.jp は CfK, [Code for Kanazawa](http://www.codeforkanazawa.org/) によって開発されたゴミ問題解決プロジェクトです:thumbsup:.

このデータはその東京都多摩市版となります.

## 使い方
-----
同梱物は幾つかありますが、順を追って説明いたします.

    5374.jp
     ┗　webroot
     　　　┗ data
     　　　┗ imgs
     　　　┗ js
     　　　┗ index.html
     ┗　5374多摩市データ.xlsm
     ┗　README.md
     
### 5374.jp/webroot 以下
----
このフォルダは web 上で公開するアプリに直接上書きしてください.

* data/
    * 多摩市用の CSV データ一式.
* imgs/
    * SVG 画像一式.
        * 2014/12/10時点で、Android + Chrome の実機から一部の SVG が切れて表示される現象を確認しています by sirone.
* js/
    * CSV を Excel で吐き出した際、1セル内の記述が複数行になった場合、JS 側が対応できていなかったので、その修正済み script.js ファイル.
    * 多摩市は細かくゴミ分けの分類があるため、それに対応するための setting.js ファイル.
* index.html
    * Google Analytics のコードが仕込まれていたので、それを削除したもの.

実際に運用するときのイメージが 5374.jp の説明を読んでもいまいち分からないのですが
単体で置く場合は上記全てが必要になります. (特に JS ファイル必須)

### 5374多摩市データ.xlsm ファイル
----
なぜマクロが必要なのかと言うと、これからも保守を続けていく CSV を、いちいち手打ちでやるわけにいかなかったからです.

今後小学生でも取り組めるような操作方法にするため、VBA マクロでボタンを取り付けました.

エクセルは中を見てもらえばわかる通り、各 CSV を吐き出すために CSV の名前でシートを整えてあります.

Excel には CSV で出力する機能が元から備わっていますが、__script.js が CSV のエンコードを UTF-8 と想定して動作していた__ため、VBA マクロとして UTF-8 の CSV 書き出しを実装しました.

### README.md
----
いわずもがなこのファイルです:wink:

Markdown 形式ですので、それに対応したエディタでご覧ください.

----
Written by [Shirone Takanashi.](https://github.com/sirone)

5374.jp "Code for Kanazawa" All right reserved.
