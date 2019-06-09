# EclipseとGitLab連携

## 3. GitLab連携（プロジェクトの配置）

作成したMavenプロジェクトをGitLabのリモートリポジトリ（masterブランチ）にアップロードします。

### 3-1. ローカルリポジトリを作成する

<img src="../img/03-02.png" width="800">

- プロジェクトを右クリック > Team > Share Project

<br>

<img src="../img/03-03.png" width="700">

- [Use or create repository in parent folder of project]にチェックする
- 一覧から対象のプロジェクトを選択する
- [Create Repository]ボタンをクリックする

<br>

<img src="../img/03-04.png" width="700">

- [Finish]ボタンをクリックする

<br>

### 3-2. ローカルリポジトリにコミットする

リモートリポジトリにアップロードするファイル群をローカルリポジトリに保持します。

<img src="../img/03-06.png" width="800">

- プロジェクトを右クリック > Team > Commit

<br>

<img src="../img/03-07.png" width="800">

> ServersやConsoleなどのブロックに「Git Staging」のタブが表示される

<br>

<img src="../img/03-08.png" width="800">

- +ボタンを押して、[Unstaged Changes] にあるファイルを [Staged Changes] に移す
- [Commit]ボタンをクリックする

<br>

### 3-3. リモートリポジトリにプッシュする

ローカルリポジトリに保持しているファイル群をGitLabのリモートリポジトリにアップロードします。

<img src="../img/03-09.png" width="800">

- プロジェクトを右クリック > Team > Remote > Push

<br>

<img src="../img/03-10.png" width="700">

- 連携先のGitLab（リモートリポジトリ）の情報を入力する<br>
**URI**: 対象リモートリポジトリのURI<br>
**User**: あなたのGitLabアカウントのメールアドレス<br>
**Password**: あなたのGitLabアカウントのパスワード<br>
**Store in Secure Store**: チェックする

<br>

<img src="../img/03-11.png" width="700">

- masterリポジトリを追加する<br>
**Source ref**: [refs/heads/master]を選択する<br>
**Destination ref**: [refs/heads/master]を選択する
- [Add Spec]ボタンをクリックする

> 下部の一覧にmasterリポジトリが追加されます。

<br>

<img src="../img/03-12.png" width="700">

- [Next]ボタンをクリックする

<br>

<img src="../img/03-13.png" width="600">

- [Close]ボタンをクリックする

> エラーがなければ、masterリポジトリにプッシュされたことが確認できます。

<br>

<img src="../img/03-14.png" width="800">

> GitLab上の対象プロジェクトを見ると、Eclipseで作成したプロジェクトの構成が連携されていることが確認できます。

<br>

<a href="04-import-project.md">>> 04. GitLab連携（プロジェクトの取り込み）</a>

<a href="../README.md">>> メニューへ</a>
