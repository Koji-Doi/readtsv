# readtsv
readtsv - easy tsv file viewer/converter
====

Tab区切りテキストファイル（TSVファイル）の内容確認および簡単な整形に使えるツール

A tool to check content or to convert tsv files.

## 概要 / Summary
tabは「見えない」ため、tsvファイルの中身を確認したいときに不便を感じることがあります。そこで、とりあえずtabを"|"に置き換えて表示したいと考えて組んだワンライナーが本ツールのルーツです。これをスクリプトファイルに仕立て、少しづつ機能を追加しながら、気が付けば10年愛用していました。折角なのでgithubで公開しようと思い立った次第です。

今では、次のようなことができます。
* 指定列のみを抜き出して表示
* 複行レコードとして表示
* csvへの変換
* html tableへの変更

## 使用例 / Example
readtsv input.tsv

readtsv -k 1,2 input.tsv

readtsv -m input.tsv

readtsv --html input.tsv

## 解説 / Description
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
