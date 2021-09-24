---
title: Markdownてなに？シンタックスてなに？？
date: 2021-08-18 11:19:04 Z
Description: ''
Tags: []
Categories:
- hugo
---

この記事では、Hugoコンテンツファイルで使用できる基本的なMarkdown構文のサンプルを提供し、Hugoテーマで基本的なHTML要素がCSSで装飾されているかどうかを示します。

<!--more-->

## Headings

以下のHTMLの `<h1>`～`<h6>` 要素は、6段階のセクションの見出しを表しています。`<h1>` がセクションの最高レベルで、`<h6>` が最低レベルです。

# H1

## H2

### H3

#### H4

##### H5

###### H6

## ブロッククォート

blockquote要素は、他のソースから引用されたコンテンツを表します。オプションで、`footer`または`cite`要素内になければならない引用を行い、オプションで、注釈や略語などのインラインの変更を行います。

#### 帰属表示のないブロッククォート

> パル思う、ゆえにパルあり
> **注意** ブロッククォート内では、_Markdown構文_を使用することができます。

#### 帰属表示のあるブロッククォート

> このようにして、私たちは自分たちの生活をより豊かにすることができるのです。<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: 上記の引用は、2015年11月18日のGopherfestでのRob Pikeの[talk](https://www.youtube.com/watch?v=PAAkCSZUG1c)からの抜粋です。

## テーブル

テーブルはMarkdownのコア仕様には含まれていませんが、Hugoはすぐにサポートします。

| Name  | Age |
| ----- | --- |
| Bob   | 27  |
| Alice | 23  |

#### テーブル内でのMarkdownのインライン化

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

## コードブロック

#### バックティック付きコードブロック

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

#### コードブロックを4つのスペースでインデント

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

#### Hugoの内部ハイライトショートコードを使ったコードブロック

{{< highlight html >}}

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example HTML5 Document</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

## リストタイプ

#### 順序リスト

1. First item
2. Second item
3. Third item

#### 順不同のリスト

- List item
- Another item
- And another item

#### 入れ子のリスト

- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese

## 他の要素 — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> はビットマップ画像フォーマット.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

<kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> を押すとセッションを終了します。

ほとんどの <mark>サンショウウオ</mark> は夜行性で、昆虫やミミズなどの小さな生き物を狩ります。
