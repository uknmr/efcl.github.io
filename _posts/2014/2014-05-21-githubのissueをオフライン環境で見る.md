---
title: Githubのissueをオフライン環境で見る
author: azu
layout: post
permalink: /2014/0521/res3908/
dsq_thread_id:
  - 2701285465
categories:
  - Github
tags:
  - github
  - tools
---
タイトル通りの事をしたくて色々ツールとかを探しているのですが、  
これだって感じのものはない気がします。

そもそもオフラインでGithub issueを見たいという要件自体がかなりマイナーなので当たり前な気もします。

自分の場合だと、[JavaScript Promiseの本][1]というのを書いてて、  
気になった事などTodoとかメモ代わりにどんどんissueにしておいて、  
それを移動中に振り返りながら処理するという感じでやってます。

*   [Issues · azu/promises-book][2]

オフライン環境に近い状態(テザリングとかするので完全なオフラインではない)でGithub issueを参照する頻度が高いので、ローカルでissueを見られたら便利だなーと思うのでそういうツールを探してました。

issueを処理する時は[yuroyoro/git-issue][3]+[percol][4]+[git-flow (AVH Edition)][5]でissueを選んでブランチを切って、WebStormからCreate PullRequestして、PullRequestをマージしてgit flow finishというフローを踏んでいます。





この辺のフローの話は[Issue][2]が潰せた頃にもう一度書くと思います(issue潰すの手伝って!)

## オフラインGithub Issue

本題に戻って、オフラインで見るアプリとか今のところ見つかってないので、  
とりあえずGithub issueの内容をローカルにダウンロードして見られるようにしています。

*   [mislav/issuesync][6]

上記のツールを使うとGithub APIでissueの内容をMarkdownファイルとして参照できるので、とりあえずオフラインでも見ることは出来るようになりました。

上記のツールだとタイトルがファイル名にないので、ちょっとfork[azu/issuesync][7]して使っています。

<img src="https://efcl.info/wp-content/uploads/2014/05/Promises-book-2014-05-21-13-50-16-2014-05-21-13-50-25.png" alt="Promises book 2014 05 21 13 50 16 2014 05 21 13 50 25" title="Promises-book] 2014-05-21 13-50-16 2014-05-21 13-50-25.png" border="0" width="600" height="547" />

Github issueで `- [x]` というTodoをよく使っているのですが、これがオフラインでも更新できて、オンラインになったら更新出来るようなツールが欲しい。

## 他の手段

他の手段を考えてみると[BugHub][8]は結構いいUIで、実はこれ[Me1000/BugHub][9]ソースが公開されているので、これをいじってオフライン対応してみるとか、  
[Githubのタイムラインや通知を見るアプリをnode-webkitで作った | Web scratch][10] とかみたいに何かアプリを作る必要がある気がします。

何か他の手段がある方は教えてください。

 [1]: https://github.com/azu/promises-book "JavaScript Promiseの本"
 [2]: https://github.com/azu/Promises-book/issues?milestone=1&state=open "Issues · azu/promises-book"
 [3]: https://github.com/yuroyoro/git-issue "yuroyoro/git-issue"
 [4]: https://github.com/mooz/percol "percol"
 [5]: https://github.com/petervanderdoes/gitflow "git-flow (AVH Edition)"
 [6]: https://github.com/mislav/issuesync "mislav/issuesync"
 [7]: https://github.com/azu/issuesync "azu/issuesync"
 [8]: http://bughubapp.com/index.html "BugHub"
 [9]: https://github.com/me1000/bughub/ "Me1000/BugHub"
 [10]: https://efcl.info/2014/0430/res3872/ "Githubのタイムラインや通知を見るアプリをnode-webkitで作った | Web scratch"
