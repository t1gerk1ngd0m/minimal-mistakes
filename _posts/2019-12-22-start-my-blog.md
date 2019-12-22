---
layout: blog
title: jekyllで技術ブログ始めました。
---

jekyllを使って技術blogを始めました。業務の中で詰まったことなど自分用にメモとしてストックしていきたいと思います。


## 目次
- なぜjekyll？
- 始め方
- デザイン
- デプロイ
- 終わりに


### なぜjekyll？

自分のメモ用にブログを書くだけなので、Qiitaに書いてしまうとSEOで上位表示されてあまりよろしくない。
かといって勉強のためにRailsでスクラッチで開発することも考えたけど、静的サイトを作るためにRailsはやりすぎ感があった。
最初はWordPressにしようかなと思ったけど、Rubyの勉強になるし会社でも使ってるし、何よりjekyllは早い！
環境構築も楽チンなのでストレスなく学習出来るので、jekyllを選びました。

### 始め方

jekyllの始め方のサイトは色々参考サイトがあるので、詳細はそちらに譲ろうと思う。
- [jekyll公式の日本語版](http://jekyllrb-ja.github.io/)
- [GitHub Pages の Jekyll で Web サイトを無料公開する方法](https://qiita.com/takuya0301/items/374b2ab5be407b138ef9)

### デザイン

デザインはMinimal Mistakesのテーマを使っています。
参考
- [JekyllでMinimal Mistakesのテーマを使う](https://qiita.com/naoyukisugi/items/42f16b7004eb0ef6ba85)
- [Minimal Mistakes -Quick-Start Guide](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

### デプロイ

デプロイはNetlifyを使っています。
最近流行りのNetlifyをプライベートでも使って見たいなと。
[jekyllをNetlifyにデプロイした](https://blog.n-z.jp/blog/2018-03-06-jekyll-to-netlify.html)

使い心地はものすごくよくて、Githubから自動デプロイ出来る！
しかも設定もすごく簡単でほとんど考えなくてもいいUXだった。
ブログみたいな静的サイトで使うだけだったら、正直Netlifyで十分だと思う。
あと今回は試していないけど、問い合わせフォームに対応した機能もあるみたいなので便利。
コーポレートページもWordPressよりJekyll+Netlifyで構築した方が良さそう感。
