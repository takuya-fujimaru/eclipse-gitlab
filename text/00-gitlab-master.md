# EclipseとGitLab連携

### 1. GitLabにログインし、新規プロジェクトを作成する

GitLab：https://gitlab.com/users/sign_in

<img src="img/01.PNG" width="800">

- プロジェクトの情報を入力する<br>
**プロジェクト名**: プロジェクト名<br>
**Visibily Level**: プライベート
- [Create project]ボタンをクリックする

<br>

### 2. 作成したプロジェクトにメンバーを追加する

<img src="img/02.png" width="800">

- 左メニュー > 設定 > メンバー

<br>

<img src="img/03.png" width="800">

- 追加するメンバーの情報を入力する<br>
**Select members to invite**: 追加するメンバーのアカウント名<br>
**Choose a role permission**: Maintainer
- [プロジェクトに追加]ボタンをクリックする

<br>

### 3. EclipseでMavenプロジェクトを作成する

<img src="img/04.png" width="800">

- 右クリックメニュー > Project > Maven > Maven Project

<br>

### 4. GitLab連携（ローカルリポジトリを作成する）

<img src="img/05.png" width="800">

- プロジェクトを右クリック > Team > Share Project

<br>

<img src="img/06.png" width="800">

- [Use or create repository in parent folder of project]にチェックする
- 一覧から対象のプロジェクトを選択する
- [Create Repository]ボタンをクリックする

<br>

<img src="img/07.png" width="800">

- [Finish]ボタンをクリックする

<br>

### 5. GitLab連携（pom.xmlを更新する）

<img src="img/08.png" width="800">

- Explorerからworkspace > 対象プロジェクトのフォルダ
- 下記リンク先のpom.xmlで上書き保存する

<a href="/file/pom.xml">pom.xml</a>

> pom.xml内の **groupId** と **artifactId** は各自のプロジェクトに合わせて修正する

<br>

### 6. GitLab連携（ローカルリポジトリにコミットする）

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

### 7. GitLab連携（リモートリポジトリにプッシュする）

<img src="img/13.png" width="800">

- プロジェクトを右クリック > Team > Remote > Push

<br>

<img src="img/14.png" width="800">

- 連携先のGitLab（リモートリポジトリ）の情報を入力する<br>
**URI**: 対象リモートリポジトリのURI<br>
**User**: あなたのGitLabアカウントのメールアドレス<br>
**Password**: あなたのGitLabアカウントのパスワード<br>
**Store in Secure Store**: チェックする

<br>

<img src="img/15.png" width="800">

- masterリポジトリを追加する<br>
**Source ref**: [refs/heads/master]を選択する<br>
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

> GitLab上の対象プロジェクトを見ると、Eclipseで作成したプロジェクトの構成が連携されていることが確認できる

<br>

### 8. GitLabからEclipseにり込む

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

- 取り込む対象のGitLab（リモートリポジトリ）の情報を入力する<br>
**URI**: 対象リモートリポジトリのURI<br>
**User**: あなたのGitLabアカウントのメールアドレス<br>
**Password**: あなたのGitLabアカウントのパスワード<br>
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
