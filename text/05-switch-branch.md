# EclipseとGitLab連携

## 5. ブランチによる開発

Gitの**ブランチ**とは、成果物（プログラムなど）の履歴を記録していく機能のことです。最終的な成果物（リリース版）は **masterブランチ** に集約されます。<br>しかし、開発者全員がそれぞれ作成したプログラムを直接masterブランチに対してアップしていくと、**コンフリクト**を起こす可能性が高まります。

> **コンフリクト**とは、複数の開発者が同じファイルを編集し、リモートリポジトリにプッシュすることで起きる競合（編集情報の重複）のことです。<br>コンフリクトについては、次章で解説します。

そのため、複数の開発者でバージョン管理をする場合、機能や作業ごとにブランチを作成し、作成したブランチに対してプログラムをプッシュします。

> 機能や作業ごとに作成するブランチを**トピックブランチ**と言います。<br>それに対してmasterブランチを**統合ブランチ**と言います。

作業が完了したらトピックブランチをmasterブランチへ **マージ（統合）** します。

<img src="../img/05-01.png" width="800">

<br><br>

### 5-1. トピックブランチを作成する

<img src="../img/05-02.png" width="800">

- プロジェクトを右クリック > Team > Switch To > New Branch

<br>

<img src="../img/05-03.png" width="600">

- ブランチ名を入力して新規にブランチを作成する<br>
**Branch name**: 作成するブランチ名
- [Finish]ボタンをクリックする

<br>

<img src="../img/05-04.png" width="400">

> Eclipse上のプロジェクトに対応するブランチ名が変わっていることが確認できます。

<br>

### 5-2. トピックブランチに成果物をプッシュする

それでは、１つの機能を作成し、トピックブランチにプッシュしましょう。

<img src="../img/05-05.png" width="600">

- 該当機能に必要なサーブレットやJSPを作成していきます。

> サーブレットの場合、作成時の[Source folder]が **src/main/java** になっていることを確認してください。

<br>

<img src="../img/05-06.png" width="800">

- プログラムを作成し終えたら、対象のファイルをステージングエリア（Staged Changes）に追加する
- [Commit and Push]ボタンをクリックする

<br>

<img src="../img/05-07.png" width="600">

- **Branch**が作成したブランチになっていることを確認し、[Next]ボタンをクリックする

<br>

<img src="../img/05-08.png" width="600">

- [Finish]ボタンをクリックする

<br>

<img src="../img/05-09.png" width="600">

- [Close]ボタンをクリックする

<br>

<img src="../img/05-10.png" width="800">

> GitLab上でブランチを切り替えると、プッシュした内容が反映されていることが確認できます。

<br>

### 5-3. トピックブランチをmasterブランチに統合する

作成したプログラムをトピックブランチに反映させたら、トピックブランチの内容をmasterブランチに **マージ（統合）** します。<br>マージするには、まずmasterブランチに切り替える必要があります。

<img src="../img/05-11.png" width="800">

- プロジェクトを右クリック > Team > Switch To > master

<br>

<img src="../img/05-12.png" width="800">

- プロジェクトを右クリック > Team > Merge

<br>

<img src="../img/05-13.png" width="600">

- masterブランチにマージするブランチを選択する
- [Merge]ボタンをクリックする

<br>

<img src="../img/05-14.png" width="500">

- マージ結果画面で[OK]ボタンをクリックする

<br>

<img src="../img/05-15.png" width="800">

- プロジェクトを右クリック > Team > Push Branch 'master'

<br>

<img src="../img/05-16.png" width="600">

- [Preview]ボタンをクリックする

<br>

<img src="../img/05-17.png" width="600">

- [Push]ボタンをクリックする

<br>

<img src="../img/05-18.png" width="600">

- [Close]ボタンをクリックする

<br>

<img src="../img/05-19.png" width="800">

> GitLab上で、トピックブランチの内容がmasterブランチに反映されていることが確認できます。

<br>

### 5-4. 最新のmasterブランチを取り込む

他の開発者は、masterブランチに切り替えてプルをすることで、マージされた内容も含めて取り込むことができます。

<img src="../img/05-20.png" width="500">

<br><br>

<a href="06-conflict.md">>> 06. コンフリクトと対処方法</a>

<a href="../README.md">>> メニューへ</a>