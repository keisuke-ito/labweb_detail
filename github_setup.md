## GitHubでの共同開発セットアップ
## Git 初期設定
管理したいプロジェクト内で
```
$ git clone [git@github.com:~~~~~]
```
をして、共有レポジトリをクローンする。
(※ ただし、SSH keyをはじめに登録を済ませること。)

## ブランチの作成
Gitの初期設定でmasterブランチができているので、
```
$ git checkout -b [branch name]
```
で新しくブランチを作成して開発をする。

ブランチは機能(スコープ)ごとに切る\
ブランチ名は\
dev-[スコープ]-[suffix]\
スコープ例

- index
- research_top
- apply
- news

### Suffix一覧

- 書かない: メイン (基本的にsuffixはなくて良い)
- version: マージリクエストをすでにしていて、それに含めたくない実装を同じ名前のブランチで行いたいとき (ブランチ名が同じなままpushするとマージリクエストにも反映されてしまう)
- fix: 修正
- tmp: 一時的にお試しなどでブランチを切る場合

### メッセージ
commitのメッセージは以下のように記述を行うものとする。
```
[アクション](スコープ): メッセージ
```
アクション例

- feat: 機能
- fix: 修正
- refactor: リファクタリング
- trivial: 軽微な変更/雑用

例:\
feat(apply): 追加読み込み\
trivial(news): 文書の色の変更\
メッセージにはスコープの文言を含めない。純粋に行ったことを示す。

## git pull
開発を始める前に必ずmasterブランチに
```
$ git pull origin master
```
を行うこと。\

## git push
コミットした内容をリモートブランチに反映させる場合
```
$ git push origin [branch name]
```
によりプッシュを行う。

## Merge Request
開発が全て完了した後にはマージリクエストを出す。\
以下に方法を記す。\

右上の緑色の「Conpare & pull request」をクリック\

!['pull_request1'](../img/pull_request1.png)

どういった変更を加えたのかを説明する内容を記入\

!['pull_request2'](../img/pull_request2.png)

どのブランチからどのブランチにpull requestするかを確認する\
※developブランチからmasterブランチへのpull request\

!['pull_request3'](../img/pull_request3.png)

「Create pull request」ボタンを押して、Pull Requestを作成