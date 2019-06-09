# EclipseとGitLab連携

## 4. GitLab連携（プロジェクトの取り込み）

開発チーム内の各メンバーは、GitLabのリモートリポジトリ（masterブランチ）にあるプロジェクトをローカルに取り込んで開発を行います。

### 4-1. GitLabからEclipseに取り込む

<img src="../img/04-01.png" width="600">

- Eclipseのプロジェクト・エクスプローラー内で右クリック > Import
- Git > Projects from Git を選択する
- [Next]ボタンをクリックする

<br>

<img src="../img/04-02.png" width="600">

- [Clone URL]を選択する
- [Next]ボタンをクリックする

<br>

<img src="../img/04-03.png" width="600">

- 取り込む対象のGitLab（リモートリポジトリ）の情報を入力する<br>
**URI**: 対象リモートリポジトリのURI<br>
**User**: あなたのGitLabアカウントのメールアドレス<br>
**Password**: あなたのGitLabアカウントのパスワード<br>
**Store in Secure Store**: チェックする

<br>

<img src="../img/04-04.png" width="600">

- master にチェックされた状態で、[Next]ボタンをクリックする

<br>

<img src="../img/04-05.png" width="600">

- 取り込み先を指定する
**Directory**: Eclipseのworkspaceを指定する
- [Next]ボタンをクリックする

<br>

<img src="../img/04-06.png" width="600">

- [Import existing Eclipse projects]を選択する
- [Next]ボタンをクリックする

<br>

<img src="../img/04-07.png" width="600">

- 対象プロジェクトが選択された状態で、[Finish]ボタンをクリックする

<br>

### 4-2. 取り込んだプロジェクトの環境整備

GitLabから取り込んだプロジェクトは設定（フォルダ構成）が崩れている可能性があります。<br>Eclipseのビルドパスの構成で環境を整えましょう。

プロジェクトを右クリック > Build Path > Configure Build Path

<img src="../img/04-08.png" width="800">

- [Source]タブで **(missing)** となっているフォルダを削除する<br>
missingのフォルダを選択する<br>
[Remove]ボタンをクリックする

<br>

<img src="../img/04-09.png" width="800">

- [Add Folder]ボタンをクリックする

<br>

<img src="../img/04-10.png" width="600">

- 一覧からプロジェクト（画像ではsample_project）を選択して、[Create New Folder]ボタンをクリックする

<br>

<img src="../img/04-12.png" width="600">

- 「**src/main/java**」を入力して、[Finish]ボタンをクリックする

> 同様に「**src/main/resources**」も作成し、次の画像のような構成にしてください。

<br>

<img src="../img/04-13.png" width="600">

- [OK]ボタンをクリックする

<br>

<img src="../img/04-14.png" width="800">

- <span style="color:red">[Apply]ボタンをクリックする</span>
- src/main/javaフォルダの **Output folder** をダブルクリックする

<br>

<img src="../img/04-15.png" width="700">

- [Specific output folder ...]を選択し、[Browse]ボタンをクリックする

<br>

<img src="../img/04-16.png" width="600">

- **target > classes**フォルダを選択して、[OK]ボタンをクリックする

<br>

<img src="../img/04-17.png" width="800">

- [OK]ボタンをクリックする

> 上記までの Output folder の設定を src/main/resourcesフォルダに対しても行います。

<br>

<img src="../img/04-18.png" width="800">

- [Apply and Close]ボタンをクリックする

<br>

<a href="05-switch-branch.md">>> 05. ブランチによる開発</a>

<a href="../README.md">>> メニューへ</a>
