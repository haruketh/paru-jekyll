+++
author = "Paru"
title = "GitbookをGithubに連携した"
date = "2021-08-19"
description = ""
categories = [
    "gitbook",
]
+++

GitbookからGithubにデータ連携したよという話。

<!--more-->

## Gitbook Integration

Gitbookのメニューバーにある **"Integration"** で Github を選んで、ブランチを指定するだけだった。

すぐに同期が始まって10秒くらいで同期完了。

GitbookとGithubは双方向の変更同期に対応していて、一旦同期したら、そのあとはGitbookをいじるでも、Githubでマージするでもどちらの変更も相互に反映されるみたい。

- Gitbook →　Github に同期
- Github →　Gitbook に同期


## ブランチを指定して同期

"Master" ブランチに同期されたから、ちょっと気に入らない。Master って古くない？

だから別のブランチを指定して同期もしてみた。

同期させてみたら、Masterとは別のブランチに同期した。


## ブランチごとに分けて同期

Gitbook上で、Masterと別ブランチでは異なるバージョンとして保存されるっぽい。Gitbookでブランチを切ってる感じ。

つまり！　変更案みたいな感じで一旦ブランチBにマージして、GithubでブランチAにプルリクして、Github →　Gitbook への同期ができるということ。

**どうしてもレビューやマージの権限、承認はGithub側でしたい！履歴を残したい！** というケースなら、この方法はありかも。

### ブランチの削除

複数のブランチ同期を作ってしまって、不要なものがある時は、Variant を削除とか、メインブランチを変更もできる。


ちなみに公開してるのは [Nimbus Book](https://paru.gitbook.io/nimbus-book-ja/) だよ。

