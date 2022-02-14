---
title: "Fyneのドラッグアンドドロップ実装進捗のまとめ"
date: 2022-02-14T22:41:52+09:00
draft: false
---

# はじめに
この記事は[2021年Goアドベントカレンダー18日目](https://qiita.com/advent-calendar/2021/go)の記事です。\
初めてのアドベントカレンダーの投稿で、ネタが思いつかずにひねり出したものなので、暖かい目で見てください...

# 概要

[Fyne](https://fyne.io/)はGoで書かれたウィジェットツールキットで、マルチプラットフォームで動作します。\
開発も結構活発です。\
が、**残念ながら記事を書いている現在ドラッグアンドドロップは実装されていません。**\
僕もFyneでアプリケーションを書いていて結構困りました。\
そこでFyneのドラッグアンドドロップ機能の実装経緯についてまとめました。
# 経緯
## 2019年ごろIssueが立てられる
![img](/images/Fyne-drag-and-drop-issue1.png)
[Add drag and drop support](https://github.com/fyne-io/fyne/issues/142)\
ドラッグアンドドロップについての提案がなされています。\
相当ニーズあるようでたくさんコメントがついています。\
~~最後のほうもう聞くなみたいなこと言われてて面白い。~~

## 2020年ごろにも同じようなIssueが立てられる
![img](/images/Fyne-drag-and-drop-issue2.png)
[Drag & Drop](https://github.com/fyne-io/fyne/issues/896)\
開発者の方に先ほどのIssueに誘導されていますね


## 2021年ごろにPRが開かれる
![img](/images/Fyne-drag-and-drop-PR1.png)
[Drag-adn-Drop proposal](https://github.com/fyne-io/proposals/pull/5)\
記事を書いている現在でもオープンのままです。

## 公式ブログの「次の大きな実装」に載る
![img](/images/Fyne-drag-and-drop-blog1.png)

読んだ感じだとドラッグアンドドロップ機能がもうすぐ実装されるようですね!!

