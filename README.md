# readtsv
readtsv - easy tsv file viewer/converter
====

Tab区切りテキストファイル（TSVファイル）の内容確認および簡単な整形に使えるツール

A tool to check content or to convert tsv files.

## Description
tabは「見えない」ため、その中身を確認したいときに不便を感じることがあります。そこで、とりあえずtabを"|"に置き換えて表示したいと考えて組んだワンライナーが本ツールのルーツです。

```
readtsv target.tsv
```

これに少しづつ機能を追加しながら、気が付けば10年愛用していました。折角なのでgithubで公開しようと思い立った次第です。
今では、次のようなことができます。
* 指定列のみを抜き出して表示
* 複行レコードとして表示
* csvへの変換
* html tableへの変更

## Demo

## VS. 

## Requirement

## Usage
readtsv input.tsv

readtsv -k 1,2 input.tsv

readtsv -m input.tsv

readtsv --html input.tsv

## Install
本スクリプトを適当なディレクトリに置いてください。perl5がインストールされていなかったらしてください。

## Contribution

## Licence

[MIT](https://github.com/tcnksm/tool/blob/master/LICENCE)

## Author

[Koji-Doi](https://github.com/Koji-Doi)
