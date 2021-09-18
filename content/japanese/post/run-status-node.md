+++
author = "Paru"
title = "Statusノードを立てたよ"
date = 2021-08-22T12:24:12+09:00
description = ""
Categories = [ "status" ]
+++

Statusノードを立てたよ。その名も ✨**Status Node Tokyo**✨ かっこいいでしょ！

<!--more-->

## Statusノードを作る

サーバを借りて早速ビルドだーーーー🔥

1. クラウドを契約

2. Linuxサーバ構築
 - アプデ
 - 自動更新、自動リムーブを設定
 - ユーザ追加
 - 公開鍵つくる
 - FWを設定（30303ポート開放）

3. Dockerインストール
 - その他のコンポーネントもインストール

4. Statusノード実行
 - GithubからStatus-goをクローン
 - Statusノードを実行


## めっちゃ動いてる！

実行したらすぐにピアを張って、エンベロープを取得できてるみたい。

```
% curl -s localhost:9090/metrics | grep '^waku_envelopes_received_total'
waku_envelopes_received_total 969
```

あとは、Statusアプリにenodeアドレスを入れてみて、ちゃんと動くかどうかだね！楽しみ！
