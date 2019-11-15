# my-coder

## これ何

[code-server](https://github.com/cdr/code-server)って便利だけど環境がまっさらなので、コンテナ作成時に欲しいミドルウェアとかツール入れちゃおうと思って作ってるやつ。

## 起動時の流れ（予定）

1. Docker Composeでcode-server環境をDockerコンテナとして作成&起動
2. 起動時に`entrypoint.sh`からAnsible Playbookを実行して環境を整備する
3. Ansible Playbook実行が完了したらcode-server起動


## FAQ

### Q. Ansible PlaybookからrbenvでRubyのインストールしてるけど遅くない？

A. せやけどコンテナに溜め込むと容量かさむかなと思った。

### Q. これDockerコンテナより仮想マシン上に構築したたほうが良くない？

A. code-server環境をポイポイ建てたいんでリソース節約したかった。