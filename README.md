## 日本語訳について 

本リポジトリは[Ruby on Rails Guides](http://guides.rubyonrails.org/)を日本語に訳したものです。

Railsガイド   
http://railsguides.jp/

また，[Ruby on Rails Tutorial](https://www.railstutorial.org/)の日本語訳「Railsチュートリアル」も無料で公開されているので，    
こちらも是非合わせて読んでみてください :)

Railsチュートリアル   
http://railstutorial.jp/


## 翻訳の流れ

![翻訳の流れ](https://raw.githubusercontent.com/yasslab/railsguides.jp/japanese/images/flow-of-translation.jpg)
参考: [[翻訳]Ruby on Rails 4.1リリース前にアップグレードガイドを先行翻訳した & 同じ翻訳を2回しないで済むようにした](http://techracho.bpsinc.jp/hachi8833/2014_03_28/16037)

### ① 原著との差分更新の方法

- cf. [Syncing a fork, GitHub Help](https://help.github.com/articles/syncing-a-fork)

### ② GTTに最新のドキュメントをアップロードする

- Google Translator Toolkit: https://translate.google.com/toolkit/
- Markdownは対応してないので、必要に応じてファイル名を `hogehoge.md.txt` などに変更する。
- ※必ずRailsガイド用の翻訳メモリに結びつけること. (shared TM は使わない)
- cf. [翻訳メモリの使用 - Translate ヘルプ - Google Help](https://support.google.com/translate/toolkit/answer/147863?hl=ja)

**GTT は共有が面倒なので，ターミナルなどで編集して Pull Request して頂いても大丈夫です :+1: その際は，@yasulab などが別途 GTT 上の翻訳メモリに訳文を格納します．**
(↑ このステップを，もうちょっとスマートにできるようにしたい...)

### ③ GTT上で英語→日本語に翻訳する (訳文は翻訳メモリに格納)

- 詳細: [Google Translator Toolkitと翻訳メモリ(ノーカット版) : RubyWorld Conference 2013より](http://techracho.bpsinc.jp/hachi8833/2013_12_16/14889)
- GTTの使用方法や文体などに関しては[こちら](https://www.facebook.com/notes/ruby-on-rails-tutorial-%E7%BF%BB%E8%A8%B3%E3%82%B0%E3%83%AB%E3%83%BC%E3%83%97/google-translator-toolkit-gtt-%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9/170100333166820)を参考にしてください。
- ※CSSの関係で、行頭が`(TIP|IMPORTANT|CAUTION|WARNING|NOTE|INFO|TODO)[.:]`から始まる場合、`(TIP|IMPORTANT|CAUTION|WARNING|NOTE|INFO|TODO)`は訳さないでください。

### ④ 日本語のHTMLファイルの生成方法

0. `/guides` フォルダに移動する
1. Google Translator Toolkit から訳文のファイルをダウンロードする (要: ダウンロード権限)
2. `./main.sh` を実行して、訳文のファイルを適切な名前に変更し、`/source` 以下に配置。
3. `bundle exec rake guides:generate:html`を実行して、`/output`以下にHTMLを生成。

### ⑤ Herokuにデプロイ

- @yasulab が対応.
- 手伝ってくれる方がいれば @yasulab まで. collaborator に追加します.

## Railsガイド協力者

- [@hachi8833](https://github.com/hachi8833)
- [@yasulab](https://github.com/yasulab)

and supported by [ヤスラボ](http://yasslab.jp/ja/).

### 協力者の相談部屋 (チャットルーム)

[idobata.io](https://idobata.io) の [yasslab/railsguides.jp](https://idobata.io/organizations/yasslab/rooms/railsguides/join_request/c89d1d3b-d6d1-4baa-9271-145fbd0c4734) 部屋にて，Rails ガイドに関する情報交換しています．   
覗いてみるだけの方も歓迎なので，是非お気軽に立ち寄ってみてください :D

![井戸端会議風景](https://raw.githubusercontent.com/yasslab/railsguides.jp/japanese/images/idobata-ss.png)

## ライセンス

[![CC BY-SA International](https://raw.githubusercontent.com/yasslab/railsguides.jp/japanese/images/CC-BY-SA.png)](https://creativecommons.org/licenses/by-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-Share Alike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

"Rails", "Ruby on Rails", and the Rails logo are trademarks of David Heinemeier Hansson. All rights reserved.

[Ruby on Rails](http://rubyonrails.org/) is released under the [MIT License](http://www.opensource.org/licenses/MIT).
