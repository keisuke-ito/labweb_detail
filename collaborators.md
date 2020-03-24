## GitHub コラボレーターについて

git hubを使って複数人とあるレポジトリを共有したい場合のメモ

注意: public repositoryではコラボレータは無限に追加できるが、private repositoryでは4人までしか追加できない。


### step1
![](../img/collaborators1.png)

共有したいレポジトリの右端にある「Settings」をクリック.

「Manage access」をクリックする。

Manage accessの右端にある「Invite a collaborator」をクリック.

### step2
![](../img/collaborators2.png)


追加したい人のusername or emaill or full nameを入力して「Select a collaborator above」をクリック.

![](../img/collaborators3.png)

上図のように表示されたら「Add 〜」をクリック.

クリックして追加された人が承認をしたらそのレポジトリにpushできるようになる。

### step3
![](../img/collaborators4.png)

上図のようにリモートレポジトリを作成したいフォルダで

$ git init

$ git remote add origin [ssh先]

$ git pull origin master

以上で、共有レポジトリが作成されるので自分のしたいことをする。