# Docker環境の更新

本授業ではDockerを使います。
2年次ではDockerをLinuxのランタイムとして利用しましたが、この科目ではDockerそのものを使用します。
Dockerはコンテナ型の仮想化技術で、アプリケーションをその依存関係とともにパッケージ化して、どこでも同じように動作させることができます。

## Dockerの更新

2年次の環境であればDockerは既に入っているので、最新版に更新しましょう。

### Windows Updateの確認

DockerをWindowsで使用する場合、バックエンドとしてWSL(2)を使用します。
その関係で、OSレベルでの更新とDockerの更新が連動する構造になっています。

Windows Updateで可能な限り最新の更新が適用されていないと、Dockerの更新に影響が出るのです。

1. Windowsの設定メニュー {kbd}`Win+X`→{kbd}`N`で設定を開き、Windows Updateの項目を探す。
2. Windows Updateの項目を開き、更新プログラムの確認をクリックする。
3. 更新プログラムがある場合は、すべてインストールする。
4. 再起動が必要な場合は、再起動する。

今後は、更新の通知が出ていたら早めに適用しておくようにしましょう。

### Docker Desktopの更新

Docker Desktopは既にインストールされているはずでしょうから、ダッシュボードを開いて確認しましょう。

1. {menuselection}`設定ボタン(右上歯車ボタン)-->Software Updates`をクリックしする。
2. {menuselection}`Check for updates`をクリックする。

以上で確認できます。
更新がある場合は、適用してください。

```{note}
以下のチェックを付けておくことを推奨します。

- {menuselection}`Automatically check for updates`
- {menuselection}`Always download updates`

これらにより、自動的に最新版のダウンロードが行われるため、通知を確認したらすぐに更新には入れます。
```

### Docker CLIの確認

更新完了後、Docker環境がきちんと使えることを確認するために、ターミナルを開いてDockerのバージョンを確認しておきます。

```pwsh
PS> docker version
Docker version XXXXXXXX, build XXXXXXXX
```

```{note}
本原稿執筆時では、Docker Engineのバージョンは28.0.4-1となっていました。
ここまでは引き上げておいてください。
```
