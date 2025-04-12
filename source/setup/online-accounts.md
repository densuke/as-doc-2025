# 各種オンラインアカウントの準備

本科目では(他科目ともあわせて)以下のオンラインサービスのアカウントを使います。
持っていない場合は適宜作成してください。

- GitHubのアカウント
- Docker Hubのアカウント

既に持っているものがあれば、そのまま使えます。
作り方は各サイトにて指示に従えば作れるはずなので、今すぐ作成してください。

- GitHub -> [GitHubの公式サイト](https://github.com)
- Docker Hub -> [Docker Hubの公式サイト](https://hub.docker.com)

## GitHubのアカウント

GitHubのアカウントをローカルでの開発の際のコミット情報に加えておきましょう。

```{warning}
Gitコマンドが入っていない({command}`git`)とこの作業は行えません。
入っていない場合は、 [Git scm](https://git-scm.com/)からインストールしてください。
```

```pwsh
# 登録方法
PS> git config --global user.name "あなたの名前(ローマ字推奨)"
PS> git config --global user.email "あなたのGitHub登録したメールアドレス"

# 確認方法
PS> git config --global --list
user.name=あなたの名前
user.email=あなたのGitHub登録したメールアドレス
```

もし打ち間違えたときは、再度同じコマンドを実行することで上書きできます。

## Docker Hubのアカウント
2025年4月より、Docker Hubのアカウントが無い状態でDocker Hubを使用すると、レート制限にすぐに引っかかることがアナウンスされています(同一IPから1時間に10回まで)。

ということで、DockerのアカウントをDocker Desktopで登録しておきましょう。

1. Docker Desktopのダッシュボードを開く。
2. ダッシュボード右上が {menuselection}`Sign in`になっていることを確認する。
   既にイニシャルやアイコンが出ている場合はログイン済みです(以降の操作はスキップ)。
3. {menuselection}`Sign in`をクリックする。
4. ブラウザにリダイレクトされるので、Docker Hubアカウント(作成済み)でログインする。
5. ログイン後、指示に従いダッシュボードへ戻る。

設定後、ターミナルで{command}`docker`コマンドで確認しておきましょう。

```pwsh
PS> docker login
Authenticating with existing credentials... [Username: XXXXXXXXXX]

To login with a different account, run 'docker logout' followed by 'docker login'

Login Succeeded
```

```{note}
"Login Succeeded"が出るのに数秒待つことがあります。
```

以上で基本の設定は完了です。