# GitHub Foundaitons ハンズオン手順書

## 参加者事前準備

- GitHubアカウントの作成
  - github.comにメールアドレスを使ってサインインして作業できること
  - 会社から付与されたIDを入力後にAzure Entra IDなど外部のサービスでサインインをする、Enterprise Managed Userをお使いの場合は別途個人アカウントを作成しておいて下さい
- gitのインストール
  - [Gitのインストール](https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)を参考に、PCにgitをインストールしておく
  - [Gitの初期設定](https://git-scm.com/book/ja/v2/%e4%bd%bf%e3%81%84%e5%a7%8b%e3%82%81%e3%82%8b-%e6%9c%80%e5%88%9d%e3%81%aeGit%e3%81%ae%e6%a7%8b%e6%88%90)を行う
    - 「個人の識別情報」にある、ユーザ名とメールアドレスの設定を行っておく
    - メールアドレスはgithub.comにサインインするメールアドレスを設定することを推奨するが、既に設定が終わっているのであればそのままで良い
- VSCodeのインストール
  - [Download Visual Studio Code](https://code.visualstudio.com/download)からダウンロードしてインストールする
- (可能であれば)自身が管理するOrganizationを作成する

## 講師準備

PowerShellでデモを行う場合は以下のコマンドを実行して、コマンド履歴の補完が表示されないようにする。

```powershell
Set-PSReadLineOption -PredictionSource None
```

また、自身が管理するOrganizationを準備し、1つ以上リポジトリを作成しておく

## ハンズオン

1. [ドメイン1:GitとGitHubの紹介](./domain1/README.md)
2. [ドメイン2:GitHubリポジトリの操作](./domain2/README.md)
3. [ドメイン3:共同作業機能](./domain3/README.md)
4. [ドメイン4:モダンな開発](./domain4/README.md)
5. [ドメイン5:プロジェクト管理](./domain5/README.md)
6. [ドメイン6:プライバシー、セキュリティ、および管理](./domain6/README.md)
7. [ドメイン7:GitHubコミュニティの利点](./domain7/README.md)

