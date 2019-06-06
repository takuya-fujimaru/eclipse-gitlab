# EclipseとGitlab連携

#### 1. Gitlabにログインし、新規プロジェクトを作成する

**プロジェクト名**：プロジェクト名
**Visibily Level**：プライベート

Gitlab：https://gitlab.com/users/sign_in

<img src="img/01.png" width="800">

<br><br>

#### 2. 作成したプロジェクトにメンバーを追加する

<img src="img/02.png" width="800">

- 左メニュー > 設定 > メンバー

<br>

<img src="img/03.png" width="800">

- 追加するメンバーを選択肢し、プロジェクトに追加する。
Select members to invite：追加するメンバーのアカウント名
Choose a role permission：Maintainer


<br>

#### EclipseでMavenプロジェクトを作成する

<img src="img/04.png" width="800">

- 右クリックメニュー > Project > Maven > Maven Project

<br>

#### Gitlab連携（ローカルリポジトリを作成する）

<img src="img/05.png" width="800">

- プロジェクトを右クリック > Team > Share Project

<br>

<img src="img/06.png" width="800">

- Use or create repository in parent folder of projectにチェックする
- 一覧から対象のプロジェクトを選択する
- Create Repositoryボタンをクリックする

<br>

<img src="img/07.png" width="800">

- Finishボタンをクリックする

<br>

#### Gitlab連携（pom.xmlを更新する）

<img src="img/08.png" width="800">

- Explorerからworkspace > 対象プロジェクトのフォルダ
- 下記リンク先のpom.xmlで上書き保存する

<a href="/file/pom.xml">pom.xml</a>

<br>

#### Gitlab連携（ローカルリポジトリにコミットする）

<img src="img/09.png" width="800">

- プロジェクトを右クリック > Team > Commit

<br>

<img src="img/10.png" width="800">

> ServersやConsoleなどのブロックに「Git Staging」のタブが表示される

<br>

<img src="img/12.png" width="800">

- +ボタンを押して、[Unstaged Changes] にあるファイルを [Staged Changes] に移す
- [Commit]ボタンをクリックする

<br>

#### Gitlab連携（リモートリポジトリにプッシュする）

<img src="img/13.png" width="800">

- プロジェクトを右クリック > Team > Remote > Push

<br>

<img src="img/14.png" width="800">

- 連携先のGitlab（リモートリポジトリ）の情報を入力する
**URI**: 対象リモートリポジトリのURI
**User**: あなたのGitlabアカウントのメールアドレス
**Password**: あなたのGitlabアカウントのパスワード
**Store in Secure Store**: チェックする

<br>

<img src="img/15.png" width="800">

- masterリポジトリを追加する
**Source ref**: [refs/heads/master]を選択する
**Destination ref**: [refs/heads/master]を選択する
- [Add Spec]ボタンをクリックする

> 下部の一覧にmasterリポジトリが追加される

<br>

<img src="img/16.png" width="800">

- [Next]ボタンをクリックする

<br>

<img src="img/17.png" width="800">

- [Close]ボタンをクリックする

> エラーがなければ、masterリポジトリにプッシュされたことが確認できる

<br>

<img src="img/18.png" width="800">

> Gitlab上の対象プロジェクトを見ると、Eclipseで作成したプロジェクトの構成が連携されていることが確認できる

<br>

#### GitlabからEclipseに取り込む

<img src="img/20.png" width="800">

- Eclipseのプロジェクト・エクスプローラー内で右クリック > Import
- Git > Projects from Git を選択する
- [Next]ボタンをクリックする

<br>

<img src="img/21.png" width="800">

- [Clone URL]を選択する
- [Next]ボタンをクリックする

<br>

<img src="img/22.png" width="800">

- 取り込む対象のGitlab（リモートリポジトリ）の情報を入力する
**URI**: 対象リモートリポジトリのURI
**User**: あなたのGitlabアカウントのメールアドレス
**Password**: あなたのGitlabアカウントのパスワード
**Store in Secure Store**: チェックする

<br>

<img src="img/23.png" width="800">

- master にチェックされた状態で、[Next]ボタンをクリックする

<br>

<img src="img/24.png" width="800">

- 取り込み先を指定する
**Directory**: Eclipseのworkspaceを指定する
- [Next]ボタンをクリックする

<br>

<img src="img/25.png" width="800">

- [Import existing Eclipse projects]を選択する
- [Next]ボタンをクリックする

<br>

<img src="img/26.png" width="800">

- 対象プロジェクトが選択された状態で、[Finish]ボタンをクリックする
