# ドメイン3:共同作業機能

## Issueの作成と操作

Issueの作成と操作について確認する。

- `foundations-hands-on-2`リポジトリにgithub.comでアクセスし、ナビゲーションのIssuesにアクセスする
- 「New issue」ボタンでIssueを作る。入力できる項目を確認する。descriptionにマークダウンが使え、ツールチップでの入力やスラッシュコマンド(`/`を入力してみる)が使えることを確認する
  - ![new issue](../image/image3-1.png)
  - 「README.mdの更新」というtitleにする
  - 「Submit new issue」ボタンを押してIssueを作成する
- 作成したIssueの画面を見る。右側にメタデータがあることを確認し、それぞれが何を表しているかを確認する。
  - メタデータのDevelopmentから`foundations-hands-on-2`リポジトリを選択し、`update-readme`ブランチを選択し、「Apply」を押してブランチと紐付けてみる
  - ![development](../image/image3-2.png)
  - ピン留めしてみる
  - ![pin issue](../image/image3-3.png)
- 2つめのIssueを作る
  - 1つめと同じ、「README.mdの更新」という内容にする
- Issueの一覧で、フィルターやソートをしてみる
- それぞれのIssueの一番下のボタンからクローズ、再オープンしてみる 
  - 「Close issue」ボタンの右の「▼」でプルダウンが避雷器、クローズに2種類あることを確認する
  - ![close issue](../image/image3-4.png)
  - ナビゲーションのIssuesをクリックしてIssueの一覧画面に戻り、フィルターの「is:open」を「is:closed」に変更すると、クローズしたissueの一覧が表示される。そのうちの一つにアクセスして、再度オープンしてみる
  - ![filter box](../image/image3-5.png)
  - ![reopen issue](../image/image3-6.png)
- 2つめのIssueにアクセスし、重複とするためにコメントに`Duplicate of #1`と入力して「Comment」ボタンを押す
  - マークがついたとメッセージが出ていることを確認する
  - ![duplicated issue](../image/image3-7.png)
  - [!TIP]これは、以下のようなケースで使うことを講師は説明する
    - もし重複したIssueを見つけたとしても、多くの人にはIssueの削除の権限がない
    - 削除できないが、「解決済み」としてcloseするのは適切でない
    - そこで、クローズする前にマークしておくことで、クローズの理由を伝えることができる
    - 現在はクローズの種類として「Close as not planned」があるのでそれを併せて使う
- リポジトリをもう１つ作る
  - 名前は`foundations-hands-on-3`
    - パブリック、READMEあり、ライセンスはMIT、.gitignoreはなし
  - `foundaitons-hands-on-3`リポジトリでIssueを作る
    - titleは`転送のテスト`とする
    - Issueの右下の「Transfer」ボタンで、`foundations-hand-on-2`リポジトリに転送してみる
    - ![transfer issue](../image/image3-8.png)
  - 転送されていることを確認する
  - 転送されてきたIssueを右下のボタンで削除してみる
  - ![delete issue](../image/image3-9.png)
