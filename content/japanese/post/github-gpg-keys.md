+++
author = "Paru"
title = "GithubのGPGキーを登録したよ"
date = 2021-08-26T22:48:12+09:00
description = ""
Categories = [ "github" ]
+++

GithubでGPGキーを登録したよ！そういうのも要るときもあるよね

<!--more-->

## GPGキー？？

Githubでコミットに署名をつけることができるんだ。（たぶん）

そうすることで「パルがコミットした！」のを信用することができるんだね（たぶん）

もともとリモートへのプッシュはPATトークンを登録していて、個人リポジトリへのプッシュには困ってないんだけど、パルはいつもひとりじゃないからさっ


## SSHキーとほぼ同じ

登録の仕方はSSHキーを設定するのとほとんど同じ。詳しくはGithubの方を見てね！

1. Macのターミナルで `brew install gpg`
2. [Github](https://docs.github.com/ja/github/authenticating-to-github/managing-commit-signature-verification/generating-a-new-gpg-key)に書いてるとおりにキーを生成
3. GithubのSettingページでキーを登録
4. Macローカルにもキーを登録
