# readtsv
readtsv - easy tsv file viewer/converter
====

Tab区切りテキストファイル（TSVファイル）の内容確認および簡単な整形に使えるツール

A tool to check content or to convert tsv files.

## 概要 / Summary
tabは「見えない」ため、tsvファイルの中身を確認したいときに不便を感じることがあります。そこで、とりあえずtabを"|"に置き換えて表示したいと考えて組んだワンライナーが本ツールのルーツです。これをスクリプトファイルに仕立て、少しづつ機能を追加しながら、気が付けば10年愛用していました。折角なのでgithubで公開しようと思い立った次第です。

Since tabs are "invisible", I always feel inconvenience to check the contents of tsv files.  One day I made a one-liner to display tsv files by replacing tab with "|". Soon I made a small perl script file based on this one-liner, and have added functions into it little by little for 10 years. I believe that this tool has been grown up to useful for everyone handling tsv files. Therefore I decided to publish it on github.

今では、次のようなことができます。
* 指定列のみを抜き出して表示
* 複行レコードとして出力
* csvとして出力
* html tableとして出力

## 使用例 / Example
readtsv input.tsv

readtsv -k 1,2 input.tsv

readtsv -m input.tsv

readtsv --html input.tsv

## 解説 / Description

readtsv [オプション] 入力元TSVファイル

パラメータを一切指定しない場合、標準入力からデータを読み取り、タブ文字を"|"に変換して標準出力に出力します。


### オプション / Options

 * -g           : postpone that the input is from grep of multiple files
 * -html        : output simple html text
 * -htmlopt 1   : html table options
 * -ifs ','     : specify field separator on input
 * -k a,b,c,... : display only designated fields
 * -multi       : display in muliple line format: one column -> one line
 * -m           : same as -multi
 * -n           : display the number of field, line No., file name
 * -s ','       : specify field separator on output
 * -sort 1n2dn  : sort option
 * -t           : treat first line as field names
 * -v           : display field names when -f is set

## インストール / Install
本スクリプトを適当なディレクトリに置いてください。perl5がインストールされていなかったらしてください。

## ライセンス / Licence

[MIT](https://github.com/tcnksm/tool/blob/master/LICENCE)

## 作者 / Author

[Koji-Doi](https://github.com/Koji-Doi)
