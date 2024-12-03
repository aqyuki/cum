<h1 align="center">📖 README</h1>

>[!IMPORTANT]
> CUMは安定版ではありません．予告なしの破壊的変更が加えられたり、安定版では異なる動作を行う可能性が有ります．

Goで実装されたDiscord Botです．のりと勢いで、機能が増えていくので実用性に関係なく、作者が面白いと思えば実装していきます．\
コントリビューションも大歓迎ですよ(ﾁﾗ)

## ✨ Features

このBotは以下の機能を持ちます．

#### VC Diff

Voice Chatへの入退出があった場合に、指定されたチャンネルにログを出力します．

#### 時報機能

指定された時刻に、指定されたチャンネルにメッセージを送信します．

#### リマインダー

指定時刻に、リマインドメッセージを指定チャンネルに送信します．

## 🔧 Development

### 🧰 Tools

このプロジェクトでは以下のツールを利用しています．必要に応じてインストールしてください．

- Go (>=1.23.0)
- Docker (>= 27.3.1)
- [Staticcheck](https://staticcheck.dev/)
- [GCI](https://github.com/daixiang0/gci)

また、以下のツールは開発に必須ではないですが、導入することでより快適に開発を進めることが可能です．

- [Taskfile](https://taskfile.dev/)
- [gotestsum](https://github.com/gotestyourself/gotestsum)
- [octocov](https://github.com/k1LoW/octocov)

### 🌟 開発の流れ

原則、以下の流れに従って開発を行ってください．なお、既存のIssueに取り組む際には1を飛ばしても構いません．

1. GitHubにIssueを作成する．
2. Issueに取り組む際には、自身をAssignしてください．
3. `master`ブランチからブランチを切る
4. コードを作成する．必要に応じてテストを追加してください．
5. `master`ブランチに対してPRを作成する．CIとレビューを通過すると`master`にマージされます．

> [!IMPORTANT]
> 具体的なカバレッジ目標は存在しませんが、作成可能な場合は単体テストを作成してください．
> 単体テストを作成しやすいコードの設計を目指してください．

### 🔖 リリース時

通常時は以下の流れに沿って、リリースを作成します．

1. Release PleaseによるPRを`master`にマージする
2. GitHub Actionsおよび、Release Pleaseによりリリースの作成とタグの作成が行われます．
3. GitHub Actionsにより、Docker ImageがGitHub Image RegistryにPushされます．

>[!CAUTION]
> 以下の運用は、GitHub Actionによる自動リリースが不可能な場合の運用です．**(非推奨)**

1. 必要なファイルを修正します．
2. GitHubのReleaseを新規に作成する．
3. タグを作成する．タグ名はセマンティックバージョニングに則ったものにする．
4. 以降通常リリース時の3が実行されます．

### ➕ ライブラリ等の使用に関して

可能な限り、標準パッケージ → 順標準パッケージ → 独自実装 → ライブラリの順番で使用してください．
ライブラリを使用する場合には、最小限の依存で住むようにDIや抽象化を活用してください．

## 📄 License

このプロジェクトはMITライセンス下で公開されています．詳細は、[License.txt](./License.txt)を確認してください．