- Issue templateとFormsを作ってみる
  - **Issue template**：Feature request のテンプレートを作る
  - [公式ドキュメント](https://docs.github.com/ja/enterprise-cloud@latest/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)
      - `foundations-hands-on-2`リポジトリにgithub.comでアクセスし、ナビゲーションのSettingsにアクセス
    - General > Features > Issuesで「Set up templates」ボタンを押してテンプレートを作ってみる
    - ![set up issue templates](../image/image3-10.png)
    - `Add template: select` から `Feature request` を選ぶ
    - ![Add template: select](../image/image3-10-a.png)
    - `Preview and edit`  ＞ `✏️` で編集画面に移動して、テンプレートを編集する
    - ![Preview and edit](../image/image3-10-b.png)
    - ![Custom template のプレビュー画面](../image/image3-10-c.png)
    - ![Custom template の編集画面](../image/image3-10-d.png)
    - 作成したファイルは`.github/ISSUE_TEMPLATES/`にあることを確認する
  - **Forms**：Bug report のフォームを作る
    - Formsは[サンプルのYAML](./bug-report.yml)をコピペして、`.github/ISSUE_TEMPLATES/bug-report.yml`を作成する
  - ナビゲーションのIssuesからIssue一覧画面に戻って「New issue」ボタンを押し、Issue templateとIssue formsを使ってIssueを作ってみる

## Pull requestの作成と操作

Pull requestの作成と操作について確認する。

- `foundations-hands-on-2`リポジトリにgithub.comでアクセスし、CODEOWNERSファイルを新規に作成する
  - ハンズオンの相方をリポジトリに招待する
    - リポジトリのナビゲーションのSettingsからCollaborators and teamsにアクセスし、「Add people」ボタンを押す
    - ![ユーザーをリポジトリへ招待](../image/image3-35.png)
    - 相方に招待メールが届いているので、リンクをクリックして招待を受け入れてもらう
  - ハンズオンの相方をCODEOWNERSファイルでレビュアーにいれておく
  - 書式は`*    @相方のアカウント名`
  - ![CODEOWNERS](../image/image3-11.png)
- github.com上でリポジトリにアクセスし、ナビゲーションのCodeから適当なファイルを選ぶと、設定したアカウント名がオーナーとしてホバーされることを確認する
- ![hover codeowner](../image/image3-12.png)
- mainブランチの`README.md`を更新。`foundation-1`という記載を`foundation-2`にし、直接プッシュではなく`Create a new branch`を押す
  - Pull request画面に移動するが、ナビゲーションのPull requestsを押してキャンセルする
- 作成したブランチからPull requestを作る
  - ナビゲーションのPull requestssから「New Pull request」を押す
  - ![new pull request](../image/image3-13.png)
  - タイトルに`Update README.md`を入れる
  - Descriptionは適宜入力しつつ、`Close #1`を入れる(もし作成したIssueの番号がずれてるなら#の後ろの数字を変える。#を入れたら補完が効く)
  - 「Create pull request」ボタンの右の「▼」を押し、draftで作成することもできることを確認する
  - 「Create pull request」ボタンを押してPull requestを作成する
  - 作成したらCODEOWNERSに先ほど入れた、ハンズオンの相方の人が自動的にレビュアーに入ってる事を確認する
- 作成したPull requestの画面で、これらの「Conversation」「Commits」「Checks」「Files changed」タブがあることを確認する
  - ![4 tabs](../image/image3-36.png)
- コメントしてみる
  - マークダウンやslash commandが使えることを確認する
- Pull requestのステータスについて確認する
    - 作った状態がOpen
    - Reviewersの所からdraftに変更できる。作業中でまだレビューを受けられる状態ではないようなときはdraftにしておく(作成時にdraftにもできる)
    - ![convert to draft](../image/image3-14.png)
    - draftになったPull requestは、コメントの下の方の「Ready for review」を押してOpenに戻せる
    - ![ready for review](../image/image3-15.png)
    - コメントの下のボタンを押してCloss、Reopenできる
    - ![close pull request](../image/image3-16.png)
- レビューしてみる
  - 自分のものにもレビューはできるが、できるだけハンズオンの相方のものをレビューする
  - レビューのステータスについて確認する
- レビューで変更提案を出す
  - ツールチップからか、[suggestionコードブロック](./suggestion.md)を直接入力する
  - ![suggestion](../image/image3-17.png)
  - 取り入れると即座に内容がコミットされることを確認する
  - ![commit suggestion](../image/image3-18.png)
- Pull requestのメターデータの「Development」からIssue #2を追加でリンクしてみる
- ![link issue to pull request](../image/image3-19.png)
- マージしたら自動でクローズされてIssueの#1/#2もクローズされることを確認する
  - マージでクローズしたものは再オープンができないことを確認する
- Pull requestテンプレートを作って、テンプレートを使ったpull requestを作ってみる
  - `.github/pull_request_template.md`を作成する
  - [サンプルテンプレート](./pull_request_template.md)を貼り付けてコミットする
  - 新しいIssueを作成してみて、Descriptionにテンプレートの内容が含まれていることを確認する

## Discussions

Discussionsについて確認する。

- `foundations-hands-on-2`リポジトリのナビゲーションのSettingsからDiscussionsをONにする
  - ![Settings](../image/image3-20.png)
  - ![Discussions](../image/image3-21.png)
- ナビゲーションにDiscusisonsが表示されることを確認する
- Discussionsにアクセスする
- カテゴリーがあることを確認する
- カテゴリー「Q&A」でスレッド(Discussion)を作る
  - 回答を書き込んでみる
  - 回答とマークしてみる
  - ピン留めしてみる
  - DiscussionからIssueを作成してみる
  - ![mark-pin-create_issue](../image/image3-22.png)

## 通知

通知について確認する。

- 任意のページから通知に移動し、届いている通知一覧を見る
  - ![notifications](../image/image3-31.png)
- IssueやPull requestのそれぞれのSubscription状態を見る
  - 自身が作ったので、自動的にSubscribeされている(Participate)ことを確認する
    - ![nofitication of issue](../image/image3-32.png)
  - Unsubscribeしてみる
- `foundations-hands-on-2`のナビゲーションのCodeに移動し、「watch」ボタンで何が選べるかを確認する
  - ![watch of repository](../image/image3-33.png)
- 通知ページから、ユーザー設定を見る(左下の「Manage notifications」)
  - ![manage notifications](../image/image3-34.png)

## Gistについて

Gistについて確認する。

- 任意のページからアカウントアイコンを押し、「Your Gists」を押してGistにアクセスする
  - ![account icon](../image/image2-7.png)
  - ![your gist](../image/image3-23.png)
- 新しいGistを作る
  - 一旦secretで作成する
  - 「Edit」からpublicにしてみる
    - ![edit gist](../image/image3-24.png)
    - ![make public](../image/image3-25.png)
    - public->secretはできないのを確認する
- fork/cloneのやり方を確認する
  - embedのプルダウンからクローンできる
  - ![embed](../image/image3-26.png)
  - forkは人のものだけなので、ハンズオンの相方のpublicなgistにアクセスしてみる
    - 右上のForkを押す
    - ![fork gist](../image/image3-27.png)

## Wikiについて

Wikiについて確認する。

- `foundations-hands-on-2`リポジトリのナビゲーションのWikiからWikiにアクセスして、読み書きしてみる
- ナビゲーションのSettings > FeaturesでWikiの権限を見てみる
  - ![Restrict editing to collaborators only Loading](../image/image3-28.png)
- 同じくナビゲーションのSettings > Featuresから、Wikiをオフにできることを確認する

## Pagesについて

GitHub Pagesについて確認する。

- `foundations-hands-on-2`リポジトリのナビゲーションのSettingsからPagesをONにする  
  - Sourceに「Deploy from branch」を選び、`main`リポジトリの`/(root)`を選択してSaveする
  - ![github pages](../image/image3-29.png)
- しばらくしてリロードしてみるとURLがでてるのでアクセスする
  - ![access github pages](../image/image3-30.png)
  - READMEの内容が見えることを確認する
- index.htmlを追加して再度アクセスすると、indexがみえる
- Settings > PagesのSourceで「GitHub Aciton」というのがあるのを確認する
  - ここでビルドしてコンテンツをデプロイする設定ができるので、時間があれば実際にやってみる

---

[前ドメインへ](../domain2/README.md)  
[次のドメインへ](../domain4/README.md)  
[目次へ](../README.md)
